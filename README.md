# POCLI Models Catalog

Official model catalog for [**POCLI**](https://github.com/artificial-intelligence-engineering/pocli).

`pocli models refresh` (and `/models refresh` in the TUI) fetches [`models.json`](https://raw.githubusercontent.com/artificial-intelligence-engineering/models/main/models.json) from `main` using HTTP `ETag` + SHA-256 comparison to detect added, updated, or removed models without requiring a new CLI release.

## Schema

Each entry in `models.json` must include:

- `provider`: Provider ID (e.g. `opencode`, `openrouter`, `anthropic`, `openai`, `gemini`, `groq`, `ollama`, `freellm`)
- `vendor`: Display vendor badge (e.g. `OPENCODE`, `GEMINI`, `ANTHROPIC`)
- `providerLabel`: Human-readable provider name
- `modelId`: Model identifier sent to the provider API
- `displayName`: Label shown in the `/models` selector
- `isFree`: Boolean indicating whether the model is free-tier
- `contextWindow`: Context size label (e.g. `"128K"`, `"1M"`)
- `recommendedFor`: Short capability note
- `defaultTemperature`: Numeric default temperature
