## What is HTTP INTERACTION discord bot?
- An Interaction Discord Bot writing using new **HTTP API**
- Although the bot is offlined, it still can be continue working properly.
- Only can use application commands, X no message content command
- There's no any status (`online`, `offline`, `idle`, `dnd`, `streaming`) to this type of bot.

<img class="httpImg" src="https://cdn.discordapp.com/attachments/958979886528221244/969958354409627718/unknown.png" alt="httpInteractionDCbot">

## This project is referred from:
- [Slash Command Discord Bot (fastify)](https://ianmitchell.dev/blog/creating-a-discord-http-slash-command-bot-with-fastify)
- [Offical Github Discord API](https://github.com/discord/discord-example-app)

## Required Packages:
-   [x] [fastify](https://www.npmjs.com/package/fastify)
-   [x] [ngrok](https://www.npmjs.com/package/ngrok)
-   [x] [node-fetch](https://www.npmjs.com/package/node-fetch)
-   [x] [fastify-raw-body](https://www.npmjs.com/package/fastify-raw-body)
-   [x] [discord-interactions](https://www.npmjs.com/package/discord-interactions)


# Set up interactivity
- The project needs a public endpoint where Discord can send requests. To develop and test locally, you can use something like ngrok to tunnel HTTP traffic.

- Install ngrok if you haven't already (```npm i ngrok```), then start listening on port 3000:

```
ngrok http 3000
```
You should see your connection open:

```
Tunnel Status                 online
Version                       2.0/2.0
Web Interface                 http://127.0.0.1:4040
Forwarding                    http://1234-someurl.ngrok.io -> localhost:3000
Forwarding                    https://1234-someurl.ngrok.io -> localhost:3000

Connections                  ttl     opn     rt1     rt5     p50     p90
                              0       0       0.00    0.00    0.00    0.00
```
Copy the forwarding address that starts with https, in this case https://1234-someurl.ngrok.io, then go to your [app's settings](https://discord.com/developers/applications) and paste it to the **Interactions Endpoint URL** option.

<img class="httpImg" src="https://cdn.discordapp.com/attachments/958979886528221244/969957873004204073/unknown.png" alt="INTERACTIONS ENDPOINT URL">

## How to run?
- Type this in your terminal and enter it:
```
npm run register
```
and then you are all set!

- do ```npm start``` for start booting the server.

# ⚠️ Note
- Remember don't close the `ngrok http 3000` terminal & ```npm start``` terminal, or else the commands in the bot will not be working
