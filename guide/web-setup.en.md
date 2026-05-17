# Web Version Setup Guide

## 1) Prerequisites
- OS: Windows / macOS / Linux
- Install Git
- Install FFmpeg (required)
- Install `uv`
- Use Python 3.10–3.12

## 2) Get Project Code (Important)
Use a **full clone with submodules**:

```bash
git clone https://github.com/Open-LLM-VTuber/Open-LLM-VTuber --recursive
cd Open-LLM-VTuber
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## 3) Install Dependencies
```bash
uv sync
```

## 4) Create or Generate `conf.yaml`
- Preferred: copy `config_templates/conf.default.yaml` to project root as `conf.yaml`
- Or run once and stop quickly:

```bash
uv run run_server.py
# Ctrl+C after startup
```

## 5) Start Backend
```bash
uv run run_server.py
```

Default web URL:
- `http://localhost:12393`

## 6) First-Run Recommended Check
- Confirm WebSocket in frontend points to `ws://127.0.0.1:12393/client-ws`
- Confirm LLM endpoint works (for Ollama: `http://localhost:11434/` should be reachable)

## 7) Remote Access Notes
For microphone/camera/screen capture on remote devices, serve with **HTTPS** (secure context required by browsers).

## 8) Common Problems
- `{"detail":"Not Found"}` → frontend submodule missing, run `git submodule update --init --recursive`
- Port in use (`12393`) → close other instance or change `system_config.port` in `conf.yaml`
