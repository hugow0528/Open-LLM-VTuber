# Frequently Asked Questions (FAQ)

## Q1. Web shows `{"detail":"Not Found"}`
Frontend submodule is missing.

Fix:
```bash
git submodule update --init --recursive
```

## Q2. `uv` installed but command not found
Restart terminal/IDE or reload shell profile.

## Q3. `Error calling the chat endpoint...`
Usually LLM connection/config issue.
Check:
- LLM `base_url` and API key
- Model name typo
- Ollama is running (`http://localhost:11434/`)
- Proxy does not block localhost

## Q4. Port 12393 already in use
Only run one backend instance, or change `system_config.port` in `conf.yaml`.

## Q5. Microphone does not work
- Grant mic permission
- Increase speech duration/volume
- Tune ASR threshold
- For remote web usage, use HTTPS

## Q6. App blocked by OS security warning
- Windows: More info → Run anyway
- macOS: allow app in Security settings (unsigned app warning)

## Q7. Can I use mobile?
Partially. Backend still runs on computer. For mobile web mic/camera, HTTPS is required.

## Q8. How to update frontend app?
Desktop app update is currently manual from release page.

## Q9. Can I run fully offline?
Yes. Use local LLM + local ASR + local TTS.

## Q10. Where is web tool for ASR/TTS testing?
`http://localhost:12393/web-tool`
