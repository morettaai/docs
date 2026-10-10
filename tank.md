# The tank

The tank is the free credit of a holder. It fills every hour while you hold $MORETTA,
and the chat spends it. This page explains the rules of the tank.

## The rules in short

| Rule | Value |
|---|---|
| The line: the minimum holding for a tank to fill | $10 of $MORETTA |
| Fill | $1 of credit every hour |
| Cap | $24 of credit |
| First fill | After you hold through one full hour |

Tanks started to fill on 10 Oct 2026, when the app went live. For now, tanks fill every 30
minutes instead of every hour, so early holders fill up faster.

## How a tank fills

The app checks every holder at the end of each hour. Your tank gets $1 of credit for
that hour if your balance stayed at or above the line through the whole hour.

The app uses your lowest balance during the hour. A buy just before the end of an hour
does not fill your tank for that hour. A sale that takes your balance below the line
during an hour stops the fill for that hour.

A full tank holds $24 of credit. A full tank does not fill more until the chat spends
some of its credit.

If the Moretta server is down during an hour, no tank fills for that hour.

## The leaderboard

The leaderboard at [moretta.ai/leaderboard](https://moretta.ai/leaderboard) shows the 100
largest holders of $MORETTA, ranked by tokens held, with their tanks. Program accounts,
such as the pump.fun curve, show apart and take no rank.

To keep your wallet off the leaderboard, connect it at
[app.moretta.ai/leaderboard](https://app.moretta.ai/leaderboard) and choose "Hide my
wallet".

## How the app values your holding

The app values your $MORETTA at the median price of the last 24 hours. A short spike or
a short drop in the price does not change your tank.

After your tank starts to fill, it keeps filling until your holding falls below $9. This
margin of 10% keeps small price moves from stopping your tank.

## How the chat spends credit

Each answer costs the price that the model provider charges for it. The chat takes that
cost from your tank, and the app shows the cost under the answer.

If you stop an answer before it ends, the app charges an estimate of its cost.

An image costs the price that the provider of the image model charges for it. Before you
send, your tank must hold at least the price of one image. If you stop an image before it
is ready, the image costs nothing.

A video costs its price per second times its length. Your tank must hold that price, and
it pays the price when the video starts. If the video fails, the price goes back to your
tank. You cannot stop a video after you send it. You can make one video at a time, and
you can chat while the app makes it.

You can send one message at a time. Your tank can fall below zero by the cost of one
answer. The next fills cover it.

## The daily limit

The app has a daily spending limit for all users together. When the app reaches it, the
chat pauses until the next day, counted in UTC. This limit keeps free credit available for
every holder.

## A daily limit that follows the fees `Coming soon`

Moretta plans to set the daily limit from the trading fees of $MORETTA. As trading grows,
the free credit for holders can grow with it.

## Holder discount `Coming soon`

Holders pay less for each answer. Moretta announces the size of the discount before the
discount goes live.

## Credit is not money

Credit pays only for the chat in the Moretta app. You cannot sell credit, send it to
another wallet, or exchange it for $MORETTA.
