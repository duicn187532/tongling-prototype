彤靈談心 Prototype v16.4 — Immersive Agent Mode

本版重點：
Agent 模式不再顯示完整 workflow UI，只保留：
1. Agent 目前狀態
2. 整體流程進度
3. 目前正在處理哪個 Step
4. 最近少量進度紀錄
5. 暫停 / 手動模式
6. 需要人時主動彈出的決策窗
7. 完成後的 PRD 下載

完整 v12 9-step 功能仍存在，但只在「手動模式」顯示。

Agent Mode
- 沉浸式單畫面
- 不顯示 sidebar / step pages / footer / 大量設定與資訊卡
- Agent 內部仍正常操作原本 9-step DOM / workflow
- 使用者不需看 Agent 如何操作每一步
- 需要人類輸入、會議、Scope 決策、PRD Final Review 時才主動彈窗

Requirement Input
- 改為直接在 Agent 決策窗輸入，不需跳回 Step 1。

Final PRD Review
- 決策窗可直接確認 PRD 完成
- 或切換到手動模式查看完整 PRD

Manual Mode
- 完整保留 v12 / v16.3 全功能頁面
- 可隨時切回 Agent Mode，流程狀態不丟失
