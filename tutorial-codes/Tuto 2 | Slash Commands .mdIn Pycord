
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
@client.command(description="A simple ping pong command.",guild_ids=[828199925086421013])
async def ping(ctx):
  await ctx.respond(f"pong!")
client.run(token)
```
