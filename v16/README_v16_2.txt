彤靈談心 Prototype v16.2

本版只調整 UI / UX，不改 v16.1 的功能流程與 Agent 邏輯。

主要調整
1. 手機 RWD 重做成 AI 助理型介面：
   - Sticky mobile header
   - 9-step workflow 改為 off-canvas drawer
   - Agent / Manual 控制列在手機上保持易操作
   - 下一步／上一步固定於底部，類似 AI 助理的 action composer
   - 所有主要按鈕、輸入框符合手機觸控尺寸
   - iOS 輸入框使用 16px，避免自動縮放
   - PRD、Meeting、表格、流程圖針對小螢幕重排或橫向滑動

2. 移除／隱藏冗餘說明：
   - 移除首頁 marketing Hero
   - 移除 9-step 大型操作說明卡
   - 移除 Agent REQUIRED / CONDITIONAL / HUMAN 三張解說卡
   - 移除每一步重複的 Agent 說明 banner
   - 移除側欄 Prototype 長篇說明
   - Settings 頁保留設定功能，縮短介紹文字

3. 保留真正有操作價值的資訊：
   - Agent 當前正在做什麼
   - Agent / Manual 切換
   - Step 狀態
   - Human Exception
   - Meeting / WAIT / RESUME
   - PRD 預覽與下載

功能核心仍為：
v12 9-step workflow + v16 Agent 代辦。
