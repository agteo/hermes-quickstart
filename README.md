# hermes-railway

One-click Railway deployments for [Hermes Agent](https://github.com/NousResearch/hermes-agent), a self-improving autonomous AI agent with Telegram support.

## Agents

A single starter agent is included in the template, pre-configured for OpenRouter:

| Agent | Provider | Default Model |
|---|---|---|
| [start-openrouter](agents/start-openrouter) | OpenRouter | `openai/gpt-5.4-mini` |

## Deploy

[![Deploy Hermes agents on Railway](https://railway.com/button.svg)](https://railway.com/deploy/hermes-agent-deploy?referralCode=id0ivo&utm_medium=integration&utm_source=template&utm_campaign=generic)

Set the Railway root directory to `agents/start-openrouter` when deploying.

## Configuration

Set the following environment variables in Railway after deploying:

### start-openrouter

| Variable | Required | Description |
|---|---|---|
| `OPENROUTER_API_KEY` | Yes | OpenRouter API key |
| `TELEGRAM_BOT_TOKEN` | Yes | Telegram bot token from [@BotFather](https://t.me/botfather) |
| `TELEGRAM_ALLOWED_USERS` | No | Comma-separated Telegram user IDs. Empty allows all |
| `HERMES_MODEL` | Yes | Preset examples: `openai/gpt-5.4-mini` or `google/gemini-2.5-flash` |

## Persistence

A Railway volume is required, mounted at `/data`. Sessions, memory, skills, and agent config persist across restarts.

## License

MIT
