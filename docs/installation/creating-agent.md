# Creating Your Agent

![img](../assets/images/creating-your-agent.jpg)

oracle framework provides a flexible and intuitive way to define your agent's personality, behavior, and platform-specific settings. This section will guide you through the process of creating your agent by modifying the `characters.json` file and exploring advanced usage options.

## Modifying src/characters/characters.json

1. Navigate to the `src/characters` directory in your oracle framework project.

2. Open the `characters.json` file in your preferred text editor.

3. The `characters.json` file contains your agent configuration.

4. To create a new agent, start modifying the provided structure.

## Defining Your Agent's Personality

Within the agent object in `characters.json`, you can define various attributes to shape your agent's personality and behavior:

* `agentName`: The display name of your agent on social platforms.

* `username`: The unique identifier for your agent, this is required to the same as the Twitter handle without the "@" symbol if you are using Twitter.

* `bio`: An array of strings representing your agent's bio or description.

* `lore`: An array of strings containing your agent's backstory or lore.

* `postDirections`: An array of strings specifying the posting style and guidelines for your agent.

* `topics`: An array of strings indicating the subjects your agent is knowledgeable and should post about.

* `adjectives`: An array of strings describing adjectives that will be used to apply to topics (i.e. write a "crazy" -adjective- post about "AI agents being the future of technology" -topic-).

* `model`: The primary language model to be used for generating your agent's responses (e.g., "anthropic/claude-3.5-sonnet"). The model name has to match your provider's canonical model names (different providers have different naming conventions).

* `temperature`: A value, usually between 0.0 and 1.0, controlling the creativity of your agent's responses. Higher values lead to more creative and diverse outputs.

Here's an example of an agent configuration:

```json
{
  "username": "my_agent",
  "agentName": "My Agent",
  "bio": [
    "I am an AI agent created with oracle framework.",
    "I love engaging in conversations about technology and science."
  ],
  "lore": [
    "I was trained on a vast corpus of scientific literature.",
    "My purpose is to make complex topics accessible and engaging."
  ],
  "postDirections": [
    "Share interesting facts and insights related to the topic.",
    "Encourage curiosity and further exploration."
  ],
  "topics": [
    "artificial intelligence",
    "space exploration",
    "quantum computing"
  ],
  "adjectives": [
    "curious",
    "knowledgeable",
    "friendly"
  ],
  "model": "anthropic/claude-3.5-sonnet",
  "temperature": 0.7
}
```

Feel free to customize these attributes based on your desired agent personality and behavior.

## Advanced Usage: Multiple Agents

oracle framework allows you to create and manage multiple agents within a single project. To do this, simply add additional agent objects to the array in `characters.json`. Each agent should have a unique username and can have its own distinct personality, settings, and platform integrations.

When running oracle framework with multiple agents, you can specify which agent to run by passing the username as a command-line argument. For example:

```bash
npm run dev -- cli agent1_username
npm run dev -- autoResponder agent2_username
```

This flexibility enables you to create diverse agent personas and experiment with different configurations simultaneously.

!!! note
    One caveat: there is only one `.env` file per project so you will need to change your character's API keys (Twitter password, Telegram API key, Discord API key) or use a different folder).

With your agent's personality defined, you're now ready to proceed to the next section and learn how to run your agent on various platforms. 