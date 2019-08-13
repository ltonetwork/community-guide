---
description: Token lockups and diluted circulating cap.
---

# Distribution & CMC

Foundation tokens, 50M LTO, are locked forever. 81M LTO are not actually circulation: they are only release as part of M&A Fund, which means it is not inflation. 53M out of the remaining supply is dedicated to a multi-year gradual programme which is released only if there is more activity and holding. This leaves around 165M for secondary market exposure, partially under Bridge Troll fee. [Check the bot for the live stats.](https://t.me/LTO_FAQ_BOT)

![](https://cdn-images-1.medium.com/max/1600/1*CgRYLna230P5lMrDQcV3JA.jpeg)

### **Foundation wallet = locked forever**

50M LTO, which is almost 11% of the total supply, is now locked forever. This will never hit the secondary market. ****The Foundation keeps improving the network and needs to retain a vote for major decisions going forward.

### **Social and Network Mining over a few years**

Marketing & Partners wallet is being re-calibrated into:

* **Community Programme:** 6.5% of the total supply is used for social mining incentives over a period of a few years. ****The gradual schedule is a guideline, it can be lower. Besides, **the community programme requires participants to hold LTO continuously, it is not any kind of airdrop**. It’s not just making the supply go higher, it only goes higher if the holding and engagement are higher \(think of a hash rate model\). [Read more here.](../../community-area/social-mining/)
* **Strategic Partners:** 3.3% of the total supply is used as developer grants and for onboarding integrators, to foster network adoption. These are also not to be sold. They are intended for leasing to influential early adopters that require the opportunity to try out the network before fully committing to it. If you were to make a supply chart, keep in mind a 100,000 LTO rewards would be depleting over a period of a year or so depending on the size of the integrator. So these are also long-term rewards.
* **Network Incentives:** 1.75% of the total supply is used for network mining incentives for over a period of a few years, ****to encourage the community to run more nodes. SO just as the community programme, it requires network participation to get some rewards. In addition to that, it can be used as a separate wallet for doing specific marketing/tech tasks as an external developers.

### **M&A Fund = locked until 2021**

The biggest supply, 81M LTO \(18%\), is reserved for M&A \(Mergers and Acquisitions\) and remain unused until at least summer 2021. As blockchain fights to find more adoption, some projects with a great team and technology, might not be able to maintain their token value. Projects which synergise with LTO and are undervalued in terms of market cap, may be acquired by merging that network into LTO Network. This is done by swapping those tokens for LTO, after which they will be rendered obsolete \(and thus valueless\). By doing so, the market cap of that project is added to LTO Network’s market cap.

{% embed url="https://docs.google.com/spreadsheets/d/1SaPvNOHk8SPMEUP9L-1OOBpGw8b6xKxQkmJE9f5zsA8/edit?usp=sharing" %}

* Seed round: [3JyYeRgJ7PeDskSvUEaFAswrd2Meo1c66hi](https://explorer.lto.network/address/3JyYeRgJ7PeDskSvUEaFAswrd2Meo1c66hi)
* Private Sale: [3JqAR1VoweDz3ZmEM1Mr3gC8FWdXGp22x3P](https://explorer.lto.network/address/3JqAR1VoweDz3ZmEM1Mr3gC8FWdXGp22x3P)
* Crowd Sale: [0xaDF10Eb786B160AEA0037887A4B95341B9b68434](https://etherscan.io/address/0xadf10eb786b160aea0037887a4b95341b9b68434)
* Team: [3JwXzo1nHcn2YhSMPmLwHx88rTDvvMSoXNf](https://explorer.lto.network/address/3JwXzo1nHcn2YhSMPmLwHx88rTDvvMSoXNf)
* Advisors: [3Jw2YRaQjgRF8KEjEWQv4fBjPEZnGvuBrtB](https://explorer.lto.network/address/3Jw2YRaQjgRF8KEjEWQv4fBjPEZnGvuBrtB)
* Foundation \(B.V.\): [3Js6LD9qsYG8FV7x7ntY2Jwym9cn94975so](https://explorer.lto.network/address/3Js6LD9qsYG8FV7x7ntY2Jwym9cn94975so)
* M&A Fund: [3Jdj7k1693T8YJJcQe2xEus1e62Zwj4RUDv](https://explorer.lto.network/address/3Jdj7k1693T8YJJcQe2xEus1e62Zwj4RUDv)
* Community & Incentives: [3Jx1sh2J3CsWgtzSUwUMiWo9zvcaeJN5GHE](https://explorer.lto.network/address/3Jx1sh2J3CsWgtzSUwUMiWo9zvcaeJN5GHE)

## Circulating Cap and Diluted Circulating Cap 

[Here is the API call](https://bridge.lto.network/stats/total-supply) and how to understand it.

```text
"burn_rate": 0.1865
"initial_supply": 500000000,
"total_supply": 454432624.9657278,
"burned_supply": 45567375.03427219,
"circulating_mainnet": 138763969.73501623,
"private_supply_mainnet": 269207877,
"circulating_erc20": 43294111.23071159,
"private_supply_erc20": 3166667

These numbers were taken as an example on March 22.
```

* **Burn Rate** refers to [Bridge Troll](bridge-troll.md) fee
* **Initial supply** was 500M LTO, but keeps decreasing due to crowd sale and bridge troll burns
* **Total Supply** is the current total ever available supply, it does not get bigger, only smaller
* **Burned Supply** is how much is burned due to unsold crowd sale and Bridge Troll swaps
* **Circulating Mainnet** is the amount of tokens controlled by the secondary market. Those are not directly available to be tradeable, only after the Bridge Troll swap.
* **Private Supply Mainnet** are company wallets, most tokens will never enter circulation
* **Circulating ERC-20** is the directly available for trading secondary market supply
* **Private Supply ERC-20** is the company wallet dedicated to Market Making

Okay, now let's get to easier numbers. Circulating Cap is referred to by everyone as Market Cap. That always takes into only account directly liquid tokens. In this case, only Circulating ERC-20: _Circulating Cap = Circulating ERC20 \* TokenPrice_

Now to a more complicated concept: Diluted Circulating Cap. This metric takes into account locked or vested tokens of all rounds, but for some reason CMC does not show it. _Diluted = CirculatingCap + Circulating Mainnet  \(100 - BurnRate\)  Price_

You don't have to calculate it all yourself. [Just ask our Telegram Bot](https://t.me/LTO_FAQ_BOT).

