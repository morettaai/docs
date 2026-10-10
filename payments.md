# Payments

This page explains how you pay for credit in Moretta. When the app opens, holders of
$MORETTA get free credit from the tank. In the next development, anyone can buy credit with a private
payment.

A section with the label `Next development` describes a feature that is not live yet.

## Free credit for holders

Hold at least $10 of $MORETTA, and your tank fills with $1 of credit every hour, up to
$24. The chat spends this credit. For the full rules, read [The tank](tank.md).

## Private top-ups on Starknet `Next development`

A private top-up buys credit with private USDC on Starknet. Starknet's privacy pool for
tokens (STRK20) hides the amount and both wallets from outside view. OpenZeppelin audited
the contracts of the pool in May 2026.

To top up, you send the exact amount that the app shows to the Moretta wallet on Starknet.
Each top-up has its own amount, so the app can match your payment without a name or an
email address.

Moretta does not keep the address that a payment came from after it matches the payment.

## Anonymous vouchers `Next development`

A top-up gives you a voucher: a secret code that holds credit. You chat with the voucher,
without a wallet sign-in. Nothing links your chats to the wallet that paid.

Keep the voucher code safe. Anyone with the code can spend its credit.

## Pay with SOL or USDC from Solana `Next development`

An automatic bridge takes SOL or USDC from Solana to the Moretta wallet on Starknet for
you. This path is quick, but the payment is visible on Solana and on the bridge. The
voucher and your chats stay unlinked to your wallet.

For a payment that nobody can see, pay with private USDC on Starknet.

## Pay with ZEC `Next development`

A planned path takes ZEC from Zcash to Starknet, for a private payment from end to end.

## Private billing `Next development`

With private billing, you pay for each chat session with a zero-knowledge proof. Nobody
can link one session to another, or to a wallet.

## What stays the same

- Credit pays only for the chat in the Moretta app. You cannot sell credit or exchange it
  for $MORETTA.
- Moretta never asks for your seed phrase or your private key.
