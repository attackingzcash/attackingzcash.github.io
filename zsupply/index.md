# Zcash Shielded Supply is less than 0.5% !

## TLDR

 * Hush has 215X the percentage of shielded funds!
 * Hush mainnet has 215X more privacy than Zcash mainnet via this metric.
 * NOTE: Data for all coins is as of May 14th 2020.

## ZEC details

This command shows a transparent supply of 8.7M ZEC:

```
./zcash-cli gettxoutsetinfo
{
  "height": 830867,
  "bestblock": "0000000002b0ef5add3356f537eb4f6ef0c6d32f7ac0928d7c3e84f326fb8be7",
  "transactions": 1045827,
  "txouts": 16147776,
  "bytes_serialized": 446222859,
  "hash_serialized": "aafac5cf4b84f17bdf996f7a5b17b4a30b6f86c6ddd0da387b4946cd4e2dea2f",
  "total_amount": 8700243.65402680
}
# data from CHMEX
```
and since ZEC has 9.1M current supply, that gives 0.49% shielded supply (zsupply percentage).

This is unacceptable from an organization that spends over 1M USD per month. Why are funds not spent enforcing
privacy on mainnet? Having such a tiny percentage of shielded funds renders them mostly defenseless to blockchain analysis. They are not *real* privacy.

# Hush has 10.5% shielded supply currently

Hush is currently the only Zcash Protocol coin with a live-updating <a href="https://myhush.org/supply">zsupply</a> and
Hush currently has the highest zsupply percentage of any non-z2z coin, behind <a href="https://pirate.black">Pirate</a> and <a href="https://arrowchain.io">Arrow</a>. 
In November 2020 Hush transitions to z2z and has a countdown <a href="https://myhush.org/halving">timer</a>.
 
 
```
hush-cli gettxoutsetinfo
{
  "height": 226953,
  "bestblock": "000000018056194602178ef751f9307f2bd8bbcd9e7c8d6ce068562d298069f9",
  "transactions": 129086,
  "txouts": 468909,
  "bytes_serialized": 17858799,
  "hash_serialized": "26efffa4cf68b9a63a1229bd2e7edac69084c4c42f4a5bf840179e1da79f9083",
  "total_amount": 8065525.12301624
}
```

Since Hush has 8.06M HUSH in transparent addresses and currently 0.901M HUSH in zaddrs, that gives HUSH a zsupply % of 10.5%!

# z2z coins

## Pirate currently has about 99% zsupply
 
 I am honored to say I helped create Pirate and since Hush and Pirate share an immense amount of code, we consider her a
 sister ship, and the races have begun! We hope you have been practicing hard!
 
 Pirate was the first z2z coin and currently has 99.92% zsupply!!! Almost all of it's current 156M supply is shielded.
 
  ```
 komodo-cli -ac_name=PIRATE gettxoutsetinfo
{
  "height": 886578,
  "bestblock": "000000012993d42e6c732641e0c403791daebc5a9e761b485492fed08d738cf4",
  "transactions": 129295,
  "txouts": 185385,
  "bytes_serialized": 10582120,
  "hash_serialized": "8688634f6601a54953e20224c7941244443574d4a4859c189e6251c92a903a54",
  "total_amount": 268518.08573661
}
```
 ## Arrow is 2nd in shielded percentage
 
 Arrow currenly has 37.5M supply with 1.69M in coinbase mining addresses which gives a zsupply of 99.49%!!!
 Right on the tails of Pirate, Arrow was the second coin to ever go z2z and is much newer than Pirate.
 One of the main differences is that it is GPU instead of ASIC mineable.
 
```
./arrow-cli gettxoutsetinfo
{
  "height": 594432,
  "bestblock": "000013f41f252038d53628554aaa076a5f5df74bf3deaca745881e632223a315",
  "transactions": 541916,
  "txouts": 605752,
  "bytes_serialized": 33987750,
  "hash_serialized": "10d882b2457478a564d147e762dd15ff79550c2f34f1c1a40b0fdcc63fd97d1d",
  "total_amount": 1694019.01903109
}
 ```

## Future work

The average zsupply is a very healthy metric to study for a Zcash Protocol coin. We can
only assume that no websites render these stats because it so clearly points out that
nobody uses the features which are the entire point of the existence of Zcash.

Hush will be studying our own zsupply over time and that of all Zcash Protocol coins
as we feel it directly shows if the blockchain is actually using privacy features.

## Thanks

Special thanks to CHMEX for providing some of the raw data for this report.
