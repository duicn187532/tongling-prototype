彤靈談心 Prototype v16.3

UX 修正：Agent 等待／需要使用者確認時，改為主動彈窗，不要求使用者自行往頁面下方找問題。

新增 Proactive Human Interruption Modal：

1. 缺需求起點
   - 自動彈窗
   - 前往輸入需求 / 選擇需求文件 / 切手動模式

2. MEETING_REQUIRED
   - 自動彈窗顯示「為什麼要開會」
   - 參與角色
   - 共同可用時間
   - 直接確認會議 / 下載 ICS / 改手動處理

3. WAITING_MEETING
   - 會議確認後再顯示等待視窗
   - 告知 Agent 已保存狀態
   - Prototype 可直接模擬會議完成 / 下載 ICS / 稍後處理

4. Step 6 Human Exception
   - Agent 只剩 R01 Scope Change 時主動彈窗
   - 可直接接受建議 / 修改 / 查看完整人工確認頁

5. Step 8 PRD Final Review
   - PRD 產生完成後主動彈窗
   - 直接前往審閱 PRD / 稍後審閱

設計原則：
- Human-in-the-loop 必須由 Agent 主動找人，不是讓人自己找 Agent 卡在哪。
- 彈窗只在真正阻塞 Agent 或需要 Human Gate 時出現。
- 關閉彈窗不會把事項視為已完成；原 Step 仍保留完整操作與稽核內容。
