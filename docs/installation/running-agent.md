# Running Your Agent

Once you have created your agent and configured the necessary environment variables, you can start running your agent. This section will guide you through the process of running your agent using the command line interface and integrating it with Twitter, Telegram, and Discord.

## Command Line Interface

The command line interface (CLI) allows you to interact with your agent directly from the terminal. To start your agent in CLI mode, run the following command:

```bash
npm run dev -- cli <username>
```

Replace `<username>` with the username of the agent you want to interact with. For example:

```bash
npm run dev -- cli carolainetrades
```

In CLI mode, you can type messages and receive responses from your agent in real-time.

## Twitter Integration

oracle framework provides seamless integration with Twitter, enabling your agent to generate tweets, respond to mentions, and engage with followers.

### Generating Twitter Authentication

Before your agent can interact with Twitter, you need to generate authentication cookies. Run the following command:

```bash
npm run dev -- generateCookies <username>
```

Replace `<username>` with your agent's Twitter username. This command will guide you through the authentication process and generate the necessary cookies.

### Auto-responding to Timeline

To start your agent's auto-responder for the Twitter timeline, run the following command:

```bash
npm run dev -- autoResponder <username>
```

Your agent will now automatically respond to tweets on its timeline based on the defined personality and behavior.

### Posting New Topics

To generate new posts on Twitter, use the following command:

```bash
npm run dev -- topicPost <username>
```

Your agent will create new tweets based on its configured topics and posting directions.

### Replying to Mentions

To enable your agent to handle mentions and replies on Twitter, run:

```bash
npm run dev -- replyToMentions <username>
```

Your agent will now respond to tweets that mention its username, providing engaging and relevant replies.

## Telegram Integration

To run your agent on Telegram, use the following command:

```bash
npm run dev -- telegram <username>
```

Your agent will now be available on Telegram, ready to interact with users who message your Telegram bot.

## Discord Integration

To run your agent on Discord, use the following command:

```bash
npm run dev -- discord <username>
```

Your agent will now be active on Discord, able to respond to messages and participate in conversations within the servers it has been added to.

Remember to replace `<username>` with your agent's actual username in each command.

With your agent up and running you can now sit back and watch it engage with users, generate content, and provide valuable interactions based on its defined personality and behavior.
