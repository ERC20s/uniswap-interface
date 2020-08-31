# UniChad.com
A balancer.finance style AMM (automated market maker) DAPP on xDai sidechain..

Build a dapp by copying balancer solidity/go smart contracts, that does market making trades on the xDai network (similar to ropsten).

# Example trade:
1. User A wants to buy 1 ETH for $400 from the pool.
(in the same way that uniswap/balancer works)

2. CHAD smart contracts borrow 1 ETH and $400 by minting CHAD and selling it to the xDai pool (CHAD/xDai).
So the oracle trades $800 CHAD for $800 xDai then $400 xDai for 1ETH..
So the CHAD oracle is in $800 profit

3. CHAD oracle then places 'limit orders' to sell the XDAI/ETH at a 5% profit.. 
Selling 0.1ETH at $404 and Increasing 1% until 0.1ETH for $440.
This is known as market making.
Whenever we sell 0.1ETH; we buy back the CHAD token..

# Conclusion
1. We make 5% profit on most of our trades due to market volatility.

2. Bull market: CHAD will gain value.
Bear market: CHAD will mint a lot of CHAD and accumulate tokens


# Additional features

1. The Chad Admin Address has ability to market sell everything in its address to buy CHAD. 

2. CHAD smart contract can borrow from the pool to migrate liquidity from uniswap to unichad?

3. CHAD tokens works in a DAO
Where the token holders vote to decide which contract address' to whitelist/blacklist for e.g. eth/xDai/MKR/etc

# Workflow

1. Fork smart contracts from balancer.finance https://github.com/balancer-labs/balancer-exchange
2. Deploy CHAD token with burn/mint functions.
3. Add buy/sell functions as described.
4. Import everything into unichad.com interface on xDai
5. Migrate liquidity. https://github.com/balancer-labs/balancer-sor


# Uniswap Interface

[![Tests](https://github.com/Uniswap/uniswap-interface/workflows/Tests/badge.svg)](https://github.com/Uniswap/uniswap-interface/actions?query=workflow%3ATests)
[![Styled With Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://prettier.io/)

An open source interface for Uniswap -- a protocol for decentralized exchange of Ethereum tokens.

- Website: [uniswap.org](https://uniswap.org/)
- Interface: [app.uniswap.org](https://app.uniswap.org)
- Docs: [uniswap.org/docs/](https://uniswap.org/docs/)
- Twitter: [@UniswapProtocol](https://twitter.com/UniswapProtocol)
- Reddit: [/r/Uniswap](https://www.reddit.com/r/Uniswap/)
- Email: [contact@uniswap.org](mailto:contact@uniswap.org)
- Discord: [Uniswap](https://discord.gg/Y7TF6QA)
- Whitepaper: [Link](https://hackmd.io/C-DvwDSfSxuh-Gd4WKE_ig)

## Accessing the Uniswap Interface

To access the Uniswap Interface, use an IPFS gateway link from the
[latest release](https://github.com/Uniswap/uniswap-interface/releases/latest), 
or visit [app.uniswap.org](https://app.uniswap.org).

## Listing a token

Please see the
[@uniswap/default-token-list](https://github.com/uniswap/default-token-list) 
repository.

## Development

### Install Dependencies

```bash
yarn
```

### Run

```bash
yarn start
```

### Configuring the environment (optional)

To have the interface default to a different network when a wallet is not connected:

1. Make a copy of `.env` named `.env.local`
2. Change `REACT_APP_NETWORK_ID` to `"{YOUR_NETWORK_ID}"`
3. Change `REACT_APP_NETWORK_URL` to e.g. `"https://{YOUR_NETWORK_ID}.infura.io/v3/{YOUR_INFURA_KEY}"` 

Note that the interface only works on testnets where both 
[Uniswap V2](https://uniswap.org/docs/v2/smart-contracts/factory/) and 
[multicall](https://github.com/makerdao/multicall) are deployed.
The interface will not work on other networks.

## Contributions

**Please open all pull requests against the `master` branch.** 
CI checks will run against all PRs.

## Accessing Uniswap Interface V1

The Uniswap Interface supports swapping against, and migrating or removing liquidity from Uniswap V1. However,
if you would like to use Uniswap V1, the Uniswap V1 interface for mainnet and testnets is accessible via IPFS gateways 
linked from the [v1.0.0 release](https://github.com/Uniswap/uniswap-interface/releases/tag/v1.0.0).
