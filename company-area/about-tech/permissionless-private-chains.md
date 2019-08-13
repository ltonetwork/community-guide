---
description: Unique concept of ad-hoc private event chains.
---

# Permissionless Private Chains

## Part One

When I tell fellow blockchain developers and enthusiasts we have a permissionless private blockchain solution, they typically make a strange face, followed by “Did you mean public permissionless?”.

I get it. Something being both private and permissionless sound like a contradiction. So what’s going on?

![](https://cdn-images-1.medium.com/max/800/1*fLdNRTYSjVy1mfc9IWdgcQ.png)

To understand the concept, let’s first look at the difference between public permissioned and permissionless blockchains.

On a public permissioned network like Ripple or EOS, the network maintainer has the ability to appoint privileged parties. These are able to run a node with abilities that are unavailable to the general public.

On a permissionless public blockchain like Ethereum, such an authoritative party does not exist. Anybody can spin up a node and join the network to broadcast transactions or mine blocks.

Still, it’s possible that there are things that I’m allowed to do on the Ethereum network, while you are not. In a smart contract, we can define an action that may only be performed by the contract’s owner and not by others. So a permissionless blockchain means there is no authority on a network level. The logic deployed on the chain, in the form of a smart contract, _does_ define permissions.

Similar to the public permissionless network, anyone can spin up a node to join a **private permissionless** network. However, unlike on a public blockchain, other nodes will only acknowledge its existence, but not share any data. At least not just yet.

The smart contracts on these private networks, not only define who is allowed to perform contract actions but also who is allowed to read the contract and all related data.

To accomplish this, private permissionless solutions don’t create a single chain shared by everyone. Instead, each instantiation of a smart contract has its own ad-hoc chain. In other words;

> Deploying a smart contract on a permissionless private network automatically creates a private \(side-\)chain associated with that contact.

A single node holds multiple of ad-hoc chains, but never all of them. You might compare it to _**git**_, where a single system holds multiple repositories.

Read privileges aren’t granted to specific nodes, but to specific persons or organizations \(identified by a cryptographic signature\). This is similar to the privilege to perform a smart contract action on Ethereum.

Each contract has a unique identifier \(or address\). Nodes also have an address in the form of a URL. To get a copy of a contract and the associated chain, you need to know both the contract identifier and the URL of a node that has a copy.

You can use any node, possibly your own or just one you trust, to request a copy of a private ad-hoc chain and start participating on the contract. A node only holds the data it needs to service its users, rather than all information on the network. This approach is coined by Holochain as **agent-centric**solutions.

### Projects

There are a lot of different types of problems you can solve with such a system, that you can’t tackle with a private permissioned or with public solutions.

With that in mind, this space seems to be highly undercrowded. I’m only aware of three active projects with a private permissionless component._\*\*_

![](https://cdn-images-1.medium.com/max/800/1*W3_dmkbCUSUti30BqvjLvg.png)

**Holochain**

Arguably the best know platform in this space is Holochain. A platform for decentralized applications, where users share information peer-to-peer on a need-to-know basis. Holochain abandons the shared hash chain altogether in favor of treading transactions as individual entities which can be validated through a distributed hash.

**LTO Network**

Our project, LTO Network, is a platform to run trustless workflows, targeting multinationals and governments. The process has a strong focus on privacy and GDPR compliance. LTO Network replaces smart contracts with Live Contracts, which define both on-chain logic and off-chain instructions.

**Monet**

Monet is a project for building ad-hoc, short-lived chains, with mobile devices acting as nodes for the participants. Collaborations are fluid as both participants come and go and nodes may be discovered based on location.

## Part Two

Once fellow blockchain developers and enthusiasts come to grips that a permissionless private blockchain is an actual thing, a new question typically follows; “Why can you not do that on _\[fill in some other blockchain\]_”.

![](https://cdn-images-1.medium.com/max/800/1*nC0VzCnQ3X-TPEBXgahIAg.png)

In [part 1 of this series](https://medium.com/ltonetwork/the-rise-of-private-permissionless-blockchains-part-1-4c39bea2e2be), I explained how a permissionless network may deal with private chains and summed up the projects in this space.

Let’s explore the differences to public permissionless chains by comparing LTO Network with Ethereum and to private permissioned chains by comparing it with Hyperledger Fabric.

_The comparison is on a conceptual level, only focussing on public vs private and permissionless vs permissioned._

### Private data on Ethereum

Ethereum has quickly become the defacto platform for decentralized blockchain applications. With a strong developer community an rich ecosystem, it makes sense to look at Ethereum first when building such apps.

To state the obvious, as a public network, all information on Ethereum is public. Every node has a copy of the full ledger. This is required because every node needs to execute the code defined in a smart contract to get calculate the current state.

Organizations are bound by regulations to respect and protect privacy, like the European GPDR. But even without regulations; organizations are typically not willing to make all the interactions they have with partners and clients public to the world. And for a good reason.

Basic encryption doesn’t provide a great solution, as encrypted data can’t be processed by a smart contract. Advances techniques like homomorphic encryption might change that someday. However, the mere interactions on the encrypted data are already more than organizations want to share.

There are some projects that are working on a hybrid solution for Ethereum, where some data kept off-chain and referenced in the smart contract. This is a good approach and applicable situations where it’s okay if most information may be public with just some details that need to be hidden.

However, when most of the information should not be publically shared, you end up with a situation where you aren’t utilizing the functionality of Ethereum but are paying the price for it \(quite literally in gas\).

This has led many organizations to take an interest in a permissioned private blockchain they control, like creating a private Ethereum network or more commonly using Hyperledger Fabric.

### Hyperledger Fabric and ownership

When it comes to blockchain for the enterprise, organizations are typically pointed towards Hyperledger Fabric; a general purpose private permissioned blockchain, backed by IBM.

Similar to Ethereum; data is shared with all nodes so it can be processed by the smart contract. Hyperledger does however natively support SideDBs, allow some data only to be shared with specific nodes.

At first glance, owning and managing your own blockchain seems great. And in some cases it is. Hyperledger is known as consortium blockchain, and for existing consortiums with a settled control structure, this might be the right solution.

Where there isn’t a consortium in place, individual organizations are setting up a blockchain. Here is where [ownership really becomes an issue](https://medium.com/ltonetwork/why-ibm-and-the-maersk-group-venture-was-doomed-to-fail-the-state-of-b2b-blockchain-adoption-dfff01e4b6fc). Having the dominant platform for your sector is an enormous competitive edge. A permissioned network doesn’t level the playing field in the way a permissionless blockchain does.

The value of a blockchain comes from being decentralized. If you’re the only party on the network, there is little to be gained. The true challenge is convincing others to join your network.

In situations where there is already a power imbalance, a party can already force the use of their \(centralized\) system. When it comes to competitors or more generally, parties with misaligned interests, are less likely to join your network and more likely to create a network of their own.

Creating a consortium blockchain ultimately means creating a consortium. It requires rules and regulations, membership procedures, etc. There are costs involved in setting up and maintaining the chain as well as other overhead costs.

With all this effort, interaction is still only possible with other members of a consortium. On a permissionless network, you can collaborate with any party on a case-by-case basis.

### LTO Network

Permissionless private networks allow businesses to collaborate without the need of creating a consortium or resort in sharing information publically.

Unlike private permissioned blockchains, all LTO nodes can communicate with each other, forming a single network that nobody controls. With LTO Network, the functionality of the public layer is limited to verifying data and event. In general, private permissionless are not the right solution if you want to interact with everybody on the network.

Regardless of the type of network, it will be difficult to get all your clients, partners, and suppliers on board. LTO can also be used, as a centralized workflow engine, with just a single node. Others can connect when they are ready for it.

> Decentralization is a feature, not a product.  
> - Jackson Palmer

Parties come to an agreement among themselves on a case-by-case basis and define these in a Live Contract.

Live Contracts are constructed in such a way, that they can be visualized \(as a flowchart\) and discussed by the decision-making authority with an organization. This way, blockchain contracts can be handled in the same way as any other type of agreement.

Blockchains should not be treated in abstract disregarding the use cases. What a decentralized peer to peer money needs from the blockchain is quite different from what an organization needs from the blockchain.

