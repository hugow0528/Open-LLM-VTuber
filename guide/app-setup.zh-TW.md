# App（Electron）版本安裝指南

## 1）先理解架構
App 版本是 Electron 前端，仍然需要本倉庫的後端服務持續運行。

## 2）先安裝並啟動後端
在此倉庫執行：

```bash
uv sync
uv run run_server.py
```

後端請保持運行。

## 3）下載桌面客戶端
到以下頁面下載：
- `Open-LLM-VTuber-Web` Releases

請下載對應平台（Windows/macOS）安裝包。

## 4）安裝與啟動 App
- Windows 若出現「Windows 已保護你的電腦」→ 點 **更多資訊** → **仍要執行**
- macOS 若提示未簽名或損毀，請到系統安全性設定允許後再開啟

## 5）連線到後端
- 後端預設位址：`localhost:12393`
- WebSocket 目標：`ws://127.0.0.1:12393/client-ws`

## 6）模式說明
- 視窗模式：一般桌面視窗
- 桌寵模式：透明背景、全局置頂
- 可透過系統托盤或桌寵右鍵選單切換

## 7）補充
- 目前桌面端更新需手動至 release 頁面下載
- App 與 Web 的個人化設定會存在本機 localStorage
