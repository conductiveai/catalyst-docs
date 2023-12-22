---
title: How to Set Up Your First Contest
route: /contest-setup
tags: ['walkthrough', 'engagement', 'contest', 'setup']
layout: default
order: 7
date: 2023-11-16
---

### Conductive Button

Use the **SceneToShowButton** field to set where the Conductive Button appears in your game. We recommend showing the button in a lobby screen or main menu.

The Conductive Button, which will be featured in-game, is part of the `CatalystSDK.prefab`. Out of the box, it will feature an image, along with a countdown clock that indicates when your active contest will end. The button also supports badges that notify players when a contest ends and if they won a prize for the contest period. If your team has suggestions on notifications that can better inform your players about the contest status or rewards, please get in touch with Conductive.ai. We are constantly making improvements to Conductive Catalyst SDK, and your feedback is valuable.

We understand that resolutions and formats need to be adjusted on a per-game basis, so the button has its own canvas. While properties like resolution and size can be adjusted, we recommend keeping other elements unchanged, as a static button with no countdown might result in lower engagement or a confused player base.

### Player Engagement Mechanics

**Funding the Master Wallet**

**Stablecoins Supported:**

- USDC & USDT (ERC-20)
- USDC & USDT (Polygon)
- USDT (BNB)

**Purpose:** These stablecoins can be utilized as rewards.

### Catalyst Account:

**Purpose:** This account is crucial for processing on-network operations.

**Scenario 1: Deposit ETH in preparation for creating a contest on the Ethereum network.**

ETH will be used to cover any gas fees associated with transactions such as sending stablecoin rewards directly to players.

### Buying ETH on a centralized cryptocurrency exchange:

- Start by visiting a centralized cryptocurrency exchange, such as [Coinbase](https://www.coinbase.com/), and creating an account.
- Follow the exchange's step-by-step instructions for buying ETH. [Here is Coinbase's walkthrough.](https://www.coinbase.com/how-to-buy/ethereum)
- When the purchase is complete, you will see your ETH balance in your Coinbase Wallet Balance.

### Obtaining your Catalyst Account wallet address:

- Visit the Catalyst Dashboard.
- In the upper right, click on **Fund Project**.
- Copy your wallet address, which is a string of alphanumeric characters starting with **0x**.
- Set this wallet address aside. You will need it when you withdraw ETH from your cryptocurrency exchange.

### Sending ETH to your Catalyst Account Master Wallet:

- Sign in to your centralized cryptocurrency exchange of choice. In this example, we'll proceed with the assumption that you are using [Coinbase](https://www.coinbase.com/).
- Click the Trading tab.
- Under Wallet Balance, select Withdraw.
- Search for ETH.
- Choose the withdrawal method: in the **To** field, enter your Catalyst Account Master wallet address.
    - Confirm you're withdrawing ETH into the correct address.
- Enter the amount of ETH you'd like to send to your Catalyst Account Master Wallet.
    - You may need to enter two-step verification before completing the withdrawal.
- Note that you will need to reserve a small amount of ETH to pay network fees (also called gas fees) for the withdrawal.

**Scenario 2: Deposit MATIC in preparation for creating a contest on the Polygon network.**

MATIC will be used to cover any gas fees associated with transactions such as sending stablecoin rewards directly to players.

### Buying MATIC on a centralized cryptocurrency exchange:

- Start by visiting a centralized cryptocurrency exchange, such as [Coinbase](https://www.coinbase.com/), and creating an account.
- Follow the exchange's step-by-step instructions for buying MATIC. [Here is Coinbase's walkthrough.](https://www.coinbase.com/how-to-buy/polygon)
- When the purchase is complete, you will see your MATIC balance in your Coinbase Wallet Balance.

### Obtaining your Catalyst Account wallet address:

- Visit the Catalyst Dashboard.
- In the upper right, click on **Fund Project**.
- Copy your wallet address, which is a string of alphanumeric characters starting with **0x**.
- Set this wallet address aside. You will need it when you withdraw MATIC from your cryptocurrency exchange.

### Sending MATIC to your Catalyst Account Master Wallet:

- Sign in to your centralized cryptocurrency exchange of choice. In this example, we'll proceed with the assumption that you are using [Coinbase](https://www.coinbase.com/).
- Click the Trading tab.
- Under Wallet Balance, select Withdraw.
- Search for MATIC.
- Choose the withdrawal method: in the **To** field, enter your Catalyst Account Master wallet address.
    - Confirm you're withdrawing MATIC into the correct address.
- Enter the amount of MATIC you'd like to send to your Catalyst Account Master Wallet.
    - You may need to enter two-step verification before completing the withdrawal.
- Note that you will need to reserve a small amount of MATIC to pay network fees (also called gas fees) for the withdrawal.

**Creating a Reward Group:**

**Objective:** Set up a reward pool or distribution group for specific players or activities.

**Procedure:** Send your desired amount of ERC-20 tokens (such as USDC or USDT) to the designated reward group address or through the specified platform interface.

***Note:** Before transferring any funds, always ensure that you’re using the correct and official addresses or methods to prevent any loss of assets. All gas fees will be paid for by the developer from the Master Wallet.*

### Setting up and customizing reward groups and rewards

Upon registering on the Conductive.ai platform, it is crucial to set up and personalize your reward groups and the rewards.

This entails defining various reward categories, which include leaderboards and quests.

To create a leaderboard, you will have to set up the ranks and define the prizes that players will receive when they achieve those ranks.

Here’s how to setup a leaderboard:

1. Give Conductive.ai a leaderboard API endpoint
2. 2. Speak with a Conductive.ai representative to share the value you want to track that determine ordinal placement.
3. Tell Conductive.ai how we can retrieve user data from your leaderboard data, and the timestamp
4. This will allow us to configure your unique leaderboard for Conductive.ai services


### Implementing and managing contests and leaderboards

To foster a competitive spirit and maintain high engagement levels, Conductive.ai offers integrated tools for implementing and managing contests and leaderboards developed by the game developer with ease. Conductive.ai can read a game's leaderboard and extract data to prove winners and give those winners rewards.

Developers have the flexibility to set up periodic contests linked to an in-game leaderboard.  These features track player performances and rankings. The management process is iterative, requiring updates based on player feedback. The aim is to ensure fairness and make necessary adjustments over time to sustain a lively and engaging gaming atmosphere.

### Catalyst Dashboard

From the Catalyst Dashboard, developers will be able to carry out a wide range of actions to enhance the gaming experience and foster greater player engagement.

Here’s a breakdown of the functionalities available:

- **Create Contests:** Set up competitive events to spur engagement and retain players.
- **Display Contests**: Showcase ongoing contests vividly to engage players effectively.
- **Delete Contests:** Remove contests that are outdated or irrelevant to maintain a streamlined player experience.
- **Update Scheduled Contests**: Modify scheduled contests to adapt to changing dynamics or improve engagement. You cannot modify or update a contest after it has gone live.
- **Create Reward Groups:** Establish groups with specified rewards to encourage certain player behaviors.
- **Display Reward Groups:** Illustrate reward groups prominently to keep players informed and motivated.
- **Delete Reward Groups:** Withdraw reward groups that are no longer beneficial or pertinent.
- **Update Reward Groups:** Revise reward groups to keep them fresh, relevant, and aligned with your game’s goals.
    - Name your reward group (example: Contest #4 Winners!)
    - Reward Amount
    - Range (i.e: 1–10 = top ten players on leaderboard will split the reward for the contest)
- **Set Withdraw Limit:** Configure the minimum amount of token rewards a user must accumulate before they can transfer rewards to their wallet.
- **Fund Master Wallet:** Ensure a seamless reward distribution process by managing financial resources effectively.

Through the Conductive.ai dashboard, developers have a centralized hub to manage and optimize the reward systems effectively, encouraging a thriving gaming community centered around continuous engagement and rich rewards. This set of tools is crafted to facilitate not just the creation and management of contests and rewards, but also to visualize and analyze data essential in iterating a successful game development strategy. It is the linchpin in creating a vibrant and responsive gaming ecosystem, enabling a deeper connection between the game and its community.

**Understanding reward transactions and withdrawal thresholds**

An essential aspect of managing the Conductive.ai platform is understanding the dynamics of reward transactions and establishing reasonable withdrawal thresholds. This involves setting a minimum limit of accumulated rewards that players must reach before initiating a withdrawal. These thresholds can be adjusted at any time.

By having a deep understanding of this, you can maintain a healthy ecosystem where players feel rewarded appropriately while preserving the economic balance of the rewards system. Establishing and communicating these thresholds clearly helps in fostering a transparent and trustful environment, encouraging players to engage more and aim higher in their gaming pursuits.