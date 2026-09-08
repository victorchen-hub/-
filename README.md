# AI 入門指南

這個倉庫新增了「常用 AI 範例」與說明，包含 ChatGPT (OpenAI) 與 Gemini/Google Generative Language 的簡單示範，方便你快速上手。

新增檔案與目錄：

- README.md（本檔）
- examples/python/demo_chatgpt.py（使用 OpenAI 的 ChatGPT 範例）
- examples/python/demo_gemini.py（使用 Google Generative Language REST API 的簡單範例，可用於 Gemini）
- requirements.txt（Python 依賴）
- .env.example（需要設定的環境變數範例）
- .github/workflows/ai-ci.yml（CI：安裝相依並執行範例，但若沒設定 secrets 會略過）

快速開始

1. 在本機建立虛擬環境並安裝依賴：

   python -m venv .venv
   source .venv/bin/activate  # macOS / Linux
   .\.venv\Scripts\activate  # Windows (PowerShell)
   pip install -r requirements.txt

2. 設定環境變數（見 .env.example）或在系統環境中加入：
   - OPENAI_API_KEY：OpenAI API 金鑰（ChatGPT）
   - GOOGLE_API_KEY：Google Generative Language API Key（若使用 Google）

3. 執行範例：
   python examples/python/demo_chatgpt.py
   python examples/python/demo_gemini.py

CI 說明

GitHub Actions workflow (.github/workflows/ai-ci.yml) 會在 push 時安裝相依並執行兩個範例腳本。為避免 CI 因沒有 secrets 而失敗，範例腳本在找不到 API 金鑰時會印出跳過訊息並以 0 結束。

注意

- Gemini 的接入方式可能會隨時間改變；examples/python/demo_gemini.py 使用 Google 的 Generative Language REST API 範例端點（text-bison-001）。若你使用其他 Gemini API 或官方 SDK，請依你的授權/端點修改範例。
- 請勿在公開倉庫直接提交金鑰；請使用 GitHub Secrets 或 CI 的 secret 機制。
