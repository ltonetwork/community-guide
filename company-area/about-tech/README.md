---
description: Hybrid architecture enabling GDPR compliance and scalability.
---

# Tech: Hybrid Architecture



{% hint style="info" %}
This is a high-level look into the LTO Network hybrid architecture and public-private setup, with a short summary on how the token comes into play. For deeper understanding, refer to [papers](../../#papers), dedicated company pages, and [Developer Area](../../developer-area/hashing-anchoring.md).

\*\*\*\*[**Help us Build!**](../../community-area/social-mining/tech-team.md)\*\*\*\*
{% endhint %}

## LTO Network in 100 words

Most blockchain projects focus on financial transactions utilizing Smart Contracts. However, this leaves an enormous B2B market untapped. The benefits those parties are actually looking for in blockchain technology are reduction of costs on paperwork, administration, and so on. They need a way to automate processes — not within, but amongst organizations — in a trustless way. They need a level playing field. This is exactly what LTO Network provides. By combining private and public layers, it allows organizations to meet GDPR and data privacy requirements, while preventing the scalability issues typically associated with blockchain projects.

## LTO Network in 300 words

LTO Network’s infrastructure allows different parties, with competing economic and/or political interests, to work within the same processes without the need to trust one another or a third party. To facilitate this, LTO Network has developed [Live Contracts](https://medium.com/harvard-undergraduate-blockchain-group/lto-network-how-reducing-power-increases-utility-bca7ca60bae4). Similar to a Smart Contract, a Live Contract provides a dynamic method for defining logic on the blockchain. However, the purpose of a Live Contract is not just to determine the state of a process, but to actively instruct humans and computers about the steps it contains.

In other words, a Live Contract is a workflow. A workflow is _a sequence of related steps or processes that are necessary to complete a particular task_. Think of it this way: a workflow has rules, where a certain action triggers another action, and so on.

A workflow is essentially the general template of a business process. For example, consider the workflow of a simple lease agreement approval, in which a document gets \(1\) drafted, \(2\) approved and \(3\) signed. A process is the specific instance of this workflow, so for example the lease agreement between parties A and B, which was drafted by an employee of B, approved by the CEO of B, and signed by both parties.

A workflow always contains certain logic: the rules mentioned before. Take for example the rule that signing can only come after approval, or that a rejection instead of an approval would lead to a re-draft of the agreement.

$$
Workflow + WorkflowRules = Live Contract
$$

Essentially, LTO Network handles inter-party Business Process Management on the blockchain. Live Contracts can be applied in a broad spectrum of areas, for example in supply chain, insurance, healthcare and KYC procedures. Moreover, the system can be used for legal contracts like lease agreements and NDA contracts. Other use cases can be found [here](../adoption/).

![](https://cdn-images-1.medium.com/max/1600/1*KszwoK2U3Pw0VVlCKyDJaw.png)

## LTO Network in 500 words

What do we usually see in blockchain projects? A TPS race with an attempt to fit everything into one general purpose blockchain \(usually referred to as layer 1\). But do we really need to do this? We don’t think so. The technology should not be looked at in abstract. Every use case has its requirements.

**LTO Network splits the functionality into two layers.**

Layer 2 consists of ad-hoc [permissionless private chains](permissionless-private-chains.md), each with their own workflow logic. Every Live Contract rests upon its own miniature chain, making for ad-hoc collaboration.

The logic in each miniature chain is defined as [Finite State Machine](https://medium.com/ltonetwork/video-how-finite-state-machine-helps-avoiding-bugs-and-stupid-mistakes-571f635618bb), which differentiates LTO Network from other side chain projects. This makes the logic in a Live Contract understandable for both humans and machines.

Each private chain is visible to and shared only with the participants that are supposed to be interacting in that particular Live Contract. This means that the number of participants on each chain is limited, as most legal contracts consist of only about a handful participants.

As a result, guaranteeing immutability on just the private chain itself is hard. This is where the public chain comes in \(layer 1\). Every event happening in layer 2 \(or rather, the fact that an event happened, not the data itself\) is being [hashed](../../developer-area/hashing-anchoring.md) onto layer 1.

A hash is _a one-way function that converts one value to another_. When a document is hashed, a unique hash is generated, consisting of just digits and letters. Because hashing is a one-way function, the document itself can never be re-generated from just the hash.

In short, the private layer is for data sharing, process automation, and collaboration. The public layer, on the other hand, acts as a security settlement layer, like an immutable digital notary for hashes of layer 2 \(a distributed hash table, of sort\). This hybrid approach makes LTO Network GDPR and data privacy compliant, as well as extremely scalable.

![](https://cdn-images-1.medium.com/max/2400/1*5Qqv61YAvsnVBUPfDJrTHA.png)

The LTO token plays an integral part in the system. We make use of our own _Leased Proof of Importance_ staking model. It is a work token acting as an economic incentive for validators on the permissionless public chain to run a node and validate transactions. But the key part is the interaction of users with the LTO token. Let’s take a closer look at both the ‘leased’ and ‘importance’ aspects:

* _Leased_ implies that you do not have to run a node yourself. Token holders can lease tokens to solution users \(companies\) directly or through a community ambassador node. This makes it possible for end users to not be directly involved with the token. **This removes frictions related to corporate use of tokens.**
* _Importance_ skews the validator reward probability based not only on the size of your stake, but also your actual usage of the network. For active users of the network, this essentially means _pay once — use forever_. In other words: **removing recurring infrastructure costs.** It also helps avoid centralization that usually plagues Proof of Stake systems by discouraging passive staking.

