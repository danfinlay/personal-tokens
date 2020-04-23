# Personal Tokens

A repository for tools and guides to help rapidly kick-start the personal-token revolution.

[A blog post I've written on personal currencies](https://medium.com/capabul/its-all-subjective-valuation-577fb5ad067f), on [Capabul](), a blog I've put my thoughts on this domain at.

## Introductory Thoughts

You may not have work, you may not have money, but if you have promises you can make and people who would value those promises, you've got yourself the makings of a bond.

A bond can be backed by anything, it can be entirely personal to you. You might do deliveries, or consultations, or grow produce, it doesn't matter. The point is that if you need cash on hand, you need to be able to make some promises that someone else will value. Heck, some close friends or family might value your tokens for free, just because they believe in your potential. You can just say "I promise to try my best to thrive and survive and do good for the world", and some people might want to contribute.

In this repository, I'm going to share with you some tools that are available TODAY that can help you mint your own token, back it with some real value (so people can sell it), establish exchange rates, distribute/sell it, and even redeem it.

This is a work in progress, so please, let me know what features/guides would be valuable to you, or even contribute yourself! I'm writing this on GitHub so that we can develop something viable faster.

## Mint Your Own Token

First of all, you'll need to choose a tool-chain for minting a token, etc. This can involve picking a blockchain, and a wallet, and a minting interface. Fortunately for you, I'm a super-opinionated crypto-wallet developer who has been working towards this for the last 4 years, so I'm going to just tell you what I think the best options right now are. We're going to deploy an ERC-20 token on the Ethereum blockchain using MetaMask when possible.

### Install a Wallet

#### On Desktop or Android

Get yourself [MetaMask](https://metamask.io/).

#### On iOS

MetaMask's beta supports limited users right now (we're working to get to the app store asap). In the meanwhile, you should probably use one of these, I won't go into why I still think you should switch to MetaMask when it's ready:

- [Status Wallet](https://status.im/)
- [TrustWallet](https://trustwallet.com/ethereum-wallet/)
- [Opera Browser](https://www.opera.com/) (yes, it has a wallet built in)

### Acquire some Ether

Transactions on the blockchain (like creating a token, or sending amounts of it) cost "gas", which you pay for with the currency "Ether". The wallet you choose should have some way of buying/depositing Ether into the wallet. If you know someone with crypto, just ask them to send you a little bit for transaction fees, that isn't much to ask.

### Mint Your Token

There is a growing number of personal-token-minting "Decentralized Apps" ("dapps") going around.

- [ERC Token Generator](https://vittominacori.github.io/erc20-generator/) is a free tool, and is very simple, so is ideal for advanced users who are willing to use multiple apps or even build their own tools.
- [Stake on Me](https://stakeonme.com/) is an app that lets you easily create a continuous sale for your own personal token.
- [Rollup](https://twitter.com/tryrollhq) is a premium personal-token solution that includes store-like features, but is invite-only at time of writing.
- [PersonalToken.me](https://personaltoken.me/) is another nice-looking site for publishing your own tokens from OpenLaw! I haven't gotten to play with it much yet, but I hope to hear from someone who does!

Whatever technique you use, you should come out with a token address. This is important, you'll want to save it. Mine is this, yours will look similar:
`0x4057950247e4ec8dc7fe399ec19ea43e80b931c8`

### Add to your Wallet

Adding custom tokens to a wallet can be a pain, but MetaMask makes it especially easy to make a simple page you can send to friends so they can add your token to their wallet.

I'll show you how to make a little page for sharing a link to your token [like this one here](https://vittominacori.github.io/watch-token/detail.html?address=0x4057950247e4ec8dc7fe399ec19ea43e80b931c8&network=mainnet&logo=http%3A%2F%2Fdanfinlay.com%2Fpics%2Favatar%2F64.jpg).

If you just visit [This Site](https://vittominacori.github.io/watch-token/) with MetaMask, you can just add your token address and a link to an icon for showing up in wallets, and it will generate a link you can share with people. You can then click that link yourself, and you now have a pretty token in your wallet! Your wallet should then allow sending tokens to whoever you want.

### Offer Goods and Services for your Tokens

- [microsponsors](https://microsponsors.io/) for selling your time.

### Establish an initial Exchange Rate

Personal tokens are cool right away, but people will take them more seriously if they can redeem them for real money, right? I sure think so.

I recommend using [Uniswap](https://uniswap.exchange/add-liquidity) to "Pool", or create an exchange rate of your token. Rather than simply partially backing your coins, like "The first 100 of my coins are worth $100, and then I'm out!", Uniswap uses something called a [bonding curve](https://yos.io/2018/11/10/bonding-curves/) to offer a buy-back at a variable rate. This is like saying "Yes, my first token is worth $100, but the fewer tokens I have left, the less each token can be redeemed for". Conversely, the more are bought, the more expensive each subsequent token is! This is a neat way of making sure that  runs on your token supply cannot deplete all your reserves, so your tokens will cling to at least _some_ value.

If you're trying to back your token, the more you can back it with, the better it will hold its price, and so the more confident your token's holders will be.

Once you have a token exchange, you're ready to start selling your tokens! You can just send people links to the uniswap page for buying your tokens, and the more they buy, the higher your token price will rise, approaching the number of tokens you posted for sale on Uniswap (the price will go up exponentially, so you'll never sell out of your tokens on Uniswap).

You can create trading links on Uniswap to send to friends. They look like this:

`https://uniswap.exchange/swap?outputCurrency=0x4057950247e4ec8dc7fe399ec19ea43e80b931c8`

Except you would replace the last part (my token address) with yours!

## Goals For This Readme

Some basic things I'd like to do:

- Mint either far more tokens than I need, or mint them freely.
- Establish trading pairs of my token on uniswap or other exchanges, so that holders of my token have a way of "cashing out" if they want to at any time.
- Give them out to close friends who I'd like to offer support to.
- Provide an easy path for recipients to use or redeem the tokens without much prior knowledge.
- Develop infrastructure that allows pairs of people to establish trading pairs between their tokens, so their holders can have access to each others' liquidity and services. (This is a bit like [Circles](https://joincircles.net/) on a bonding curve).
- Develop tools for allowing easy multi-hop personal token exchange, so that larger and larger networks of people with personal tokens can access each others' liquidity and services.
- Create simple tools that allow people to easily deploy their own personal tokens.
- Create tools that allow people to generically offer common services for their tokens (scheduling, payments, inventory, rentals, etc).

