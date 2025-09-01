# Google Summer of Code 2025 Final Project Report
<img width="1086" height="620" alt="image" src="https://gist.github.com/user-attachments/assets/961a05ca-e5bd-4d6e-bf74-b502e6c40793" />


Contributor: Karan Kumawat  
Email: kumawatkaran523@gmail.com  
GitHub: [kumawatkaran523](https://github.com/kumawatkaran523)  
LinkedIn: [Karan Kumawat](https://www.linkedin.com/in/karan-kumawat-26770b24a/)  
Organization: [Australian Open Source Software Innovation and Education (AOSSIE)](https://aossie.org/)  
Project Repository: [Chainvoice](http://github.com/stabilityNexus/chainvoice/)  
Mentors:  [Dr. Bruno Woltzenlogel Paleo](https://www.linkedin.com/in/brunowp/), [Aditya Bhattad](https://www.linkedin.com/in/adityabhattad/)    
Project Duration: 350 Hours

## Abstract
This project presents the development and enhancement of Chainvoice, a blockchain-based invoicing platform that automates cryptocurrency payment workflows. Traditional crypto invoicing requires manual PDF sharing, error-prone address copying, and tedious payment tracking. Chainvoice eliminates these inefficiencies through automated, on-chain invoice management.

The implementation introduces privacy-enhanced invoice storage, multi-token payment support, pre-filled invoice links, batch processing, and enhanced UI/UX design. The system leverages smart contract automation and encryption technologies to create seamless payment experiences for freelancers, businesses, and Web3 organizations, transforming manual crypto invoicing into an automated, trustless system.

## Technologies Used
- Frontend: React.js, TailwindCSS, ShadCN UI, Material UI
- Blockchain: Foundry, Solidity
- Additional Tools: Wagmi, Viem, Rainbow Kit, React Hook Form

## Github Repository
[Chainvoice Github Repository](https://github.com/stabilityNexus/chainvoice/)

## Project Demonstration
[🎥 Click to Watch the Demo Video](https://www.youtube.com/watch?v=fZJ3YqzwXZg)

## Test Deployed Instances
Smart Contract: [Sepolia Testnet](https://sepolia.etherscan.io/address/0x54a542dCDC306eE281b5De4613EcEfe6e6ABc562)
Frontend: Coming Soon...

## Problem Statement and Motivation
Current cryptocurrency invoicing faces critical challenges:

### Manual Process Inefficiencies:
- PDF invoice sharing with wallet addresses
- Error-prone manual address copying
- Manual blockchain payment verification
- No automated invoice tracking
### Security and Privacy Concerns:
- Sensitive financial data exposed on public blockchains
- No encryption for invoice details
- Lack of access control mechanisms
### Operational Limitations:
- Limited payment token options
- No bulk processing capabilities
- Complex address sharing workflows
- Absence of professional documentation tools

## Technical Implementation
Core Innovation: Automated Blockchain Invoicing  
The implementation transforms traditional cryptocurrency payments into an automated, secure system through comprehensive workflow automation and privacy protection.

### Phase 1: Privacy Enhancement Implementation (Weeks 1-2)
#### Lit Protocol Integration for Invoice Encryption

- Implemented comprehensive Lit Protocol encryption and decryption for secure handling of sensitive invoice data
- Developed hybrid encryption system using AES-256 symmetric keys with wallet-based access control
- Streamlined smart contract architecture to handle encrypted invoice data only, removing plaintext sensitive fields
- Established secure data sharing between authorized parties with automatic encryption/decryption workflows
- Integrated access-controlled decryption ensuring only invoice creators and recipients can view details

#### Smart Contract Optimization:

- Refactored contract ABI with updated function names and parameters
- Removed obsolete methods and detailed invoice fields from on-chain storage
- Implemented encrypted data storage with proper access control mechanisms

### Phase 2: Multi-Token Payment Infrastructure (Weeks 3-4)
#### Comprehensive ERC-20 Token Integration

- Extended smart contract architecture supporting both native cryptocurrency and ERC-20 token payments
- Implemented dynamic, chain-aware token selection with searchable modal interfaces
- Developed custom token verification flow with on-chain validation and status badges
- Created curated token presets for faster selection across different networks including testnet support
- Added automatic token metadata and logo resolution with robust fallback systems

#### Enhanced Token Selection UX:

- Built TokenPicker with searchable modal, token avatars, and copy-to-clipboard functionality
- Implemented token carousel and comprehensive token selector with preset and custom verification options
- Added real-time balance checking and payment capability verification for selected tokens

### Phase 3: Sharable Invoice Links Implementation (Weeks 5-6)
#### Intelligent Pre-filled Invoice Generation

- Created dedicated "Generate Link" page for creating sharable, prefilled invoice links
- Implemented URL-based form prefill system eliminating manual address entry errors
- Developed wallet connection prompts and automatic chain validation
- Integrated secure link generation with embedded wallet addresses, token contracts, and network IDs
- Added copy-to-clipboard functionality for seamless link sharing

#### User Experience Enhancements:

- Enhanced navigation with improved active state highlighting
- Added new routing system for Generate Link functionality
- Implemented comprehensive error handling and user feedback mechanisms

### Phase 4: Advanced Features & UI/UX Overhaul (Weeks 7-10)
#### Complete Interface Redesign

- Redesigned Landing page, Dashboard, Sent/Received invoice views, and navigation bar
- Revamped entire application layout with modern, intuitive design patterns
- Enhanced invoice creation flow with step-by-step guidance and real-time validation
- Improved invoice views with richer data tables, status chips, and detailed invoice drawers
- Invoice Management System
- Implemented comprehensive invoice cancellation for unpaid invoices with proper access controls
- Added print and download functionality for professional invoice documentation (PNG format)
- Enhanced invoice status tracking with visual indicators and automated updates
- Created detailed invoice drawer views with comprehensive invoice information

#### Advanced UI Components:

- Added Dialog, Separator, Avatar, and CopyButton components for enhanced user interactions
- Implemented global toast notification system with improved styling and timing
- Integrated animation dependencies (framer-motion) for smooth user experience
- Added react-window for optimized large dataset rendering

### Phase 5: Documentation & Treasury Management (Weeks 11-12)
#### Treasury Administration Features

- Implemented treasury admin functionality for fee and treasury address management
- Added comprehensive withdrawal flow for accumulated platform fees
- Integrated Citrea testnet support for extended network compatibility
- Created detailed deployment instructions for Ethereum Classic using Foundry
- Comprehensive Documentation & Testing
- Enhanced README with detailed deployment steps and setup instructions

### Relevant Pull Requests

#### Initial Development (Main Branch)
- Project Initialization
- Set up the project structure and development environment
- Configured blockchain development tools and dependencies
- Smart Contract Implementation
- Developed core smart contracts for invoice management
- Frontend Implementation
- Developed comprehensive dashboard with invoice management

After the initial development on the main branch, I transitioned to creating Pull Requests for subsequent changes. Here are the major PRs I've made:

PR #4: [Frontend and Smart Contract Updates for Encrypted Invoice Handling](https://github.com/StabilityNexus/Chainvoice/pull/4)  

PR #5: [Enhanced Documentation with Deployment Guide for Chainvoice](https://github.com/StabilityNexus/Chainvoice/pull/5)  

PR #6: [Refactored Dashboard, Treasury Management, and Routing Architecture](https://github.com/StabilityNexus/Chainvoice/pull/6)  

PR #7: [Implemented Multi-Token (ERC20) Payment Support and Invoice Cancellation](https://github.com/StabilityNexus/Chainvoice/pull/7)  

PR #8: [Introduced Pre-Filled Invoice Links for Seamless Invoice Creation](https://github.com/StabilityNexus/Chainvoice/pull/8)  

PR #9: [Enhanced User Experience with Advanced Token Selection Interface](https://github.com/StabilityNexus/Chainvoice/pull/9)  

PR #10: [Batch Invoice Processing for Efficient Payment Handling](https://github.com/StabilityNexus/Chainvoice/pull/9)

## Challenges and Solutions
### 1. Encryption Implementation Complexity
#### Problem: Integrating Lit Protocol's decentralized encryption while maintaining seamless user experience was challenging due to complex wallet signature requirements and access control conditions.
#### Solution:
- Implemented hybrid encryption using AES-256 symmetric keys with Lit Protocol's identity-based encryption
- Created automated encryption/decryption workflows triggered by wallet connections
- Streamlined smart contracts to handle only encrypted data, removing sensitive plaintext fields

### 2. User Experience for Complex Workflows

#### Problem: Blockchain interactions and encryption processes created friction in the invoice creation and payment flows.
#### Solution:
- Developed pre-filled invoice links eliminating manual address entry
- Added comprehensive loading states and error handling
- Implemented step-by-step guidance with real-time validation feedback
- Created intuitive token selection interface with search and filtering capabilities

## Future Plans
- Implement notification mechanism using Push Protocol or Waku for wallet-native alerts
- Develop automated overdue invoice handling with status updates and penalty enforcement
- Implement alert system for upcoming due dates and payment reminders
- Build mobile app integration for real-time push notifications
- Enhance analytics dashboard with overdue invoice metrics
- Add moderation and escalation workflows for dispute resolution
- Optimize gas usage further for batch processes and automated tasks

## Acknowledgments
This project was completed under the mentorship of [Dr. Bruno Woltzenlogel Paleo](https://www.linkedin.com/in/brunowp/), [Aditya Bhattad](https://www.linkedin.com/in/adityabhattad/) and the [AOSSIE](https://aossie.org/) team as part of Google Summer of Code 2025.

I express my sincere gratitude to my mentors at AOSSIE, who provided continuous guidance and valuable feedback throughout my GSoC journey. Their support was instrumental in successfully implementing the privacy-enhanced invoicing system and creating a comprehensive Web3 payment solution.

Thank you.