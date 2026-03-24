# I want to add a command to my Discord bot that sends a direct message to a user

_Implement a command to send a direct message to a user_

## Steps

1. Define the command function with the `@bot.slash_command()` decorator, for example `@bot.slash_command(name='dm_user', description='Send a direct message to a user')`
2. Get the user object from the command context, for example `user = ctx.author`
3. Use the `user.send()` method to send a direct message to the user, for example `await user.send('Hello, this is a direct message')`
4. Handle the case where the user has direct messages disabled, for example `try: await user.send('Hello, this is a direct message') except discord.Forbidden: await ctx.send('The user has direct messages disabled')`
5. Test the command by sending a direct message to a user and checking that it is received correctly
6. Consider adding a check to ensure the bot has the `members` intent enabled to access the user object

## Pitfalls

- Not handling the case where the user has direct messages disabled
- Not checking for the required intents to access the user object