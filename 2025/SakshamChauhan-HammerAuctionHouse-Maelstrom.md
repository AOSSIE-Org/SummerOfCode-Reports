# Google Summer of Code 2025 Final Project Report

**Contributor:** Saksham Chauhan  
**Email:** sakshamchauhan707@gmail.com  
**GitHub:** [kaneki003](https://github.com/kaneki003)  
**LinkedIn:** [Saksham Chauhan](https://www.linkedin.com/in/saksham-chauhan-073a6927b/)  
**Organization:** [Australian Open Source Software Innovation and Education (AOSSIE)](https://aossie.org/)  
**Project Repository:** [Hammer-Auction-House](https://hammer-auctions.stability.nexus/) & [Maelstrom](https://maelstrom.stability.nexus/)      
**Project Duration:** 350 Hours

## Project Overview

During my Google Summer of Code 2025 journey with AOSSIE, I successfully developed and enhanced two groundbreaking blockchain projects that push the boundaries of decentralized finance and auction mechanisms. This report details the comprehensive work done on **Hammer Auction House** - a multi-protocol decentralized auction platform, and **Maelstrom** - an innovative auction-driven decentralized exchange.

Both projects represent significant contributions to the DeFi ecosystem, implementing complex smart contract architectures, modern web interfaces, and solving real-world challenges in decentralized trading and auction mechanisms.

# Hammer Auction House

## Abstract

This project presents the development and enhancement of Hammer Auction House (HAH!), a comprehensive decentralized auction platform. The platform enables users to host and participate in auctions of ERC20 tokens and NFTs through multiple sophisticated auction protocols powered by HAH!.

### Supported Auction Protocols

**All Pay Auctions:** All bidders pay their bid amount, but only the highest bidder wins the asset.

**English Auctions:** Traditional ascending price auctions where losing bidders receive full refunds and the winner obtains the asset.

**Reverse Dutch Auctions (Linear, Exponential, Logarithmic):** Time-based descending price auctions where the first bidder to place a bid wins. The accepted bid amount starts high and decreases over time following Linear, Exponential, or Logarithmic decay patterns.

**Vickrey Auctions:** Sealed-bid auctions where bidders commit hidden bids during the bidding period. During the reveal phase, the highest bidder wins but pays the amount of the second-highest bid.

All transactions and asset movements are executed on-chain through smart contracts without any human intervention, ensuring complete decentralization and trustless operation.

## GitHub Repositories
- [Hammer Auction House - WebUI GitHub Repository](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI)
- [Hammer Auction House - Solidity GitHub Repository](https://github.com/StabilityNexus/HammerAuctionHouse-Solidity)

## Deployment & Addresses
- **Hammer Auction House Frontend (Live):** https://hah.stability.nexus/
- **Smart Contract:** *Deployment in progress*

## Key Flows

### Auctioneer Flow
- **Choose Auction Type:** Select from six different auction protocols to host your auction
- **Configure & Preview:** Set auction parameters including start price, duration, and decay type. Preview how your auction will behave before deployment
- **Deploy Securely:** Deploy auction contract on-chain with automated security checks and verification

### Bidder Flow
- **Discover Auctions:** Browse active auctions with advanced filtering and search capabilities
- **Place Bids:** Connect your wallet and place bids with real-time price updates and gas estimation
- **Win & Collect:** Automatically claim your NFT or ERC20 tokens upon winning with blockchain proof of ownership

## Major Pull Requests

### Hammer Auction House - WebUI
- [#6](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/6): UI Revamp with support for all 6 protocols
- [#7](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/7): Local Storage Integration for client data storage
- [#8](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/8): End-to-End Blockchain integration
- [#10](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/10): Added strict type-checks & setup GitHub Pages deployment config
- [#11](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/11): Final UI/UX changes based on feedback
- [#12](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/12): Integrated multi-chain support
- [#13](https://github.com/StabilityNexus/HammerAuctionHouse-WebUI/pull/13): Additional changes based on contract modifications

### Hammer Auction House - Solidity
- [#6](https://github.com/StabilityNexus/HammerAuctionHouse-Solidity/pull/6): Contract suite first draft with all protocols
- [#7](https://github.com/StabilityNexus/HammerAuctionHouse-Solidity/pull/7): Add asset retrieval by auctioneer (in cases of no bids) and minBid feature in Vickrey Auction
- [#8](https://github.com/StabilityNexus/HammerAuctionHouse-Solidity/pull/8): Added Protocol Fee feature in all contract suite & simplified contract logic
- [#9](https://github.com/StabilityNexus/HammerAuctionHouse-Solidity/pull/9): Changes done during final contract audit 

---

# Maelstrom

## Abstract

This project presents the development of Maelstrom, an innovative Auction-Driven Decentralized Exchange (DEX). The platform enables users to create liquidity pools, provide liquidity to earn fees from swaps, and execute trading operations including swaps, buys, and sells.

Maelstrom introduces a novel price discovery mechanism based on the volume of buy and sell orders, designed to achieve zero slippage during trading operations. This innovative approach aims to solve one of the most significant challenges in decentralized trading - price impact and slippage for traders.

## GitHub Repositories
- [Maelstrom-WebUI GitHub Repository](https://github.com/StabilityNexus/Maelstrom-WebUI)
- [Maelstrom-Solidity GitHub Repository](https://github.com/StabilityNexus/Maelstrom-Solidity)

## Key Flows

### Liquidity Providers Flow
- **Create Pool:** Initialize new token pools with custom parameters
- **Deposit:** Deposit ETH and tokens according to pool ratio to earn Liquidity Pool Tokens (LP tokens)
- **Withdraw:** Use LP tokens to withdraw proportional pool holdings with accumulated fees

### Traders Flow
- **Swap:** Exchange between different token pairs with optimized routing
- **Buy or Sell:** Execute buy/sell orders for tokens against ETH with minimal slippage

## Deployment & Addresses
- **Maelstrom Frontend (Live):** https://maelstrom.stability.nexus/
- **Smart Contract:** *Deployment in progress*


## Major Pull Requests

### Maelstrom-WebUI
- [#1](https://github.com/StabilityNexus/Maelstrom-WebUI/pull/1): Prototype UI/UX Completed
- [#2](https://github.com/StabilityNexus/Maelstrom-WebUI/pull/2): End-to-End blockchain Integration
- [#3](https://github.com/StabilityNexus/Maelstrom-WebUI/pull/3): Resolved Next.js Server build failures
- [#4](https://github.com/StabilityNexus/Maelstrom-WebUI/pull/4): Additional UI/UX changes based on feedback
- [#5](https://github.com/StabilityNexus/Maelstrom-WebUI/pull/5): Multi-Chain support, Token-List integration & updated Price-Chart

### Maelstrom-Solidity
- [#1](https://github.com/StabilityNexus/Maelstrom-Solidity/pull/1): Contract first draft
- [#2](https://github.com/StabilityNexus/Maelstrom-Solidity/pull/2): Updated price calculation formulas & added user and pool registry
- [#3](https://github.com/StabilityNexus/Maelstrom-Solidity/pull/3): Added Protocol Fee & slippage tolerance in buy and sell orders

---

## Technical Challenges & Solutions

### Challenge 1: Code Maintainability Across Multiple Auction Protocols

**Problem:** Managing six different auction protocols simultaneously led to significant code duplication and maintainability issues. Each protocol had similar core functionality but with protocol-specific variations, resulting in code smell and repetitive implementations.

**Solution:** Implemented an abstract contract architecture that centralizes all common functionality and helper functions. This approach:
- Improved maintainability and reduced potential for bugs
- Made it easier to add new auction protocols in the future
- Ensured consistent behavior across all protocols

### Challenge 2: User Experience & Data Persistence

**Problem:** Fetching all user data from on-chain sources resulted in poor user experience due to long loading times.

**Solution:** Integrated local storage functionality to cache user session data and auction states:
- Stored user's last interaction stage locally
- Implemented smart refresh mechanisms to sync with blockchain when necessary
- Implemented batch fetching to optimize data retrieval and prevent long waiting queue.



# Technologies Used

## Frontend Development
- **Framework:** Next.js (React-based full-stack framework)
- **UI Libraries:** ShadCN UI, Material UI
- **Styling:** Tailwind CSS
- **State Management:** React hooks and context

## Blockchain Development
- **Smart Contracts:** Solidity
- **Development Frameworks:** Hardhat, Foundry

## Web3 Integration
- **Blockchain Interaction:** Wagmi, Viem
- **Wallet Connection:** RainbowKit
- **Local Storage:** Browser localStorage for caching

---

## Acknowledgments

I am deeply grateful to my mentor **Dr. Bruno Woltzenlogel Paleo** and the entire **AOSSIE team** for their constant guidance, support, and valuable feedback throughout my GSoC journey. Their expertise and mentorship were instrumental in the successful completion of both projects.

Special thanks to the Google Summer of Code program for providing this incredible opportunity to contribute to open-source blockchain technology and grow as a developer.

---
