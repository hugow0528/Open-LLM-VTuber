# App Usage Guide (Window + Pet Mode, Button-Focused)

## 1) Before Using
- Backend must be running: `uv run run_server.py`
- Launch Electron app
- Confirm WebSocket connected

## 2) Window Mode (Buttons and Controls)
Window mode is functionally the same as Web mode, plus desktop app controls.

### Sidebar controls
- **Settings**: open configuration drawer
- **History**: open conversation history
- **New Conversation**: start a new chat
- **Sidebar Fold Button**: collapse/expand sidebar

### Main panel controls
- **Connection status / reconnect icon**: shows WS status; reconnect when disconnected
- **Live2D model area**: drag model; optional click interactions

### Bottom controls
- **Mic Button**: enable/disable microphone capture
- **Interrupt Button**: stop current AI speech immediately
- **Text Input + Send**: send text message to AI
- **Bottom Fold Button**: collapse/expand bottom panel

### Settings drawer tabs
- **General**: connection, background, subtitle, character preset
- **Live2D**: interaction and scaling behavior
- **ASR**: speech threshold and auto-mic behavior
- **TTS**: model-related options (if available)
- **Agent**: proactive speaking behavior
- **About**: project/app info

## 3) Pet Mode (Buttons and Menus)
Pet mode adds transparent always-on-top behavior.

### Right-click model menu
- **Mic On/Off**
- **Interrupt current conversation**
- **Enable/Disable scaling**
- **Show/Hide input box and subtitle**
- **Switch mode (pet/window)**
- **Switch character**
- **Hide app / Exit app**

### Input/subtitle floating panel
- Draggable
- Can be shown/hidden
- Includes mic toggle, interrupt button, text input

## 4) System Tray Menu
- Show/hide window
- Switch mode
- Quick exit

## 5) Practical Flow
1. Start backend
2. Open app and verify connection
3. Choose window or pet mode
4. Use mic or text input
5. Use interrupt when needed
6. Save/reopen history from sidebar
