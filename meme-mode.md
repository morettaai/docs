# Meme mode

Meme mode makes a short video of the meme of a Solana token. You paste the contract address
of a meme coin, and the app makes a new video of its meme, with the ticker and the contract
address at the end. Holders of $MORETTA pay for it with the free credit of their tank.

## Make a meme video

To make a meme video:

1. Turn on **Meme** in the chat.
2. Paste the contract address of the token.
3. Optional: add an idea after the contract address, such as "surfing a giant wave".
4. Pick a video model, an aspect ratio, and a length.
5. Optional: turn on **Sound**. Some video models make no sound, and sound costs more.
6. Send.

The chat shows each step: "Reading the token", "Writing the scene", "Drawing the first
frame", and "Making the video". The first frame shows while the video model works. A meme
video takes about one minute to a few minutes. You can keep chatting while the app makes it.

When the meme video is ready, you can download it. With the meme video, the chat shows the
ticker, the style, the place, and the camera move of the scene.

The app reads the first Solana address in your prompt. The rest of the prompt is your idea,
up to 300 characters. You cannot attach images in Meme mode: the meme video starts from the
image of the token.

## What a meme video shows

A meme video shows the character of the token in a new scene. The character comes from the
image of the token, so it keeps its look.

After the video model makes the video, the Moretta server adds two things:

- The Moretta mark, small, in the lower right corner.
- An end card of 2 seconds: the mark, the ticker, the contract address, and `moretta.ai`.

The video models make no text, so the app writes the ticker and the contract address itself.
The end card adds 2 seconds to the length that you pick. If the server cannot add the mark and
the end card, you get the video without them.

## Each meme video is new

Meme mode makes a new scene for each meme video, so two meme videos of one token differ. The
scene comes from three layers:

| Layer | What Meme mode reads |
|---|---|
| The lore of the token | The name, the ticker, the description, and the image. The title and the description of up to 2 websites of the token. |
| The mood of the chart | The price change of the token in 24 hours. A rise of 20% or more gives a victory. A fall of 20% or more gives a comeback. Anything between gives a confident scene. |
| A new recipe | A style, a place, an action, and a camera move, drawn again for each meme video. |

Meme mode has 10 styles: Trailer, Anime, Documentary, Music video, Claymation, Pixel art,
Film noir, 90s camcorder, 3D cartoon, and Sports replay. The scene model picks a style that
fits the character of the token.

Your browser keeps the recipes of the last 6 meme videos of each token. It sends them with
the next request, so the next meme video gets another style, place, and camera move. The
Moretta server keeps no recipe.

## Real people

Meme mode makes no videos of real people. Meme mode turns down a token when its image shows a
real person that someone can identify: a celebrity, a politician, an influencer, or a photo of
a private person.

Meme mode accepts a realistic, made-up character. The description or the websites of the token
must present the character as made-up or made with AI. Meme mode turns down a known public
figure, whatever the token says.

When Meme mode turns down a token, the chat says: "Meme mode makes no videos of real people.
Try a token with a cartoon, an animal, or a made-up character." Your tank pays only for the
scene, about $0.002.

## When Meme mode stops

Meme mode can stop at each step. This table shows what the chat says and what your tank pays.

| Case | What the chat says | What your tank pays |
|---|---|---|
| The prompt has no contract address | A note asks for a contract address, and you cannot send. | Nothing |
| The address is a wallet, not a token | "This address is not a token." | Nothing |
| The token has no image | "This token has no image to make a meme from." | Nothing |
| The image shows a real person | "Meme mode makes no videos of real people." | The scene, about $0.002 |
| The image model turns the token down | "The image model turned this token down. Try another token." | The scene, about $0.002 |
| The video fails | "The model did not make the video. Its price is back in your tank." | The scene and the first frame, about $0.07 |

## Video models

Meme mode uses the video models that can start a video from an image. Meme mode leaves out
Veo, because Veo turns down realistic faces. For each video model, the model list shows the
price of a meme video: the video, the first frame, and $0.01 for the scene.

The aspect ratios and the lengths come from the video model that you pick. Meme mode starts
with tall (9:16), because X and phones show tall videos large. If your video model cannot make
meme videos, Meme mode starts with Grok Imagine Video 1.5 Lite.

## The price of a meme video

A meme video has three parts, and your tank pays for each part:

| Part | Model | Price |
|---|---|---|
| The scene | Gemini 3.8 Flash | About $0.002 |
| The first frame | Nano Banana 2 | About $0.067 |
| The video | The video model that you pick | The price of a video that starts from an image |

Before you send, your tank must hold the price of the video, the price of the first frame, and
$0.01 for the scene. Your tank pays for the scene and the first frame when each one is ready.
Your tank pays for the video when the video starts. If the video fails, the price of the video
goes back to your tank.

For example, on 13 Oct 2026 a meme video of 4 seconds with Grok Imagine Video 1.5 Lite cost
about $0.20: $0.13 for the video, and about $0.07 for the scene and the first frame.

You can make one meme video or one video at a time. The daily limit of the app applies. Read
[The tank](tank.md).

## Privacy in Meme mode

Meme mode reads only public data about the token. The Moretta server reads it, so the services
see the Moretta server, not you:

- The token and its market: Helius, DexScreener, and the IPFS and Arweave gateways of the
  metadata of the token.
- Up to 2 websites of the token: the server reads only the title and the description of each
  page, over HTTPS. It skips links to X, Telegram, and Discord. It sends nothing about you.

The models get the token, never your wallet. The scene model gets the image, the name, the
ticker, the description, the text of the websites, the mood, your idea, and your recent
recipes. The image model gets the image of the token and the scene. The video model gets the
first frame and the scene.

Every video model has the label "Anonymous": the provider keeps each video for a short time.
While the provider makes the video, the server keeps your wallet, the job id, and the price,
as for any video. The server keeps no token, no idea, and no recipe. It adds the mark and the
end card in a temporary folder.

Your meme videos, their first frames, and their recipes stay in your browser, with your chats.
Read [Privacy](privacy.md).

## Limits

| Limit | Value |
|---|---|
| Your idea | Up to 300 characters |
| Recipes that your browser sends | The last 6 meme videos of the token |
| Websites of a token that the server reads | Up to 2 |
| Meme videos or videos at a time | 1 for each wallet |
| End card | 2 seconds, after the video |
