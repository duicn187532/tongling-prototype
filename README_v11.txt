彤靈談心 Prototype v11

v11 新增：設定頁（不列入 9 步需求流程）
入口：左側「AI 與系統設定」

設定分類
1. AI 模型與連線
   - Cloud API：OpenAI、Anthropic、Google Gemini、Azure OpenAI、Mistral AI、Cohere、AWS Bedrock、OpenAI-compatible API
   - Local / Self-hosted：Ollama、LM Studio、vLLM / Local Endpoint、llama.cpp Server
   - Mock Mode
   - Model ID、Base URL、API Key、Timeout、連線測試（皆為 Prototype 模擬）
2. 任務模型路由
   - Requirement Matrix
   - 衝突／變更辨識
   - Knowledge Query Generation
   - Meeting Assistant
   - PRD
   - Mermaid / Architecture
   - Embedding / Reranker
   - Fallback
3. Knowledge Retrieval / RAG
   - Top-K、Evidence K、最低相關度
   - Chunk Size / Overlap
   - Hybrid Search
   - Recency / Authority Boost
   - Strict Evidence Mode
4. 安全與隱私
   - Local-only
   - 只傳必要 Evidence Chunk
   - PII Mask
   - AI Log / File Retention
5. 會議助理
   - 即時問題
   - Decision / Change 偵測
   - 敏感度 / 批次 / 摘要格式
6. PRD 與輸出
   - 語言
   - PRD Template
   - Export Format
   - Traceability / Open Issues / Diagrams / Meeting Summary
7. 進階
   - Temperature
   - Max Tokens
   - Confidence Threshold
   - Escalation / Conflict Evidence Guardrail
   - 成本上限
   - Custom System Prompt

快速 Preset
- Local-first / 零 API 費用
- Cloud API / 快速驗證
- Bank Guardrail / 嚴格來源模式
- Demo Mock Mode

重要：
- Prototype 不會真的連線或送出 API Key。
- API Key 在正式產品不應存瀏覽器 LocalStorage，應改由後端 Secret / Vault 管理。
- 設定儲存只保存非敏感設定到本機瀏覽器 LocalStorage。
