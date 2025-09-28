# Google Summer of Code 2025 Final Project Report

- **Name:** Kanishk Sogani
- **GitHub:** [KanishkSogani](https://github.com/KanishkSogani)
- **Social Profiles:** [LinkedIn](https://www.linkedin.com/in/kanishk-sogani/)
- **Organization:** [Australian Open Source Software Innovation and Education (AOSSIE)](https://www.aossie.org/)
- **Projects:**
  - [VouchMe](https://github.com/StabilityNexus/VouchMe) — Improved the decentralized testimonial system by adding structured testimonial flows, Waku-based messaging, enhanced UI/UX, social sharing, and new smart contract features like update/burn.
  - [TNT (Trust Network Tokens)](https://github.com/StabilityNexus/TNT) — Redesigned and modernized the entire UI and flows for issuing, revoking, and managing trust tokens, making the platform clearer and more accessible.

## Abstract

During GSoC 2025, I contributed to two projects under Stability Nexus — **VouchMe** and **TNT (Trust Network Tokens)**.

- **VouchMe**: Enhanced how testimonials are created, delivered, displayed, and managed. Key work included structured testimonial forms, Waku integration, smart contract improvements, and UX refinements.
- **TNT**: Focused on rebuilding the UI/UX to simplify and improve how users issue, manage, and interact with trust tokens.

Together, these contributions strengthen the ecosystem for decentralized trust and reputation.

## Project Overview

**VouchMe**  
VouchMe is a blockchain-based testimonial system that enables users to **request, sign, and store testimonials** on-chain, ensuring full ownership and decentralization. It serves as an alternative to centralized reputation systems like LinkedIn endorsements and marketplace ratings, which are controlled by platform owners and can be censored, monetized, or lost.

By storing testimonials on-chain, VouchMe ensures that users can maintain their professional and personal credibility across different platforms without the risk of data loss due to bans or platform shutdowns.

**TNT (Trust Network Tokens)**  
TNT is a platform that allows users to issue and, optionally, revoke Trust Network Tokens (TNTs)-ERC721 tokens that represent trust relationships between individuals or organizations.

TNTs have a wide range of applications, such as:

- Universities issuing TNTs to graduates to certify their expertise.
- DAOs distributing TNTs to members as a trust badge.
- Businesses issuing TNTs to loyal customers as a sign of endorsement.

## Technologies Used

- **Frontend:** Next.js, TypeScript, TailwindCSS, RainbowKit
- **Blockchain / Smart Contract:** Solidity, Foundry
- **Additional Tools:** GitHub Actions, Wagmi, Viem

## Deployments & Addresses

- **VouchMe Frontend (live):** https://vouchme.stability.nexus/
- **VouchMe Smart Contract:** [Sepolia Testnet](https://sepolia.scrollscan.com/address/0x344fe9f4bee36dadd4b584be8e9a968b1515d291)
- **TNT Frontend (live):** https://tnt.stability.nexus/

## Project Details

### VouchMe Enhancements

1. Integrated **Waku messaging** for decentralized, peer-to-peer testimonial delivery.
2. Redesigned **Write/Testimonial pages** with structured fields (name, testimonial, GitHub/LinkedIn).
3. Enhanced testimonial display: show giver’s name, links, and timestamps.
4. Added **social sharing features** — share testimonial requests or testimonial cards directly.
5. Upgraded smart contract: burn (soft delete), testimonial updates, enforce one active testimonial per sender–receiver.
6. Improved UX: clearer error handling, loading states, and lock screens for restricted pages.

### TNT UI / Flow Overhaul

1. Revamped **landing page** for better clarity and engagement.
2. Created a guided **“Create TNT” flow** with a more intuitive form.
3. Redesigned **“My TNTs” page** to better show issued and received tokens.
4. Refined **Token Actions page** for issuing, revoking, and burning tokens with a more user-friendly interface.

## Pull Requests

### VouchMe

- [#7](https://github.com/StabilityNexus/VouchMe/pull/7) — Dashboard, Testimonials & Write Page with Web3 Integration and Multi-Chain Deployment
- [#8](https://github.com/StabilityNexus/VouchMe/pull/8) — Deploy on Ethereum Classic Mainnet
- [#9](https://github.com/StabilityNexus/VouchMe/pull/9) — Fix TypeScript Errors and Update Pages
- [#10](https://github.com/StabilityNexus/VouchMe/pull/10) — Fix GitHub Actions and Dynamic Address Handling
- [#11](https://github.com/StabilityNexus/VouchMe/pull/11) — Config Update
- [#12](https://github.com/StabilityNexus/VouchMe/pull/12) — Add Loading States, Bug Fixes & Toast Notifications Improvement
- [#13](https://github.com/StabilityNexus/VouchMe/pull/13) — Add user profiles and enhanced testimonial management to VouchMe contract
- [#14](https://github.com/StabilityNexus/VouchMe/pull/14) — Add Comprehensive Foundry Test Suite for VouchMe Smart Contract
- [#15](https://github.com/StabilityNexus/VouchMe/pull/15) — Implement Profile Management & Testimonial Flow Improvements
- [#16](https://github.com/StabilityNexus/VouchMe/pull/16) — Waku integration
- [#17](https://github.com/StabilityNexus/VouchMe/pull/17) — Update Dashboard and other pages UI/UX
- [#18](https://github.com/StabilityNexus/VouchMe/pull/18) — fix indentation and UI/UX update
- [#19](https://github.com/StabilityNexus/VouchMe/pull/19) — Update the landing page and add the total users and testimonials count

### TNT

- [#7](https://github.com/StabilityNexus/TNT/pull/7) — Add new landing page
- [#16](https://github.com/StabilityNexus/TNT/pull/16) — Revamp Core TNT Pages UI
- [#21](https://github.com/StabilityNexus/TNT/pull/21) — Added IndexedDB Caching and Protected route provider
- [#22](https://github.com/StabilityNexus/TNT/pull/22) — update navbar and buttons text

## Challenges & Solutions

1. **Decentralized messaging with Waku**

   - _Challenge:_ Delivering testimonials gas-free without relying on centralized servers was a challenge.
   - _Solution:_ I integrated Waku messaging into the dApp to allow gas-free testimonial requests and sharing. Users are authenticated via their Ethereum wallets, and messages are encrypted and relayed through decentralized Waku nodes, ensuring censorship resistance and reliability.

2. **Smart contract flexibility for testimonials**

   - _Challenge:_ On-chain data is permanent, making edits and deletions complex. Designing a contract that supports updates while maintaining integrity was a key hurdle.
   - _Solution:_ I added soft-delete (burn) and update functionality to the VouchMe contract. Instead of erasing history, testimonials are marked as deleted for transparency. I also enforced one active testimonial per sender–receiver pair. These updates were backed with Foundry unit, fuzz, and invariant tests to ensure robustness.

3. **UI clarity in TNT**
   - _Challenge:_ The old TNT interface was unintuitive, making token issuance and revocation confusing for new users.
   - _Solution:_ I redesigned the UI with a step-based token creation flow, a revamped “My TNTs” page for issued/received tokens, and a clearer Token Actions page. The landing page was also rebuilt to better explain TNT’s purpose, lowering the learning curve significantly.

## Acknowledgements

I am deeply grateful to my mentor [Dr. Bruno Woltzenlogel Paleo](https://www.linkedin.com/in/brunowp/) and the [AOSSIE](https://aossie.org/) team for their constant guidance, support, and valuable feedback throughout my GSoC journey.

---

### Thank You!
