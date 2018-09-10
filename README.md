# Discord Pusher

Sharing code from Visual Studio Code between people in a university study group or at work through Discord is a somewhat cumbersome task. It is not impossible, but just about annoying enough that a bot should programmed to do the work for us.

## The Manual Way:
1. Grab the selection of code that you want from Visual Studio Code
2. Switch to Discord and find the channel you want to paste to
3. Paste it into Discord
4. Sourround the code in ```, which in itself is a pain to do
5. Define the correct shorthand for the language that you need for syntax highlighting

## The Discord Pusher Way:
1. Press "Ctrl + Shift + P" to bring up the command menu in Visual Studio Code
2. Select either the "Discord: Push Current Document" or the "Discord: Push Current Selection" command
3. If a Text Channel has not been previously selected the user will be prompted to select one, otherwise, your code has been pushed with correct syntax highlighting

## Features:

- Functionality to push current document code to a Discord text channel (Discord: Push Current Document)
- Functionality to push current selected code to a Discord text channel (Discord: Push Current Selection)
- Functionality to change text channel (Discord: Select Channel)

## Requirements:

- A generic Discord bot that is logged in to your server
- The secret token of the Discord bot logged in to your server, in order to authenticate the Visual Studio Code extension

## Setting It Up The Bot:
1. First you will need a willing Discord Bot that you own. To create a bot, first you need to create an application here: https://discordapp.com/developers/applications
2. You will then need to add a bot to the application, which can be done through the **Bot** settings tab of the application you created earlier
3. Once a bot has been created, click the **"Click to Reveal Token"** link below the Bot's name. This will display a secret token that you should not share with others. You will need this to set up your Visual Studio Extension *(If for some reason you loose your token, or accidentally share it with someone, you can always generate a new one)*
4. To add the new bot to your Discord server you need to get the **Client ID** of your application, which can be found in the **General Information** settings tab of the application you created.
5. Once the client id has been found, paste it in to this link, replacing only the **CLIENTID** part with your client id: https://discordapp.com/oauth2/authorize?client_id=CLIENTID&scope=bot 

## Setting Up The Extension:
1. Install the **Discord Pusher** extension from the Visual Studio Extension Marketplace
2. Go to the settings of Visual Studio Code and overwrite the setting `discordPusher.token` to what the secret token of your bot is
3. Restart Visual Studio Code

## Extension Settings:

* `discordPusher.token`: The token needed from the Discord bot
* `discordPusher.keepAliveMinutes`: The amount of minutes that the bot will stay logged in after the latest command

## Known Issues:

There are no checks for:
- Length of documents
- Whether or not the user is in a text document

## Release Notes:

- Initial release