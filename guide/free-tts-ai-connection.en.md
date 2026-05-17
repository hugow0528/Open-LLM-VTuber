# Free AI/TTS/ASR Connection Guide (Recommended)

## Goal
Build a low-cost (or free) stack first, then upgrade only when needed.

## Recommended Free Baseline
- **LLM**: Ollama (local)
- **ASR**: `sherpa_onnx_asr` (default, local)
- **TTS**: `edge_tts` (no API key, online) or `pyttsx3_tts` (fully local)

## A) Free Local AI (LLM) via Ollama
1. Install Ollama
2. Pull/run model:
   ```bash
   ollama run qwen2.5:latest
   ```
3. In `conf.yaml`:
   - `agent_config->agent_settings->basic_memory_agent->llm_provider: ollama_llm`
   - `agent_config->llm_configs->ollama_llm->model: qwen2.5:latest`

## B) Free ASR (Speech to Text)
Default is already local:
- `asr_config.asr_model: sherpa_onnx_asr`

If you need better multilingual cloud ASR with free quota:
- use `groq_whisper_asr` + API key

## C) Free TTS
### Option 1: edge_tts (easy)
- `tts_config.tts_model: edge_tts`
- No API key required, but internet is required

### Option 2: pyttsx3_tts (fully local)
- Usually no extra install is needed in this repository setup.
- If your environment is missing it, install with:
  ```bash
  uv add pyttsx3
  ```
- Set `tts_config.tts_model: pyttsx3_tts`

## D) Fully Offline Suggestion
- LLM: Ollama local model
- ASR: sherpa_onnx_asr
- TTS: pyttsx3_tts or local sherpa-onnx/piper model

## E) Start and Verify
```bash
uv run run_server.py
```
Check:
- Open `http://localhost:12393`
- WebSocket connected
- Mic input recognized
- AI replies with voice output
