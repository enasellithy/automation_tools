# 🤖 AI Legacy Docs Crawler

An automated GitHub Action that crawls your PHP/Laravel legacy codebase and generates technical documentation using Local AI (Ollama).

## ✨ Features
- **Incremental Documentation:** Uses a tracker file to avoid re-processing unchanged files.
- **Batch Mode:** Processes files in small batches to stay within CI/CD time limits.
- **Local AI:** Powered by `qwen2.5-coder:1.5b` via Ollama for privacy and speed.
- **High Performance:** Optimized caching strategies for sub-2-minute execution.

## 🚀 How it Works
1. The action scans specific directories (e.g., `Dir1/SubDir`, `Dir2/SubDir`).
2. It checks against `.ai_docs_tracker.txt` to find undocumented files.
3. It sends the code to Ollama to generate a structured Markdown table.
4. It prepends the new documentation to `TECHNICAL_DOCS.md` and commits the changes.

## 🛠 Setup
1. Create a folder `.github/workflows/` in your repo.
2. Add the `ai-docs-generator.yml` file.
3. Configure your `TARGET_PATHS` in the script.
4. Run manually or push code to trigger the magic!
