# Configuration

oracle framework provides a flexible configuration system that allows you to customize your agent's personality, behavior, and platform settings. This section will delve into the details of character setup, environment variables, LLM providers, and model selection.

## Character Setup

The `characters.json` file in the `src/characters` directory is the central place to configure your agent's personality, behavior, and platform-specific settings.

### Personality, Behavior, and Platform Settings

Within each agent object in `characters.json`, you can define various attributes:

* `postingBehavior`: Defines the posting frequency, removal of periods, chance of posting images, and rules for chat interaction.

* `imageGenerationBehavior`: Specifies the provider and model for image generation, along with provider-specific settings.

* `audioGenerationBehavior`: Configures the provider and settings for audio generation.

* Platform-specific settings: Includes `telegramBotUsername` for Telegram and `discordBotUsername` for Discord.

### Key Configuration Fields

Some of the key configuration fields in `characters.json` include:

* `model`: The primary language model for generating agent responses (e.g., "anthropic/claude-3.5-sonnet").

* `fallbackModel`: The fallback language model to use if the main model fails or a prompt is banned.

* `temperature`: Controls the "creativity" and "randomness" of the generated responses.

## Environment Variables

oracle framework uses environment variables to store sensitive information and configuration options. The `.env` file in the project root directory is used to set these variables.

* `LLM_PROVIDER_URL`: The URL of the LLM provider's API.

* `LLM_API_KEY`: The API key for the LLM provider.

* `AGENT_TWITTER_PASSWORD`: The password for the agent's Twitter account.

* `AGENT_TELEGRAM_API_KEY`: The API key for the agent's Telegram bot.

* `AGENT_DISCORD_API_KEY`: The API key for the agent's Discord bot.

## LLM Providers

oracle framework supports various LLM providers, allowing you to choose the one that best suits your needs.

### OpenRouter (Recommended)

OpenRouter is the recommended LLM provider for oracle framework. It offers a wide range of models and an easy-to-use API. To use OpenRouter, set the following environment variables:

```bash
LLM_PROVIDER_URL=https://openrouter.ai/api/v1
LLM_PROVIDER_API_KEY=your_openrouter_api_key
```

### RedPill

RedPill is another LLM provider compatible with oracle framework. To use RedPill, set the following environment variables:

```bash
LLM_PROVIDER_URL=https://api.redpill.ai/v1
LLM_PROVIDER_API_KEY=your_redpill_api_key
```

### OpenAI

OpenAI can also be used as an LLM provider, but it has limitations on available models. To use OpenAI, set the following environment variables:

```bash
LLM_PROVIDER_URL=https://api.openai.com/v1
LLM_API_KEY=your_openai_api_key
```

## Model Selection

oracle framework allows you to specify the primary and fallback language models for your agent in the `characters.json` file.

The recommended primary model is "anthropic/claude-3.5-sonnet", which excels at creative writing tasks. The recommended fallback model is "meta-llama/llama-3.3-70b-instruct", as it has no content restrictions compared to Claude.

For chat mode interactions, "meta-llama/llama-3.3-70b-instruct" is the recommended model due to its responsiveness and, since it's a largely unmoderated model, we don't check for "banned" replies making the interactions faster.

When using OpenAI as the LLM provider, ensure that the models specified in `characters.json` are compatible with OpenAI's offerings.
