彤靈談心 Prototype v16.5 — Modern Agent Session UI

本版重新設計 Agent Mode，使其更接近現代 Agent 操作介面，而不是「儀表板」。

Agent Mode 預設畫面：
- 單一 Agent Session Thread
- 使用者訊息 / Agent 進度以對話串呈現
- 簡潔的工作 Todo / Progress
- Tool activity 使用可折疊卡片
- 預設 Focus：隱藏完成的工具細節
- 「活動」可切換較詳細模式
- Bottom Composer 永遠可補充指示
- 執行中輸入會排入下一個安全工具邊界
- Composer 上方顯示 Live Work Banner
- 需要人時使用 Blocking Decision Modal / Mobile Bottom Sheet
- 完成後直接顯示 PRD.docx 下載

Agent Mode 不顯示完整 9-step 頁面。
Manual Mode 仍完整保留 v12 / v16 所有流程與工具。

核心：
Agent Mode = Session / Work Stream
Manual Mode = Workflow / Expert Console
兩者使用同一份 Workflow State。
