# App (Electron) Setup Guide

## 1) Concept
The app version is an Electron frontend. It still requires the backend (`Open-LLM-VTuber`) running.

## 2) Install and Start Backend
In this repository:

```bash
uv sync
uv run run_server.py
```

Keep backend running.

## 3) Download Desktop App
Download the Electron package from:
- `Open-LLM-VTuber-Web` Releases

Choose your platform installer (Windows/macOS).

## 4) Install and Launch App
- Windows may show “Windows protected your PC” → click **More info** → **Run anyway**
- macOS may show unsigned app warnings; allow in Security settings if needed

## 5) Connect to Backend
- Backend default host/port: `localhost:12393`
- WebSocket target: `ws://127.0.0.1:12393/client-ws`

## 6) Modes
- Window mode: regular desktop window
- Pet mode: transparent, always-on-top desktop companion
- You can switch modes from tray menu or right-click menu in pet mode

## 7) Notes
- App update is currently manual (check release page)
- App and web settings are stored locally (localStorage)
