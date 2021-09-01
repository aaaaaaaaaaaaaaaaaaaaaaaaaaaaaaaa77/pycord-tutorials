Tutorial 1 | [install pycord in replit](https://www.youtube.com/watch?v=YZ-ePaaazUI)

```
import discord
import os
client = discord.Client()
token = os.environ.get('token')

@client.event
async def on_ready():
    print('Logged in as {0.user} using Pycord!'.format(client))

@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('!ping'):
        await message.channel.send('pong!')

client.run(token)
```
