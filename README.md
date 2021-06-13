[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
# Discord.py-MaxEmbeds
An EmbedBuilder for Discord bots in Python. You need discord.py to use this module.

## Installation
### Step 1

First you have to install the `requirements.txt`, you do this by running this command in your folder where `MaxEmbeds.py` is:
```
pip install -r requirements.txt
```
### Step 2
Now you have to install the Python module `maxembeds`, if you don't want to do this, you can also drag the file `MaxEmbeds.py` into your folder where your bot is programmed.
```
pip install maxembeds
```

## Usage
There are the following parameters you can use to build your embed:
- title
- description
- color
- thumbnail
- author
- footer
- fields

Here would be an example to build and send an embed with all parameters:
```py
import discord
from MaxEmbdes import EmbedBuilder

client = discord.Client()

@client.event
async def on_message(message):
  if not message.author.bot:
    if message.content.starswith("MaxEmbeds")
      embed = EmbedBuilder (
        title = "MaxEmbeds - EmbedBuilder",
        description = "Test description",
        color = discord.Color.dark_gold(),
        fields = [["Field 1", "Test field", True], ["Field 2", "Test field", True]],
        footer = ["Test footer", message.author.avatar_url],
        author = [message.author.name, message.author.avatar_url],
        thumbnail = message.author.avatar_url
      ).build()

      await message.channel.send(embed=embed)
```

**Tip:** A field always consists of three parts: the name, the value and the inline information. So `field[0]` is the name, `field[1]` the value and `field[2]` the inline specification.

## Links
PyPi-Profile: https://pypi.org/user/MaxiPy/ <br>
PyPi-Project: https://pypi.org/project/maxembeds/ <br>
Support-Discord: https://discord.fastcord.de/ <br>

[![Discord](https://img.shields.io/discord/839563450752958484.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/N2ejzCEeXv) [![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/IncredibleDesign/Discord.py-MaxEmbeds/blob/main/LICENSE)
