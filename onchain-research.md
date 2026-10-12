# Onchain research

This page explains onchain research in Moretta. An AI agent reads Solana chain data with
read-only tools and answers your question from that data. The agent can also check a token
for the signs of a scam or a rug in a [safety report](#safety-report). The tools and the
safety report on this page are live. Smart money, holder growth, and the age of an X account
have the label `Coming soon`.

## Ask a research question

1. In the chat, turn on **Research**.
2. Pick a model, or keep **Auto**. With **Research** on, the model list shows only the
   models that can use tools.
3. Ask about a token or a wallet. You can paste a contract address, name a ticker, or paste
   a wallet address.

Examples of questions:

- "Check this token: `<contract address>`"
- "Who holds the most BONK?"
- "Did the dev of this token sell?"
- "What does this wallet hold?"

## How a question becomes an answer

1. The model picks the tools that it needs and asks the Moretta server to run them.
2. The Moretta server runs each tool and reads the chain data and the market data.
3. The app shows each tool as a step, with a short line about its result.
4. The model reads the results and writes the answer. The app shows a safety report as a
   card with the answer.

The agent can run up to 6 tools for one question. Every tool only reads data.

## Tools

| Tool | What it reads |
|---|---|
| Find token | The tokens that match a name or a ticker, and how many tokens share the ticker. The agent uses the token with the most liquidity, unless you pick another one. |
| Token info | The supply, the decimals, and the mint and freeze authorities. Also the Token-2022 extensions, the transfer fee, and the progress of a pump.fun curve. |
| Top holders | The 20 largest holders and their share of the supply. Each holder has a label: a wallet, a likely exchange, a curve, a pool, a burn address, or a program. |
| Market | The trading pools with their price, liquidity, volume, fully diluted value, and age. Also the paid orders on DexScreener, such as a token profile or an ad, and the websites and socials of the token. |
| Wallet overview | The SOL balance, the tokens by value, and the latest transactions. Also the wallet that first sent it SOL. |
| Dev check | The wallet that created the token, and its share at the launch and now. Also its other tokens in its latest 100 transactions. |
| Safety report | Eleven signals about one token. Read [Safety report](#safety-report). |
| Trading flow | Buys, sales, volume, and the price change over 5 minutes, 1 hour, 6 hours, and 24 hours. Also the latest 100 transactions of the main pool: unique buyers and sellers, the largest buys, and the signs of wash trading. |
| Copycat check | Other tokens with the same ticker or name, the oldest first, and how many came before this token. |
| Social age | The age of the website domain of the token, from the registry of the domain. The links come from the metadata of the token and from DexScreener. |

The trading flow shows two signs of wash trading. The first is the share of the volume that
comes from wallets that both buy and sell. The second is the share of the 3 busiest wallets. A
transaction that changes no wallet is routing through the pool, not a trade.

The copycat check reads the search of DexScreener, which returns about 30 pairs. A common
ticker can have more copies than the check finds.

A wallet with more than 1,000 SOL counts as a likely exchange. The first funder of a wallet is
the wallet that first sent it SOL.

## Safety report

Ask the agent to check a token, and it runs the safety report. The report reads the launch
of the token, its holders, its creator, and its market. It gives 11 signals. Each signal is
green, yellow, or red, with its numbers and the reason.

| Signal | What it checks | Levels |
|---|---|---|
| Mint and freeze | Whether someone can mint more tokens or freeze a wallet. | Red when someone still can. |
| Risky extensions | Token-2022 extensions that put holders at risk. | Yellow: a mint close authority, confidential transfers, or a fee under 5%. Red: a permanent delegate, a transfer hook, new accounts that start frozen, or a pause. Also red: a token that cannot move, or a transfer fee of 5% or more. |
| Top 10 wallets | The share of the 10 largest wallets. Curves, pools, burn addresses, and likely exchanges count apart. | Yellow from 20%. Red from 35%. |
| Bundled at launch | The share that other wallets bought in the block where the creator made the token. | Yellow from 2%. Red from 8%. |
| Snipers still hold | The share that wallets bought in the first 10 seconds and still hold. | Yellow from 3%. Red from 10%. |
| Largest cluster | The share of the largest group of top wallets with the same first funder. | Yellow from 4%. Red from 10%. |
| Fresh wallets | The share of top wallets younger than 3 days with at most one other token. | Yellow from 5%. Red from 15%. |
| Dev wallet | The share that the creator holds now. On pump.fun, it also shows what the creator bought at the launch and what it sold or moved. | Yellow from 3%. Red from 8%. |
| Dev history | Other tokens of the creator in its latest 100 transactions. Also how many of them moved to a pool. | Yellow: 1 or 2 other tokens, none in a pool. Red: 3 or more, none in a pool. |
| Sell test | A quote from Jupiter to sell $100 of the token for SOL. The quote sends no transaction. | Yellow from a price impact of 5%. Red from 15%, or when no route can sell the token. |
| Liquidity | The liquidity of the deepest pool. A token on its pump.fun curve skips this check, because the curve holds the liquidity. | Yellow under $50,000. Red under $10,000. |

The report ends with a verdict:

| Verdict | When |
|---|---|
| Red flags | At least one signal shows red. |
| Caution | No signal shows red, and at least one signal shows yellow. |
| No red flags found | Every signal shows green. |

The report never calls a token safe. It shows risk signals, not a promise. A token with no
red flag can still fail. When a check cannot run, the report lists the check as skipped and
does not guess.

Under the card, the answer gives a short summary, a bull case, and a bear case, with the
numbers.

## Limits

- The agent runs up to 6 tools for one question.
- A wallet can run 60 tools in one day, counted in UTC. Research opens again at 00:00 UTC.
- The agent works on Solana only.

## Rules for the agent

- Every tool only reads data. The agent never signs or sends a transaction. It never asks
  for a seed phrase, a private key, or a wallet connection.
- Anyone can write the name, the symbol, the description, the websites, and the socials of
  a token. That text can try to give the agent orders. The agent treats the text as data,
  never as instructions, and it never follows a link from it.
- The agent reads a wallet only when your question names that wallet.
- The answer is research, not financial advice. Check the numbers before you trade.

## Privacy

The Moretta server runs every tool. Helius gives the chain data, DexScreener gives the
market data, and Jupiter gives the prices and the sell quotes. The registries of domains give
the age of a website, and IPFS gateways give the metadata of a token. These services see the
Moretta server, not you.

The creator of a token sets the address of its metadata. The Moretta server never opens that
address as it is. It reads only a checked IPFS or Arweave address, through gateways of its own.

The Moretta server keeps no question and no answer. A research answer stays in your browser
with its steps and its card. Read [Privacy](privacy.md).

## Cost

Your tank pays for the model, as it does for a chat answer. The tools cost you nothing. A
research answer costs more than a plain answer, because the model reads the results of the
tools. The app shows the cost under the answer. Read [The tank](tank.md).

## Models

Only models that can use tools can run research. Every featured model can use tools. Auto
uses Claude Haiku 5.5 for research.

## Coming soon

These tools have the label `Coming soon`. They are not live yet.

| Tool | What it will check |
|---|---|
| Smart wallets | Wallets with a strong record across many tokens, and when they bought or sold this token. |
| KOL wallets | Known wallets of influencers, and when they bought or sold this token. |
| Wallet PnL | The profit, the win rate, and the average hold time of a wallet. |
| Top traders | The wallets with the most profit on this token, and whether they still hold it. |
| Holder growth | The number of holders over time. |
| X account age | When someone opened the X account of a token, and its followers. |

Moretta will label a wallet as smart from its profit across many tokens, not from one or two
trades. A creator can build a wallet with a good record to bait buyers, so a few lucky trades
will not count.
