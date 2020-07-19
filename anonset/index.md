# Anonymity Sets in Zcash Protocol Cryptocoins

## TLDR

 * Most coins, including ZEC and Pirate cannot even correctly define anonymity set!
 * We exactly define anonymity sets (anonsets), AKA "shielded pools"
 * Hush is currently the only cryptocoin that can calculate anonset in real-time

## Definition

The anonymity set is a set! Josh Swihart of Zcash Company does not seem to understand
the difference between a daily count of transactions and the current set of privacy.
They are completely different, yet he talks as if they are the same. All graphics
from Swihart + ZEC related to transaction counts and *NOT* anonymity sets.

They do not understand that the anonset can change with every block, and go up and down.
They show graphs of counts monotonically going up, attempting to lie (badly) with statistics.
Additionally, Zcash Company is running test scripts behind the scenes to massage their
incorrectly-defined data.

The *size* of the anonset is a count, and we can measure it at every block with a very simple
equation:


```
    size(anonset) = outputs - spends
```

At every block, the Hush full node keeps track of all shielded spends and outputs, so it can
calculate the size of the anonset at any block height. To our knowledge, Hush is the first
cryptocoin to every have this ability.

## Hush details

When the `-zindex` CLI argument is enabled, the Shielded Index keeps tracks of many
statistics, two of which are `shielded_spends` and `shielded_outputs`. This data can
be retrieved via:

```
    hush-cli getchaintxstats
```

## Current Stats

As of Hush Block Height 263573 on 19th July 2020:

  * Anonset Size     = 93559
  * Shielded Spends  = 38954
  * Shielded Outputs = 132513

What this means, is that every time you do a shielded Hush transaction, it's "hiding"
in the "anonymity set" of about 100,000 others, which gives us privacy. The larger the
anonset, the more privacy. If our anonset was just a small number, most privacy properties
are lost.

## Comparing to Monero/CryptoNote coins

The way privacy works in Monero/CryptoNote coins is different and the way anonymity set
is defined is different. With Monero, about 10 or so "mixins" are added to each transaction,
so that it's unclear exactly which funds are being spent. So the anonymity set of every Monero
transaction is a different small set of about 10, which constantly changes.

The author believes that Zcash Protocol anonymity sets are stronger, but concedes that Monero
has a much stronger dedication to privacy than Zcash and has better GUI wallets with great UI/UX.

For these reasons, Hush considers Monero to be it's main competition, as Zcash mainnet is now
supported by Chainanlysis and Ciphertrace.


## Questions

  * Why doesn't Zcash provide these stats in real-time?

The author proposes they realize it would be too depressing to see how small their anonset is, after four years.
This is why Josh Swihart lies with statistics and tells investors whatever they want to hear.

  * Is Josh Swihart commiting financial fraud by knowingly misrepresenting ZEC mainnet statistics?

The author believes Swihart is mostly ignorant of how the internals work but also is dancing on the line of
outright fraudulent numbers about Zcash mainnet. This report hopes to clarify these misunderstandings.

