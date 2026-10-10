# Privacy

Moretta is a private AI chat. This page explains where your chat history lives, what the
Moretta server keeps, and what each model provider can see.

## Your chat history stays in your browser

The app saves your chats in the storage of your browser, on your device. The Moretta
server does not keep a copy of your chats.

If you clear the storage of your browser, your chats are gone. A chat that you start on
one device does not show on another device.

## The Moretta server keeps no prompts

When you send a message, the Moretta server passes it to the model provider and passes
the answer back to you. The server does not store your messages or the answers.

The server keeps only what the tank needs:

- Your wallet address and your sign-in session.
- The $MORETTA balance of each wallet.
- The credit in each tank.
- The total that the app spends each day.

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

## The leaderboard

The leaderboard shows the tanks of the 100 largest holders, so it shows how much credit a
large holder has left. Any wallet can hide itself from the leaderboard in the app. Read
[The tank](tank.md).

## Private payments `Next development`

Moretta plans payments that link no payment to your identity: private top-ups on
Starknet and anonymous vouchers for the chat. Read [Payments](payments.md).
