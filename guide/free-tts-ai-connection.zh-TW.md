# 免費 AI / TTS / ASR 連接指南（建議組合）

## 目標
先用低成本（甚至免費）組合跑通，再視需求升級。

## 建議免費基線
- **LLM**：Ollama（本地）
- **ASR**：`sherpa_onnx_asr`（預設、本地）
- **TTS**：`edge_tts`（免 API Key、需網路）或 `pyttsx3_tts`（全本地）

## A）免費本地 AI（LLM）- Ollama
1. 安裝 Ollama
2. 下載/啟動模型：
   ```bash
   ollama run qwen2.5:latest
   ```
3. 修改 `conf.yaml`：
   - `agent_config->agent_settings->basic_memory_agent->llm_provider: ollama_llm`
   - `agent_config->llm_configs->ollama_llm->model: qwen2.5:latest`

## B）免費語音辨識（ASR）
預設即為本地：
- `asr_config.asr_model: sherpa_onnx_asr`

若需要多語系雲端且有免費額度，可考慮：
- `groq_whisper_asr` + API key

## C）免費語音合成（TTS）
### 選項 1：edge_tts（簡單）
- `tts_config.tts_model: edge_tts`
- 不需 API Key，但需要網路

### 選項 2：pyttsx3_tts（全離線）
- 若你要使用此引擎，請先安裝依賴：
  ```bash
  uv add pyttsx3
  ```
- 設定 `tts_config.tts_model: pyttsx3_tts`

## D）全離線建議
- LLM：Ollama 本地模型
- ASR：sherpa_onnx_asr
- TTS：pyttsx3_tts 或本地 sherpa-onnx/piper

## E）啟動與驗證
```bash
uv run run_server.py
```
確認：
- 可開啟 `http://localhost:12393`
- WebSocket 已連線
- 麥克風可辨識
- AI 回覆可正常語音播放
