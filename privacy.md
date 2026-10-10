# Privacy

Moretta is a private AI chat. This page explains where your chat history lives, what the
Moretta server keeps, and what each model provider can see.

## Your chat history stays in your browser

The app saves your chats, your images, and your videos in the storage of your browser, on
your device. The Moretta server does not keep a copy of your chats, images, or videos.

If you clear the storage of your browser, your chats, images, and videos are gone. A chat
that you start on one device does not show on another device.

## The Moretta server keeps no prompts

When you send a message, the Moretta server passes it to the model provider and passes
the answer back to you. The server does not store your messages or the answers. An image
takes the same path, and the server keeps no copy of it.

A video takes longer. While the provider makes a video, the server keeps your wallet, the
job id of the video, and its price, so that it can give the video to your browser and
settle the price. The server deletes this record when your browser has the video, and
after 24 hours at the latest. The server never keeps the prompt or the video.

The server keeps only what the tank needs:

- Your wallet address and your sign-in session.
- The $MORETTA balance of each wallet.
- The credit in each tank.
- The total that the app spends each day.
- The price of the last image of each image model, with no wallet and no message.
- While a video is made: your wallet, the job id of the video, and its price.

The server does not ask for your name, your email address, or a password.

## Model providers do not see your wallet

The app sends each message to the model provider under the Moretta account, not under
your wallet. A model provider never learns which wallet sent a message.

## Private models and anonymous models

Each model in the app has one label. The label tells you what the model provider can
keep.

| Label | What the model provider keeps |
|---|---|
| Private | Nothing. The provider keeps no data from the message. |
| Anonymous | The provider can keep the message, but it does not know who sent it. |

For the most private chat, choose a model with the label "Private". The model list has a
filter that shows only private models.

Every video model has the label "Anonymous". The provider keeps each video for a short
time, until the app gets it.

## The leaderboard

The leaderboard shows the tanks of the 100 largest holders, so it shows how much credit a
large holder has left. Any wallet can hide itself from the leaderboard in the app. Read
[The tank](tank.md).

## Private payments `Next development`

Moretta plans payments that link no payment to your identity: private top-ups on
Starknet and anonymous vouchers for the chat. Read [Payments](payments.md).
