# I want to create a basic Discord bot that responds to a specific command, but I'm not sure where to start

_Create a bot with discord.py and handle a custom command_

## Steps

1. Install the discord.py library by running `pip install discord.py` in your terminal
2. Create a new Discord bot on the Discord Developer Portal and obtain the bot token
3. Create a new Python file for your bot and import the discord.py library with `import discord`
4. Create a new instance of the Bot class with `intents = discord.Intents.default()` and `bot = discord.Bot(intents=intents)`
5. Define a custom command using the `@bot.slash_command()` decorator, for example `@bot.slash_command(name='hello', description='Say hello')`
6. Add an event listener for the `on_ready` event to print a message when the bot is ready with `@bot.event` and `async def on_ready(): print('Bot is ready')`

## Pitfalls

- Forgetting to invite the bot to your server with the correct permissions
- Not handling errors and exceptions properly