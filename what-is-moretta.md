# What is Moretta

Moretta is a private AI chat. You chat with the AI model of your choice and make images and
videos in the same chat. Your chat history stays in your browser. Holders of $MORETTA get free credit
for the chat every hour. The app is live at [app.moretta.ai](https://app.moretta.ai).

## The chat

In the chat, you pick a model and send a message. The app lists hundreds of models from
many providers. You can switch the model in the middle of a chat.

The app also has an Auto model. Auto picks a model for each message.

Under each answer, the app shows the cost of that answer in US dollars.

You can also attach your own images to a message and ask about them. Read
[Attach images](#attach-images).

## Images

The chat also makes images. To make an image:

1. Turn on **Image** in the chat.
2. Pick an image model and an aspect ratio: square (1:1), wide (16:9), tall (9:16), or
   classic (4:3).
3. Describe the image that you want, and send.

The image shows up in the chat. You can download the image, or make it again with another
image model.

The app lists dozens of image models, such as Nano Banana 2, Nano Banana Pro, Seedream,
GPT Image, and FLUX. The model list shows the price of one image for each image model. When
the price depends on the image, the model list shows "varies".

Your tank pays for each image. Your images stay in your browser, with your chats. Read
[Privacy](privacy.md).

## Compare mode

Compare mode sends one prompt to two to four image models at the same time. The images show
up side by side, so you can compare the image models. To compare image models:

1. Turn on **Image** in the chat, and then turn on **Compare**.
2. Pick two to four image models. The model list shows the total price of your picks.
3. Pick an aspect ratio. The app offers only the aspect ratios that all of your picks can
   make.
4. Describe the image that you want, and send.

Each image shows up when its image model is ready. Under each image, the app shows the image
model, its label, and the price of the image. The answer shows the total price. You can
download each image, or make the images again with the image models that you pick now.

Each image model charges its own price. Before you send, your tank must hold the total price
of your picks. If you stop a compare, you pay only for the images that are ready. Read
[The tank](tank.md).

Compare mode works with image models. Compare mode for chat answers is not live yet.

## Videos

The chat also makes short videos. To make a video:

1. Turn on **Video** in the chat.
2. Pick a video model, an aspect ratio, and a length from 4 to 10 seconds. The aspect
   ratios are wide (16:9), tall (9:16), and square (1:1).
3. To add sound, turn on **Sound**. Some video models make no sound, and sound costs more.
4. Describe the video that you want, and send.

A video takes about 30 seconds to a few minutes. You can keep chatting while the app makes
it. If you close the page, the video shows up when you open the chat again.

The model list shows the price of the video for each video model. Your tank pays the price
when the video starts. If the video fails, the price goes back to your tank. You cannot
stop a video after you send it.

Every video model has the label "Anonymous": the provider keeps each video for a short
time. Your videos stay in your browser, with your chats. Read [Privacy](privacy.md).

## Attach images

You can attach your own images to a prompt in the chat, in image mode, in compare mode, and
in video mode. To attach an image, use one of these ways:

- Click the paper clip in the chat, and pick an image file.
- Paste an image into the chat.
- Drop an image file on the chat.

The attached images show as small squares over your prompt. To remove an image, click the
remove button on its square.

| Mode | What the model does with your images | Images on one prompt |
|---|---|---|
| Chat | The model reads your images and answers about them. | Up to 4 |
| Image | The image model uses your images as references for the new image. | Up to 4 |
| Compare | Each image model that you pick uses your images as references. | Up to 4 |
| Video | The video starts from your image. | 1 |

Not every model can take images. Many chat models read images, but some do not. Some image
models take fewer than 4 images. If a model cannot take your images, the chat tells you why.
You can send again after you pick another model or remove some images.

Before the app sends an image, it makes the image smaller: a JPEG of at most 1,568 pixels on
its longest side. You can attach only images. Other files, such as PDFs, are not live yet.

An image can change the price. A video that starts from your image can cost more than a video
from text. When you attach an image, the model list shows the price of a video that starts from
it. Some image models charge more for an image with references than the price that the model
list shows. Read [The tank](tank.md).

Your attached images go to the model provider with your prompt. The Moretta server keeps no
copy of them. They stay in your browser, with the prompt. Read [Privacy](privacy.md).

## Features

A feature with the label `Coming soon` is not live yet. A feature with the label
`Next development` comes after that.

| Feature | What it does | Status |
|---|---|---|
| Chat | Chat with hundreds of models, in private. | Live |
| Private and Anonymous models | Each model shows what its provider can keep. Read [Privacy](privacy.md). | Live |
| Leaderboard | The 100 largest holders of $MORETTA and their tanks. Read [The tank](tank.md). | Live |
| Images | Make images in the chat with dozens of image models, paid from your tank. | Live |
| Video | Make short videos in the chat with Veo, Kling, and more, paid from your tank. | Live |
| Compare mode | Send one prompt to two to four image models, and see the images side by side. | Live |
| Attach images | Attach your own images to a prompt in every mode of the chat. | Live |
| Onchain research | An AI agent reads chain data with tools. It answers questions about a token or a wallet, checks tokens for scams and rugs, and tracks smart wallets. Read [Onchain research](onchain-research.md). | `Coming soon` |
| Compare mode for chat | Send one message to several models, and see the answers side by side. | `Coming soon` |
| Share to X | Turn an answer into a card for X. | `Coming soon` |
| Private payments | Pay for credit without a link to your identity. Read [Payments](payments.md). | `Next development` |
| Telegram bot | Use Moretta in Telegram groups. | `Next development` |

## Sign in with a Solana wallet

You sign in with a Solana wallet, such as Phantom, Solflare, or Backpack. You do not need
an email address or a password.

To sign in, the app asks your wallet to sign a short message. This signature sends no
transaction and costs nothing. The app uses it only to confirm that you own the wallet.

A sign-in lasts 7 days on that browser.

## How you pay for the chat

The chat spends credit from your tank. Your tank fills for free every hour while you
hold at least $10 of $MORETTA. For the full rules, read [The tank](tank.md).
