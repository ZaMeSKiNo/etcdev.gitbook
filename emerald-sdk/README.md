---
description: >-
  The Emerald SDK is a set of development tools that help developers create
  decentralized applications (DApps) on Ethereum Classic.
---

# Emerald SDK

![](../.gitbook/assets/emerald_sdk_green.jpg)

## The DApp Development Environment 

In software development, an application is built in a testing environment before the production version is deployed. A testing environment allows developers to review the design, usability, and security of an application before deployment. This is true when building DApps and arguably more so due to the immutability of a decentralized public blockchain.

When a critical bug is discovered on a traditional application, it is possible for an admin \(or hacker\) to completely remove the application until further notice. However, on a decentralized public blockchain, mistakes cannot be _magically_ forgotten. This high-assurance is why DApp developers need their own testing environment with all the tools they’d expect on the main-net. So what tools does a DApp developer need for end-to-end development?

### Overview of a DApp Tool Set

1. **Interface**: The front-end a user interacts with the DApp.
2. **Test-net**: A personal Ethereum Classic test-net to develop against with the usual blockchain suspects; blocks, hashes, test-net accounts, etc…
3. **Wallet**: A wallet to create and sign transactions on the DApp.
4. **Block-explorer**: A personal block explorer to explore blocks on a test-net.
5. **Smart Contract Testing and Deployment**: Tool to compile, test, and deploy the DApp on a given network.

There are many tools available to developers such as ReMix to compile contracts, and MetaMask to interact with test contracts. However these tools do not work together, and do not provide a simple build chain to create a whole app. Presently everything is very piecemeal. The Emerald SDK encapsulate this workflow to make DApp development easier...

### Overview of Emerald SDK Tool Set

1. **Emerald-JS-UI** & **Emerald-JS**: Highly reusable and customizable React library that connects to the blockchain \(test-net or main-net\) through the Emerald-JS RPC API.
2. **Emerald TestRPC**: Light weight test-net \(based on SputnikVM-Dev\)supporting all the opcodes as the main-net. Generates blocks, test accounts, and the usual subjects you’d expect on the main-net to develop upon.
3. **Emerald Wallet**: An Ethereum Classic wallet that can toggle between network nodes \(test-net or main-net\) allowing developers to sign and send transaction for their DApps.
4. **Emerald Explorer**: A blockchain explorer that can toggle between networks. Developers can use the explorer to explore transaction 
5. **Emerald-CLI**: _The Swiss Army Knife_ of the Emerald SDK, encapsulating the testRPC, wallet, explorer, and new project generation in one CLI with smart contract testing and deployment capabilities.

