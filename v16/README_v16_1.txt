彤靈談心 Prototype v16.1

修正項目：
1. 修正 Agent 在 Step 2「知識檢索」呼叫錯誤 DOM ID：
   genKbQuery → generateKbQuery
2. Agent 不再用固定 1.45 秒等待知識搜尋，而是等待 kbResults 真正完成顯示。
3. 加入 waitUntil()，確保 4 份建議知識已成功加入後才進 Step 3。
4. Agent 發生錯誤時會顯示實際錯誤訊息，方便定位。

原 v16 設計維持不變：
- 保留 v12 9-step workflow
- Agent 在原流程中代辦
- 支援 Manual takeover
- Step 5 可 REVISIT Step 2 / 3 / 4
- Meeting WAIT / RESUME
