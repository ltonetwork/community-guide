---
description: >-
  LTO supply exists on different chains simultaneously. But it's the same token
  everywhere!
---

# Bridge Troll

There are bridges among **Mainnet &lt;-&gt; ERC20 &lt;-&gt; BEP2** which make it possible to travel from one side to another. A bridge troll in-between manages the flow of tokens and punishes early sell-offs. It protects the community during the first 6 months \(since launch in January 2019\) and burns the tokens, according to a dynamic fee which should be counted since January 17, 2019. **It's a dynamic fee based on:** 

$$55exp(-0.5t)$$

Once someone goes from mainnet to ERC20/BEP2, and gives 40 LTO to mainnet nodes if someone goes from ERC20/BEP2 to mainnet. LTO mainnet are not directly tradeable but can come into or leave the network via bridges. For liquidity purposes, LTO ERC20 and LTO BEP2 tokens are used. The mainnet LTO coins, BEP2 LTO and ERC-20 LTO tokens share the same supply. They can be exchanged for each other using the bridge in a 1:1 ratio.

* **ERC20 -&gt; Mainnet**: 40 LTO for crossing the bridge. Given to mainnet nodes.
* **Mainnet -&gt; ERC20**: dynamic fee is taken and is forever burned.
* **Mainnet -&gt; BEP2**: dynamic fee is taken and is forever burned.
* **BEP2 -&gt; Mainnet**: 40 LTO for crossing the bridge. Given to mainnet nodes.
* **ERC20 -&gt; BEP2**: no fee, LTO Network pays the gas fees
* **BEP2 -&gt; ERC20**: not available

![](../../.gitbook/assets/lto-network-bridge-bep2-model.jpg)

{% hint style="info" %}
Check bridge fee stats in the [bot](https://t.me/LTO_FAQ_BOT). You can [make the swap within the LTO wallet](https://wallet.lto.network/start).
{% endhint %}

