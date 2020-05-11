# Zcash Protocol Family Tree

Here we represent, for the first time that we know, a family tree of Zcash
Protocol coins which use Zcash source code. We note that Bitcoin Gold (BTG)
is not listed because they use the PoW algorithm from Zcash (Equihash) but
do not use any of the privacy-related code.

Zcash originally forked the source code of Bitcoin 0.11.2 and has cherry-picked
many individual fixes and features but primarily remains Bitcoin 0.11.2 internals
with brand new Zcash features bolted on top of that.

Notably, recent developments by Bitcoin Core to manage wallets via the RPC
interface is lacking in Zcash, as well as P2P improvements.

<a href="zcash-family-tree.png" target="_blank">
<img src="zcash-family-tree.png" height="75%" width="75%">
</a>

The category of "Komodo Asset Chains" contains dozens of blockchains which
have shielded transaction support. Hush Smart Chains are similar but focus
purely on Proof-of-Work (not Proof-of-Stake) use cases and are focused on
privacy-by-default use cases. This is sometimes calles "z2z" because sending
to zaddrs is required and sending from a zaddr to a transparent address is
not allowed.

It is easy to see that ZClassic has been used as a base for many new source
code and chain forks and that Komodo has creates a micro-universe of it's
own run-time forks, such as Pirate, and source code forks, such as Hush v3.
There are close to 100 known run-time forks of Komodo which blockchain
parameters can be specified completely via the command-line and thus do not
require maintaining source code forks.

KMD originally had shielded addresses but in response to the Sprout inflation
but CVE-2019-7167, it migrated all shielded functionality to the Pirate chain and disabled
shielded features on KMD. This was a very strategic move to isolate
metadata leakage and increase the anonymity set of Pirate.

As of May 2020, Pirate and Arrow are the only Zcash Protocol blockchains
which enforce privacy by default, by disabling sending to transparent addresses.
In November 2020 Hush will join them in the bliss of privacy-by-default.

Pirate was the very first blockchain to enforce privacy by default, while
the Hush was the first pure Sapling blockchain, completely rid of the Sprout
shielded addresses. Arrow is a newer cryptocoin which builds on these
recent ideas and was the first pure Sapling blockchain to enforce
privacy by default.

Hush originally was based on Zcash 1.0.8 but in response to the Sprout CVE
we migrated to Komodo as our upstream. The original blockchain was sunset
at Block 500,000, snapshotted and airdropped to a new Pure Sapling blockchain.
by giving users and miners a choice and in that way it was User Activated
Hard Fork. The Hush community is on their second mainnet and tools
such as Hush Smart Chains can spin up a new blockchain with a single command
to experiment with new side-chains or launch new projects based on this
tech.

Hush Smart Chains support launching completely private blockchains with
no public access, or hybrids, or public blockchains which can have
delayed-Proof-of-Work protection.



