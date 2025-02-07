# Environment Setup

![img](../assets/images/environment-setup.jpg)

Before you can start running your oracle agent, you need to configure your environment variables and set up the necessary credentials for the LLM provider and social media platforms. This section will guide you through the process of setting up your `.env` file and obtaining the required tokens and credentials.

## Configuring the .env File

1. In the root directory of your oracle framework project, locate the `.env.example` file.

2. Create a copy of this file and rename it to `.env`.

3. Open the `.env` file in your preferred text editor.

4. Fill in the required environment variables as described in the following sections.

!!! note
    The only REQUIRED fields are `LLM_PROVIDER_URL` and `LLM_PROVIDER_API_KEY`. You don't need to supply a Discord API key if you're not going to deploy your agent to Discord. The same applies to all platforms. You can always use the CLI mode to start interacting with your agent.

## LLM Provider Credentials

oracle framework supports various LLM providers, such as OpenRouter, RedPill, and OpenAI. To use an LLM provider, you need to get the necessary credentials and add them to your `.env` file.

### OpenRouter (Recommended)

1. Sign up for an account at OpenRouter.

2. Obtain your API key from the OpenRouter dashboard.

3. In your `.env` file, set the following variables:

```bash
LLM_PROVIDER_URL=https://openrouter.ai/api/v1
LLM_PROVIDER_API_KEY=your_openrouter_api_key
```

### RedPill

1. Sign up for an account at RedPill.

2. Obtain your API key from the RedPill dashboard.

3. In your `.env` file, set the following variables:

```bash
LLM_PROVIDER_URL=https://api.redpill.ai/v1
LLM_PROVIDER_API_KEY=your_redpill_api_key
```

### OpenAI

1. Sign up for an account at OpenAI.

2. Obtain your API key from the OpenAI dashboard.

3. In your `.env` file, set the following variables:

```bash
LLM_PROVIDER_URL=https://api.openai.com/v1
LLM_PROVIDER_API_KEY=your_openai_api_key
```

## Twitter Account Credentials

To enable your oracle agent to interact with Twitter, you need to provide your Twitter account credentials in the `.env` file.

1. In your `.env` file, set the following variable:

```bash
AGENT_TWITTER_PASSWORD=your_twitter_account_password
```

## Telegram Bot Token

To run your oracle agent on Telegram, you need to create a bot and obtain its token.

1. Start a conversation with the BotFather on Telegram.

2. Follow the instructions to create a new bot and obtain its token.

3. In your `.env` file, set the following variable:

```bash
AGENT_TELEGRAM_API_KEY=your_telegram_bot_token
```

## Discord Bot Token

To run your oracle agent on Discord, you need to create a bot and obtain its token.

1. Go to the Discord Developer Portal.

2. Create a new application and add a bot to it.

3. Obtain the bot token from the "Bot" section of your application settings.

4. In your `.env` file, set the following variable:

```bash
AGENT_DISCORD_API_KEY=your_discord_bot_token
```

With your `.env` file configured and the necessary credentials in place, you're now ready to create your agent and start running it on various platforms. 