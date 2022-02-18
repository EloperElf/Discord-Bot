# Discord-Bot
import discord

class MyClient(discord.Client):
    async def on_ready(self):
        print('Logged on as', self.user)

    async def on_message(self, message):
        # don't respond to ourselves
        if message.author == self.user:
            return

        if message.content == 'ping':
            await message.channel.send('pong')

client = MyClient()
client.run('token')
[discord.py-1.7.3.tar.gz](https://github.com/EloperElf/Discord-Bot/files/8098094/discord.py-1.7.3.tar.gz)
