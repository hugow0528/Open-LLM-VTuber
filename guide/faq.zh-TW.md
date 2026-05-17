# 常見問題（FAQ）

## Q1. Web 出現 `{"detail":"Not Found"}`
通常是前端 submodule 沒有拉下來。

修正：
```bash
git submodule update --init --recursive
```

## Q2. 已安裝 `uv` 但找不到指令
請重新開啟終端機/IDE，或重新載入 shell 設定。

## Q3. `Error calling the chat endpoint...`
多半是 LLM 連線或設定錯誤。
請檢查：
- LLM `base_url` 與 API key
- 模型名稱是否拼錯
- Ollama 是否啟動（`http://localhost:11434/`）
- 代理是否攔截 localhost

## Q4. 12393 埠號被占用
請勿同時啟動多個後端，或修改 `conf.yaml` 的 `system_config.port`。

## Q5. 麥克風無法使用
- 確認已授權麥克風
- 說話音量與時長要足夠
- 調整 ASR 閾值
- 若是遠端 Web，需使用 HTTPS

## Q6. App 被系統安全機制阻擋
- Windows：更多資訊 → 仍要執行
- macOS：在安全性設定中允許（未簽名應用警告）

## Q7. 可以用手機嗎？
可部分使用。後端仍需跑在電腦上；手機 Web 若要用麥克風/攝影機需 HTTPS。

## Q8. 前端 App 如何更新？
目前需到 release 頁面手動下載更新。

## Q9. 可以完全離線嗎？
可以。請使用本地 LLM + 本地 ASR + 本地 TTS。

## Q10. ASR/TTS 測試頁在哪裡？
`http://localhost:12393/web-tool`
