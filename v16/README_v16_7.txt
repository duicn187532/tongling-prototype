彤靈談心 Prototype v16.7 — Resumable Agent Session UI

本版不是單純修動畫，而是重整 Agent / Manual 的狀態控制。

主要修正
1. Agent Mode / Manual Mode 與 Agent Runtime 分離
   - 切換 UI 模式不再直接破壞 agentRunning / checkpoint。
   - Manual takeover 會使舊的 async run 失效，避免背景流程繼續亂寫狀態。

2. 新增 run epoch / controlled stop
   - Agent 每次執行都有 epoch。
   - 切手動、暫停、重新執行都會 invalid 舊 run。
   - 舊 async 在下一個安全邊界停止，不會繼續推進。

3. 切回 Agent 會先 derive resume plan
   - 不再一律從知識檢索重跑。
   - 可恢復：Meeting Required、WAITING_MEETING、Post Meeting、Human Exception、
     Flow / PRD 組裝、Final Review、PRD Ready。

4. 新增 agentMeetingScheduled
   - 解決安排會議後切手動，再切 Agent 又重複要求開會的問題。

5. Human Decision 可跨模式續接
   - 若在 Manual 完成 Scope 決策，切回 Agent 會直接接 Step 7 / PRD，不會卡住。

6. Manual 修改會標示 downstream stale
   - 切回 Agent 從受影響最早 Step 重新檢查。
   - 不會假裝既有 Analysis / PRD 還有效。

7. Pause 統一
   - Desktop / Mobile / Manual 只使用一套 pause state。
   - Resume 後會重新 derive checkpoint。

8. Decision Modal dismiss != resolve
   - 關閉決策窗後，Composer 上方保留「需要你的決定」狀態。
   - 點狀態可重新打開決策窗。

9. Agent 執行中補充指示
   - 不會硬中斷正在執行的工具交易。
   - 在下一個安全 boundary 重新評估。

10. 進度改為 monotonic
    - REVISIT / 回查不會讓百分比突然倒退。

11. 模式切換更柔和
    - 新增短暫 transition overlay。
    - Manual Mode 會直接落在相關 Step，並顯示「交還 Agent」banner。

12. Agent 附件
    - 不再為了選檔案強制切到 Manual Mode。

驗證
- JavaScript syntax check
- DOM id audit
- Pure resume planner transition tests

補充嚴格檢查：resume planner 已擴充為 14 個 transition cases，包含不同 workflow readiness 與 downstream stale 路徑。
