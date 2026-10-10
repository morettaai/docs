# Onchain research

This page explains onchain research in Moretta: an AI agent that reads chain data with
tools and answers your question from that data. The agent also checks a token for the
signs of a scam or a rug, and shows where smart wallets buy. Onchain research has the label
`Coming soon`: it is not live yet.

## What the agent does

You ask a question about a token, a wallet, or a transaction, such as "Who holds most of
this token?" or "Did the dev sell?". The agent decides which tools it needs, runs them,
reads the results, and writes an answer from the data. The answer shows the numbers that
it uses, so you can check them.

Ask "Check this token", and the agent writes a [safety report](#safety-report).

The agent works on Solana first.

## How a question becomes an answer

1. You ask a question in the chat and choose a model that can use tools, or Auto.
2. The model picks one or more tools and asks the Moretta server to run them.
3. The Moretta server runs each tool and reads the chain data. Every tool only reads data.
4. The model reads the results and writes the answer, with a short card of the key
   numbers.

The agent can run up to 6 tools for one question.

## Tools

The tools come in four groups: basics, scam and rug checks, smart money, and flow.

### Basics

| Tool | What it reads |
|---|---|
| Token info | The supply, the decimals, the mint authority and the freeze authority, the Token-2022 extensions (such as a transfer fee), and the name and the symbol. |
| Top holders | The largest holders of a token, their share of the supply, and labels for known wallets, such as a launchpad curve or a burn address. |
| Market | The price, the liquidity, the trading volume, the fully diluted value, and the age of the pool. |
| Wallet overview | The SOL balance, the tokens that a wallet holds, and its latest transactions. |
| Dev check | The wallet that created a pump.fun token, and how much of the token that wallet sold. |

### Scam and rug checks

On pump.fun, the creator cannot pull the liquidity of the curve. A rug there usually comes
from insiders who hold a large share in secret and then sell it. These checks look for
those insiders and for traps in the token itself.

| Tool | What it checks |
|---|---|
| Bundle check | Wallets that bought in the same block as the creation of the token. A creator can buy with many wallets at once to hide a large share. |
| Snipers | Wallets that bought in the first seconds, and the share that they still hold. |
| Clusters | Large holders that got their funds from the same wallet. One person behind many holders shows as one cluster. |
| Fresh wallets | The share of the supply in new wallets that hold only this token. |
| Dev history | The other tokens from the creator wallet: how many moved from the curve to a trading pool, and how many died. |
| Sell test | A simulated sale: whether a holder can sell, and the real cost of the sale. |
| Risky extensions | Token-2022 extensions that put holders at risk. A permanent delegate can take tokens from any wallet, and a transfer hook can block sales. |
| Copycat check | Other tokens with the same name or ticker, and which one came first. |
| Socials | The age of the X account, the age of the website domain, and whether the token has a paid profile on market sites. |

### Smart money

| Tool | What it checks |
|---|---|
| Smart wallets | Wallets with a strong record across many tokens, and when they bought or sold this token. |
| KOL wallets | Known wallets of influencers, and when they bought or sold this token. |
| Wallet PnL | The profit, the win rate, and the average hold time of a wallet. |
| Top traders | The wallets with the most profit on this token, and whether they still hold it. |

Moretta labels a wallet as smart from its profit across many tokens, not from one or two
trades. A creator can build a wallet with a good record to bait buyers, so a few lucky
trades do not count.

### Flow

| Tool | What it checks |
|---|---|
| Buy and sell flow | Buys against sales over 5 minutes, 1 hour, and 24 hours, the number of unique buyers, and large buys. |
| Wash trading | The volume against the number of unique traders, and wallets that buy and sell back and forth. |
| Holder growth | The number of holders over time. |
| Curve progress | How far a pump.fun token is along its curve toward a trading pool. |

## Safety report

The safety report is one tool that runs the scam and rug checks together. It shows each
signal as green, yellow, or red, with the reason. It ends with the bull case and the bear
case for the token.

The report shows risk signals, not a promise. A token with no red signal can still fail,
so the report never calls a token safe.

## Rules for the agent

- Every tool only reads data. The agent never signs a transaction and never asks for your
  wallet.
- Token names and token descriptions can contain text that tries to give the agent
  orders. The agent treats chain data as data, never as instructions.
- The answer is research, not financial advice. Check the numbers before you trade.

## Privacy

The Moretta server sends the tool requests to the chain and to market data providers. The
providers see the Moretta server, not you. The agent reads a wallet only when your question
names that wallet.

## Cost

A question with tools costs more than a plain answer, because the model reads the tool
results. The chat takes the full cost from your tank, and the app shows the cost under the
answer. Read [The tank](tank.md).

## Models

Only models that can use tools can run the agent. In the model list, these models carry a
tools label. Auto picks such a model for a research question.
