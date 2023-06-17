# **ERC20**

📜 The `ERC20` standard, also known as "Ethereum Request for Comment 20", is a smart contract standard used on the Ethereum blockchain to create digital tokens(fungible tokens). This standard defines a common interface that enables different tokens to be compatible and interact seamlessly with wallets, exchanges and other smart contracts.


🔧 To facilitate the creation of ERC20 contracts, the OpenZeppelin library provides a set of ready-to-use, secure contracts. It is very popular in the Ethereum ecosystem due to its robustness and quality. Here's how to install it in your project:

```console
$ npm install @openzeppelin/contracts
```

🌐 Here's a simple example of an ERC20 contract using the OpenZeppelin library:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Seth is ERC20 {
    constructor(uint256 initialSupply) ERC20("Seth", "STH") {
        _mint(msg.sender, initialSupply);
    }
}
```

This example creates an ERC20 contract named "SethToken" with the symbol "STK". initialSupply is a parameter in the constructor function of the SethToken contract. It represents the initial quantity of STH (Seth) tokens that will be created when the contract is deployed.


`Now let's talk about IERC20`.

📜 **IERC20** is an interface that defines standard functions for ERC20 contracts. It represents the base contract that other ERC20 contracts must implement to comply with the standard.

[ERC20 GitHub link ](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.0.0/contracts/token/ERC20/ERC20.sol)

🔀 **ERC20**, meanwhile, is a standard that specifies the rules and expected behaviors of tokens on the Ethereum blockchain. It's a set of rules for smart contracts that enable the creation, management and exchange of digital tokens.

[ERC20 interface GitHub link ](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.0.0/contracts/token/ERC20/IERC20.sol)

>💡 Use IERC20 when you want to create a contract that interacts with other ERC20 contracts in a standardized way. You don't need to reinvent the functions, but you do need to provide your own implementations for each function defined in the interface.

>⚙️ ERC20, on the other hand, is used when creating a new ERC20 contract. You must implement the IERC20 interface functions in your own ERC20 contract to ensure compliance with the standard and interoperability with other contracts and applications.


🌟 Using IERC20, you can easily integrate token management functionality into your contract, while implementing ERC20 allows you to create a new ERC20 token compatible with the existing ecosystem.

Feel free to use them according to your specific needs in developing smart contracts on the Ethereum blockchain.

[For more information](https://docs.openzeppelin.com/contracts/4.x/)

🌟 ERC20 can be used in application projects aimed at solving real-world problems. Here are three examples:

### 🏥 Health
>1️⃣ **`Rewards for healthy behavior`**: Health applications can use ERC20 tokens to encourage healthy behavior. For example, users can receive tokens in exchange for achieving fitness goals or adopting healthy lifestyles. These tokens can be exchanged for rewards, such as health products, services or discounts, creating positive incentives to improve individuals' overall health.

<br>

### 🌱 Agriculture:
>2️⃣ **`Incentives for sustainable agriculture`**: Farmers who adopt sustainable agricultural practices can be rewarded with ERC20 tokens. These tokens can be exchanged for benefits such as subsidies, farm equipment, or additional training. By creating economic incentives, this encourages farmers to adopt environmentally friendly methods, thus preserving natural resources and reducing the environmental impact of agriculture.

<br>

### 🌍 Fighting global warming :
>3️⃣ **`Financing climate projects`**: ERC20 tokens can be used to finance projects linked to the fight against global warming. Tokens representing stakes in renewable energy, carbon capture and storage, or climate change adaptation projects can be issued. Investors can purchase these tokens to financially support these projects and contribute to the transition to a low-carbon economy.


These examples demonstrate how the ERC20 standard can be used in innovative ways to solve problems in healthcare, agriculture, and the fight against global warming.


🌟 Thanks to the **`ERC20`** standard and the **`IERC20`** interface, it becomes possible to create innovative solutions in various sectors, offering interoperability and ease of use for digital tokens on Ethereum.

>We plan to add other standards commonly used in the ecosystem for token management. 🔄🔜📊

[🔙](https://github.com/orgs/ChainShareLabs/repositories)