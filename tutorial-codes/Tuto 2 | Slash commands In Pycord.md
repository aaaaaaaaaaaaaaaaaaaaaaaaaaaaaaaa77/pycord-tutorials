Tutorial 2 | [Slash commands in Pycord](https://youtu.be/)
```py
import discord
from discord.ext import commands 
import os
client = discord.Bot()
token = os.environ.get('token')

@client.event
async def on_ready():
    print('Logged in as {0.user} using Pycord!'.format(client))

@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('ping'):
        await message.channel.send('pong!')

@client.slash_command(description="A simple ping pong command.")
async def ping(ctx):
  if ctx.guild.id == GUILD ID:
    await ctx.send(f"pong!")
client.run(token)

```
