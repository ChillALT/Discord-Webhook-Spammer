# Discord-Webhook-Spammer

![alt text](https://i.imgur.com/HJyvi3L.png) ![alt text](https://i.imgur.com/bzrjWH9.png)



Discord webhook spammer that spams a webhook as much as you want

 
coded by ChillALT
[source code pastebin](https://pastebin.com/JgXJ4aEm)

```python 
import discord_webhook
from discord_webhook import DiscordEmbed, DiscordWebhook
import string
import random
import time
import requests
import colorama
import json
from colorama import *

colorama.init()

def sbammah():
    webhook = input(Fore.GREEN + "[>] Enter The Webhook Link: ")
    message = input(Fore.GREEN + "[>] Enter The Message: ")
    messagedeley = float(input(Fore.RED + "[>] Enter The Delay of the spam: "))
    print(Fore.RESET + '')

    while True:

        print(Fore.CYAN + "Sending -> " + message)
        print(Fore.RESET + " ")
        try:
            time.sleep(messagedeley)
            _data = requests.post(webhook, json={'content': message})

            if _data.status_code == 204:
                print(Fore.CYAN + "Sent -> " + message) 
        except:
            print("Something Happend! | check if the webhook is working -> " + webhook)
            time.sleep(5)
            exit()

x = 5
while x == 5:
    sbammah()
    ```
 
