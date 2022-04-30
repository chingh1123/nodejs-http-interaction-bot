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
