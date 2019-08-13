---
description: Defeating centralization with Leased Proof of Importance
---

# LPOI

Almost a year ago, on a cold day, the team sat down to discuss a radical new idea; should we create LTO as an open permissionless network? Initially, LTO was going to be a network controlled by us, with licensed nodes.

Permissioned networks had become the defacto choice for blockchains with an enterprise focus. It seemed logical that we’d also go in that direction. However, we couldn’t shake the feeling that a centrally controlled network isn’t what blockchain is about.

Giving up control can be a scary thing. We could no longer depend on intervening in any way. Instead, we had to brush up on game theory; how would the rules of the network influence the behavior of the participants.

Before we could stipulate the rules, we needed to decide on what we wanted to accomplish.

If a large portion of a permissionless network is controlled by bad actors, they’ll abuse that power for short term gain, hurting the network in the long run. Businesses that depend on the network to be secure and trusted, are much more likely to be a good custodian.

> LTO Network should be controlled by participants that use it on a daily basis.

**Leased Proof of Stake**

Users of the network, which include governments and large corporations, would require to own and hold LTO tokens. However, often these organizations aren’t comfortable with dealing with crypto tokens directly.

Leased Proof of Stake is a way to deal with this. Large organizations tend to deal with integrators for their software solutions, making integrators ideal candidates for tokens holders.

Unfortunately, Leased Proof of Stake tends to lead to centralization, which isn’t the dynamics we had in mind. Token holders primarily lease to big pools, as they can yield the highest return and are perceived as most trustworthy.

> Over 75% of the NXT network is controlled by only 3 nodes.

![](https://cdn-images-1.medium.com/max/1600/1*4__jz_oGXBcKDVXS3CopMg.png)

**Proof of Importance**

One way of combatting centralization is by rewarding nodes not only based on the tokens staked, but also based on usage. For LTO Network, transactions would mostly be done by organizations running nodes, rather than by individuals, making this a viable option.

NEM had already introduced a concept of rewarding usage called Proof of Importance. It’s a fairly complicated algorithm. Luckily, the dynamics of LTO Network would allow us to implement this in a much simpler way.

Aiming to incentivize staking according to the percentage of transactions, we skew the probability of forging a block towards those token holders that actually use the network by contributing transactions. For example;

* If a user stakes 10% of the total number of tokens staked on the network and contributes 10% of the total transactions, his chances of validation will be higher than 10%.
* If a user stakes 10% of the total token supply but does not contribute any transactions, his chances of validation will be lower than 10%.

The ratio between the staked tokens and transactions a node does \(S/T ratio\) determines the raffle factor. This raffle factor increases the chance of forging a block for a node that actively uses the network up to 150%, compared to a node with an equal stake that doesn’t do any transactions.

![](https://cdn-images-1.medium.com/max/1600/1*-xK6Aurvib8FjJkxVtEpxQ.png)

**Importance inflation**

A big risk of Proof of Importance is importance inflation; a node can do spam transactions just to increase to raffle factor. Fortunately, simple math shows that the costs of those spam transactions would negate the rewards if the raffle factor is below 200%.

A node holds 1% of all staked tokens and gains 100 LTO from transaction fees per day without doing any transactions itself. The node would need to 1% of all transactions to get a raffle factor of 150%. To achieve this, it needs to spend between 100 LTO and 150 LTO \(based on the raffle factor of the other nodes in the network\). It means it yields 50 LTO to 100 LTO **LESS** than before the spam transactions.

The unique use cases of different blockchains require different reward schemes for the consensus algorithm. In some cases, keeping control is the only way to combat abuse. Fortunately, Leased Proof of Importance provides the right incentives for users targeted by LTO Network, allowing it to stay true to the spirit of blockchain; permissionless and trustless.

