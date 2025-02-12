Discord Set Up For Normies. A Simple Guide to Setting up your Agent on Discord.

1. Go to https://discord.com/developers/
2. Login or create a developer account if you've not done so.
3. Click on applications at the top right corner.
![Screenshot 2025-02-12 at 03 35 59](https://github.com/user-attachments/assets/2e07b037-21d1-4c65-9b9e-f862a778fbc1)

4. Create an application by assigning a username to your bot. It's best to use the same name for both your application and agent. Accept the terms and conditions, then proceed to create your bot.
![Screenshot 2025-02-12 at 03 39 42](https://github.com/user-attachments/assets/d3df3135-1e19-4a01-bafe-4fe7bd9d64d8)

5. After creating the bot, you'll be directed to the general information page, which includes the description and logo.
Note: Click on Copy Application ID and save it in your notes—this will be useful during the character setup step in docs/installation/configuration.md
Leave the Endpoint URL, Application URL, Service URL, and Policy URL fields blank, as they are not needed.
![Screenshot 2025-02-12 at 03 53 00](https://github.com/user-attachments/assets/4db82a47-2163-4c31-b6fa-2c2d9dd3245b)

6. In the left menu, click on Installation. This step focuses on how your bot will be installed on your Discord server.
Note: We’re primarily interested in the Guild Install option, so you can toggle off the User Install option.
Ensure the Install Link is set to the default Discord-provided link.
![Screenshot 2025-02-12 at 04 03 39](https://github.com/user-attachments/assets/99d6c981-ce8e-4c4c-a529-75f818bf9885)

7. In the default install settings, toggle the Application Command options and select Bot. This defines the actions your bot can perform in the guild or community server.
Note: It’s best to grant minimal permissions. The essential commands are Read Message History and Send Messages. Depending on your agent's lore and functionality, you may choose to add other permissions, such as Use External Stickers, Embed Links, and Add Reactions.
![Screenshot 2025-02-12 at 04 11 52](https://github.com/user-attachments/assets/52deb087-c9f0-48a2-8947-9dc152f96df2)

8. After saving the changes, copy the Install Link provided and paste it into a new browser tab.
You'll be prompted to add the bot to your Discord server.
![Screenshot 2025-02-12 at 04 25 46](https://github.com/user-attachments/assets/390a78d2-85ce-48c8-a642-08524a13d16e)

9. In the left menu, click on Bot. This section provides additional details about your bot.
Adding a banner is optional, so you can choose to skip it if you prefer.
Click on Reset Token to generate a new token for your bot. Copy and securely save this token in your notes or another safe place.
This token will be needed for your agent configuration and will serve as your Discord API key 
![Screenshot 2025-02-12 at 04 25 46](https://github.com/user-attachments/assets/53ecfff0-bf62-44cb-be8a-6d1a3b0911f8)

10. The only Privilege Gateway Intent setting you'll need is Message Content Intent.
Toggle this on to allow your bot to respond to messages on your server.
![Screenshot 2025-02-12 at 04 33 37](https://github.com/user-attachments/assets/cf1786bc-49f4-48d5-a304-734be5bb61b7)

11. One final step, and it’s crucial:
Your Discord bot will need Administrator permissions to function properly while running your agent.
This allows the bot to respond to tags and messages and operate as a moderator in the server.
![Screenshot 2025-02-12 at 04 43 37](https://github.com/user-attachments/assets/34fcba33-9d3f-4e29-ad33-5158627295d8)

12. You’ve completed the Discord bot setup! Now, follow the instructions to run your agent and complete the setup. Check docs/installation/running-agent.md
