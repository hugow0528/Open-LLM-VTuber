# Web 版本安裝指南

## 1）環境需求
- 作業系統：Windows / macOS / Linux
- 安裝 Git
- 安裝 FFmpeg（必要）
- 安裝 `uv`
- Python 版本建議 3.10–3.12

## 2）取得專案程式碼（重要）
請使用**含 submodule 的完整 clone**：

```bash
git clone https://github.com/Open-LLM-VTuber/Open-LLM-VTuber --recursive
cd Open-LLM-VTuber
```

若你先前沒加 `--recursive`：

```bash
git submodule update --init --recursive
```

## 3）安裝依賴
```bash
uv sync
```

## 4）建立或產生 `conf.yaml`
- 建議做法：複製 `config_templates/conf.default.yaml` 到專案根目錄並改名為 `conf.yaml`
- 或先啟動一次再中止：

```bash
uv run run_server.py
# 啟動後按 Ctrl+C
```

## 5）啟動後端
```bash
uv run run_server.py
```

預設網頁網址：
- `http://localhost:12393`

## 6）首次啟用建議檢查
- 前端 WebSocket 位址是否為 `ws://127.0.0.1:12393/client-ws`
- LLM 端點是否可用（若用 Ollama，請確認 `http://localhost:11434/` 可連線）

## 7）遠端存取注意事項
若要在其他裝置使用麥克風／攝影機／錄屏，必須配置 **HTTPS**（瀏覽器安全上下文限制）。

## 8）常見問題
- `{"detail":"Not Found"}` → 通常是 frontend submodule 未拉下來，執行 `git submodule update --init --recursive`
- 12393 連接埠被占用 → 關閉另一個後端，或修改 `conf.yaml` 的 `system_config.port`
