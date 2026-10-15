彤靈談心 Prototype v16 — Agent-Assisted Requirement Workflow

設計原則：
「流程保留，操作減少。」

完整保留 v12 的 9 個能力：
1. 需求說明
2. 知識檢索
3. 補充資料／競品
4. 會議助理
5. AI 分析
6. 人工確認
7. 流程／架構
8. 預覽 PRD
9. 下載 PRD

Agent 是 Workflow Proxy / Orchestrator：
- Step 1：使用者輸入。
- Step 2：Agent 自動搜尋並加入 Evidence。
- Step 3：Agent 補 SA，判斷競品可 Skip。
- Step 4：Agent 先分析既有 Meeting；若 Step 5 發現跨角色 blocker，Loop 回 Step 4 安排追加會議。
- Step 5：Agent 自動執行 Requirement Intelligence；Meeting 完成後只重跑受影響分析。
- Step 6：Agent 先代辦 Evidence 充分、不需裁量的項目，只把 Scope/Risk/Compliance 例外留給人。
- Step 7：Agent 自動產流程／架構。
- Step 8：Human 最後審閱 PRD。
- Step 9：下載 PRD。

Agent / Human 可隨時切換；手動模式仍可完整操作 v12 原流程。

Meeting：
- 模擬 Directory 解析 required roles。
- Calendar 採 Free/Busy First。
- 產生 RFC5545 .ics。
- WAITING_MEETING 保存流程狀態。
- 會議結果加入後 Agent Resume。

最終輸出：
- Primary：PRD.docx 情境版。
- Secondary：依畫面決策動態產出的 Word .doc。
