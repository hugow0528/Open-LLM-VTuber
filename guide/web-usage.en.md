# Web Usage Guide

## 1) Open Web UI
- Start backend: `uv run run_server.py`
- Open: `http://localhost:12393`

## 2) Main Layout
- Sidebar: settings, history, new conversation
- Main area: Live2D model, background, subtitles, connection status
- Bottom bar: AI status, mic switch, interrupt, text input

## 3) Settings Overview
### General
- Language (if available)
- Background image / custom URL / camera background
- Character preset
- WebSocket URL
- Base URL
- Subtitle on/off

### Live2D
- Mouse interaction on/off
- Scale on/off (wheel/pinch)

### ASR
- Auto mic control
- Speech detection thresholds

### Agent
- AI proactive speaking on/off
- Idle time before proactive speaking

## 4) Conversation Methods
- Voice input (mic permission required)
- Text input
- Proactive AI speaking (if enabled)

## 5) Interrupt Behavior
Interrupt can be triggered by:
- Interrupt button
- Talking while AI is speaking (mic must be on)
- Sending message while AI is speaking

## 6) History
- Scroll current chat
- Open history drawer to load/delete saved conversations

## 7) Live2D Interaction
- Drag to move
- Wheel/pinch to zoom
- Optional look-at and click actions (depends on config)

## 8) Remote Usage
Use HTTPS for mic/camera/screen capture on non-localhost devices.
