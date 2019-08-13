---
description: How we solved the GDPR x Blockchain with ad-hoc private permissionless chains.
---

# GDPR x Blockchain

### What is GDPR?

The General Data Protection Regulation \(GDPR\) came into force on the 25th of May, 2018 and is drawing a lot of attention in the media and the corporate world. The law aims to protect data privacy of all individuals in the EU and EEA areas, while companies that do not comply with it risk hefty fines of up to €20mln or 4 percent of annual global turnover. No wonder that GDPR compliance is on top of the agenda for many firms, including those in the blockchain space. Without going too much into legal detail, the three most crucial aspects of GDPR are:

* the right to access, which gives citizens the right to access their data and to know how it’s being handled;
* the right to rectification, enabling citizens to amend and correct their personal data;
* the right to erasure, a.k.a. _the right to be forgotten,_ allowing subjects to request deletion of related personal data.

In the context of blockchain, GDPR poses an even greater challenge due to the intrinsic characteristics of the technology, even causing [some projects to shut down](https://paritytech.io/picops-discontinued-may-24th-2018/) and go out of business.

LTO Network came up with a solution makes it not only compatible with GDPR, but also desirable in the sense of data protection and privacy.

### Data storing on blockchain

Blockchain technology brings numerous advantages when comes to security and trust. The irreversibility attribute makes blockchain the perfect tool for dispute resolution and transparency. At first glance, this feature makes any blockchain, public or private, incompatible with GDPR: one just can’t possibly erase or amend data once it’s on the chain.

One of the proposed solutions is storing _encrypted_ data on the blockchain. If the encryption key is destroyed, the data become inaccessible. Unfortunately, the right to be forgotten requires the data to be erased rather than just being made inaccessible.

### Hashing

Hashing is a process that transforms data into a very long number through a mathematical formula. Unlike encryption, it’s impossible to get the original data from the hash. Identical data will always result in the same hash, but slightly altered data will always result in a very different hash. As such a hash can be used to verify that data has not been modified.

Putting a hash on the blockchain might still get you in trouble. A hash is still be considered personal data if it can be linked to the person. Let’s say the data contains a name and phone number. If you know this name and phone number, you can generate the relating hash and look for occurences of it in the blockchain.

LTO Network prevents the hash from being used for anything else than verifying received data, by putting it in an envelope together with a timestamp and some random data. The hash created form the envelope will never occur on the blockchain more than once. Additionally, the complete envelope, rather than just the personal data, is required to create the hash.

![](https://cdn-images-1.medium.com/max/1600/1*sovk9qmvY8PYUyfGG8FNYQ.png)

### Storing data on LTO Network

With a centralized system, personal data is uploaded to the system of an organization \(the controller\) for further processing. While this is possible under the rules of GDPR it’s putting a large burden on the organization to make sure the data is stored safely and isn’t being used in any other way than described by the data agreement.

The Live Contracts feature on LTO Network assist in this. A Live Contract is a digitized procedure where all the possible actions for each participant are predefined. The data is only made available within the context of the procedure and can only be used for specific actions within the procedure. Each Live Contract creates a new miniature private blockchain. This already sets the ground rules for the data agreement.

However, as a distributed system LTO Network can do one step better. Each participant will connect to the private blockchain via a node of his choosing. Each node has a private storage service, where users can store data. Users have complete control over data stored here, similar to data stored on a service like DropBox. They can remove their personal data at any time. The data is not shared or processed without a valid data processing agreement and explicit approval of the user.

_**With LTO Network, the node of the user is the controller. You are only a processor.**_

### The LTO Network private miniature blockchain

While this method of hashing and storing is useful for data minimization, the public key can still be used to track the actions of an identity on a blockchain. As such, each node of the blockchain is a data processor and requires a data processing agreement. A public chain has, by definition, a large amount of anonymous nodes. This anonymity makes consistent use of data agreements impossible. A private blockchain, on the other hand, does require each node to identity itself.

With a single private blockchain it is difficult to facilitate the right to be forgotten. When an individual wants to exercise this right, the whole blockchain would have to be erased or rewritten. While technically possible, this would severely affect the integrity of the blockchain.

LTO Network creates a private _miniature_ chain for each process. Only the nodes selected by the parties involved have this chain, similar to other distributed systems like _Git_. To safeguard the integrity of these miniature chains, each event is anchored in the LTO permissionless public blockchain.

When requested, nodes can erase specific processes. Because GDPR states that data cannot be kept indefinitely, this happens automatically after a specified retention period. Should law require data to be stored for a longer period, data can be extracted before chain erasure.

### A practical example

A private sale is digitized as the Live Contract. During the sale, the organization is required to do KYC by identifying the customer and doing a risk assessment. To comply, the customer must supply a government issue ID as well as other personal information.

The first step of the procedure asks the user to provide personal information and upload his ID.

The application wraps this in an envelope and creates a hash. The envelope with the personal data is send to the node for storage. The customer signals he has performed the action by adding an event to the blockchain. The hash is also added to the event.

Because all possible states and actions are known, the customer can pre-approve the exact situation and purpose required for the organization to get access to the data. He is also allowed to retract this permission or erase the data at any time.

Further in the procedure, a state is reached where KYC is required to continue. The organization indicates it want to perform this action. For that is needs the data entered by the customer in the first step. The node of the organization forms a data request containing the reason the data is needed, the identity of the processor, the time will be stored for processing, etc. Accepting this request automatically forms a valid data processing agreement.

If the request matches a pre-approved condition, the organization will receive a copy of the envelope containing the personal data. Once the KYC action is performed, it will add an event to the blockchain, indicating the customer has been approved. After this, the node of organization will automatically erase all traces of the personal data.

![](https://cdn-images-1.medium.com/max/1600/0*w-zU8-pouAfUMZ8o.)

In case the permission was retracted or the data was removed before the KYC, the organization will not get a copy of the data. This doesn’t hurt the integrity of the blockchain. The organization can simply deny participation of the customer and end the process.

When replaying the blockchain, it’s not necessary to have a copy of the personal data. The organization can verify it has done KYC because of the approval event on the blockchain with their signature on it.

**This is already live in a number of products! Check out the Adoption section:**

{% page-ref page="../adoption/" %}

