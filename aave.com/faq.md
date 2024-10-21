# FAQ

# General

## What is Aave?
Aave is a decentralised non-custodial liquidity protocol where users can participate as suppliers or borrowers. Suppliers provide liquidity to the market while earning interest, and borrowers can access liquidity by providing collateral that exceeds the borrowed amount.

## How do I interact with Aave?
Aave is a decentralised, non-custodial liquidity protocol that is completely permissionless, meaning anyone can access it. Users can interact with Aave through a user-friendly interface or directly with its smart contracts on supported blockchain networks. This openness also enables the creation of third-party services or applications that integrate with the protocol.
To interact with the Aave Protocol, simply connect your crypto wallet and supply your preferred asset and amount. Once supplied, you'll earn passive income based on market borrowing demand. Additionally, your supplied assets can be used as collateral, enabling you to borrow other assets.

## Do I need a wallet to interact with Aave?
Yes, you need a wallet to interact with Aave. Each instance of the Aave Protocol is deployed to a blockchain network. To interact with Aave, you need a wallet on the corresponding network such as a hardware wallet, browser extension, mobile wallet, multi-signature wallets, among others.
When interacting with an Aave Protocol interface, wallets are connected using methods such as mobile wallets (Family), browser wallets (MetaMask, Rabby, etc.), WalletConnect, and more. These connection methods are utilized to prompt for messages and transactions to be signed in the connected wallet.

## What is the cost of interacting with Aave?
Interacting with the Aave Protocol requires transactions on Ethereum or other blockchain networks where Aave is deployed. These transactions may incur gas fees, which are non-refundable network transaction fees determined by the network status and transaction complexity.
Transaction costs are typically highest on Ethereum, and significantly cheaper on all other networks, which can be compared [here](https://www.growthepie.xyz/fundamentals/transaction-costs). The connected wallet will ask you to confirm the gas fee when signing a transaction.

## How can I access Aave?
There are multiple interfaces available to access the Aave Protocol. Below are just a few examples:
[Aave Labs Interface](https://app.aave.com/)
All functionalities + leverage and auto liquidation (repayment with collateral) through [DeFi Saver](https://app.defisaver.com/aave).
Flash Loans, supply and withdrawal from [Furucombo](https://furucombo.app/) interface.
Supply and withdraw from [Argent wallet](https://www.argent.xyz/).
Manage positions via smart account with [Brahma Console](https://console.brahma.fi/).
Asset management with [Fireblocks](https://www.fireblocks.com/).
All actions are available directly through protocol smart contracts, which can be accessed through block explorers or code by following the guidelines available in the [docs](https://aave.com/docs).
Be careful. Aave never advertises on any social media platform or search engine and does not have any downloadable mobile application available. If you find one, it is a scam. Aave Protocol will never ask for your wallet seed phrase.

## How can I try out Aave without using actual funds?
You can use Aave in a simulation environment designed for testing and development. In this environment, the assets are not real and have no economic value.
Go to the [Aave Labs Interface](https://app.aave.com/), select the settings button on the top right corner, enable testnet view.
Switch to the testnet you wish to utilize over your wallet provider.
Make sure to have the native asset for the specific network.
Get some tokens from the test client faucet.

## Can funds be frozen?
No central entity, including Aave Labs or any individual contributor, has the authority or ability to freeze or alter individual user positions within the Aave ecosystem. The Aave Protocol is fully decentralized and governed by the Aave Decentralized Autonomous Organization (DAO), which is controlled by AAVE token holders. As such, users maintain complete self-custody of their funds, and there is no mechanism for freezing or modifying individual positions by any entity.
Risk Management Controls: While individual positions are untouchable, the protocol includes specific risk management functions designed to safeguard the overall system. These functions are strictly limited to broader protocol actions and do not extend to individual user positions:
1. PoolAdmin Role: In Aave V2, the PoolAdmin can only pause all interactions within the entire pool of assets.
2. EmergencyAdmin Role: In Aave V3, the EmergencyAdmin role — currently held by the Aave Guardian — can pause specific reserves for purposes of risk management. However, even this action is limited to the reserve level and does not allow for freezing or altering individual positions. These roles are designed to protect the integrity of the protocol as a whole and do not have the capability to interfere with or directly manage individual user funds. For detailed information on these roles and their specific limitations, please refer to the [Aave Permissions Book](https://github.com/bgd-labs/aave-permissions-book) and the [governance forum](https://governance.aave.com/).

## Why do I need to approve tokens?
Approving tokens is a necessary step when performing actions that involve transferring tokens to a smart contract, such as supplying and repaying tokens to the Aave Protocol. If a token approval is required, frontends such as the [Aave Labs interface](https://app.aave.com/) will prompt users to perform the approval with one of the following methods:
Transaction: a transaction is an onchain action that requires gas fees and time to confirm. You will be prompted to approve/pay for the gas fee to facilitate the transaction.
Signature: when a signature approval is required to transfer tokens, you will be prompted to sign a message with the same wallet making the transaction. Message signing is free and instant, however, it is only available for certain tokens ( [EIP-2612](https://medium.com/noncept/understanding-eip-2612-and-erc20-permit-43ce8b829bd5) compatible), and wallet types (private key wallets).

# Risk

## What are the risks involved in using Aave?
No protocol can be considered entirely risk free, but extensive steps have been taken to minimize these risks as much as possible – the Aave Protocol code is publicly available and auditable by anyone, and has been audited by multiple [smart contract auditors](https://aave.com/security). Any code changes must be executed through the onchain governance processes. Additionally, there is an ongoing [bug bounty campaign](https://immunefi.com/bounty/aave) and service providers specializing in technical reviews and risk mitigation. It is recommended to use or migrate to the latest version of the protocol (Aave V3) due to the introduction of granular risk parameters such as supply caps, borrow caps, and isolated collateral assets.
Different risk categories are explained in detail below. You can find additional risk and security related information in the [risk framework](https://aave.com/docs/concepts/risks) and [security and audits](https://aave.com/security) sections.
Smart Contract Risk
Smart contract risk involves the potential for bugs or vulnerabilities within the Aave Protocol code or the underlying reserve tokens.
Oracle Risk
Oracle risk arises from the reliance on third-party data providers for price feeds and other external data such as redemption ratio for liquid staking tokens. If an oracle fails or is compromised, it could lead to incorrect valuations of assets.
Collateral Risk
Collateral risk pertains to the value and stability of assets used as collateral. The inability to liquidate collateral due to rapid decrease in value or insufficient external liquidity can result in bad debt.
Network / Bridge Risk
Network or bridge risk involves the potential issues related to the underlying blockchain networks and bridges upon which the Aave Protocol operates. These risks include congestion, censorship, or security vulnerabilities.

## What steps are taken to mitigate risks?
Smart Contract Risk
To mitigate smart contract risks, the Aave Protocol code is publicly available and has been audited by multiple [smart contract auditors](https://aave.com/security). Aave employs onchain governance, which validates that any changes to the protocol are thoroughly vetted and approved by the community. Additionally, service providers contribute their expertise to identify and mitigate potential risks. The protocol also runs an ongoing bug bounty program that encourages external developers to find and report vulnerabilities.

Oracle Risk
Aave mitigates oracle risks by using decentralised oracles such as Chainlink to provide reliable and tamper-resistant price and redemption ratio feeds.

Collateral Risk
To address collateral risks, the Aave DAO engages risk service providers who continuously monitor the collateral assets and market conditions to provide insights and adjustments. The protocol sets risk parameters such as loan-to-value (LTV) and liquidation thresholds to promote the maintenance of overcollateralized borrow positions. Onchain governance allows the community to adjust these risk parameters as needed to respond to changing market conditions, further safeguarding the protocol.

Network / Bridge Risk
Aave Governance has adopted a robust [network onboarding framework](https://governance.aave.com/t/bgd-aave-v3-deployments-technical-evaluation-framework-of-a-network/10237) to thoroughly vet new networks and bridges before integration. Onchain governance oversees decisions related to network and bridge integrations, ensuring community participation and scrutiny. This comprehensive approach helps to mitigate network and bridge risks, enhancing the security and reliability of the Aave Protocol.

# Supplying & Earning

## How do I supply?
Browse to the "Supply" section and click on "Supply" for the asset you want to supply. Select the amount you'd like to supply and submit your transaction. Once the transaction is confirmed, your supply is successfully registered and you begin earning interest.
Transferring tokens on an Ethereum based network requires a token approval from your self-custodial wallet. This must be performed with a transaction or signed message prior to the supply.

## How much can I earn?
Suppliers receive continuous earnings that evolve with market conditions based on:
The interest rate payment on borrow positions: Suppliers share the interests paid by borrowers corresponding to the average borrow rate times the utilization rate. The higher the utilization of a reserve, the higher the yield for suppliers.
Flash Loan fees: Suppliers receive a share of the Flash Loan fees corresponding to 0.09% of the Flash Loan volume.
You can find the current supply rate for each token in the Markets tab of the [Aave Labs Interface](https://app.aave.com/markets). Historic rates can be viewed by clicking on individual tokens to view their corresponding reserve details page.

## Are there limitations to supply?
There is no minimum amount to supply.
However, assets on Aave V3 markets may have a supply cap parameter which limits the total amount that can be supplied of a particular asset.

## Where are supplied tokens stored?
Supplied tokens are stored in publicly accessible smart contracts that enable overcollateralised borrowing according to governance-approved parameters. The Aave Protocol smart contracts have been audited and formally verified by third parties.

## How do I withdraw?
Withdrawing from the Aave Protocol occurs on the Pool smart contract. Withdrawal transactions can be performed through the [Aave Labs Interface](https://app.aave.com/) by navigating to the "Dashboard" section and clicking “Withdraw.” Select the amount to withdraw and submit the transaction.
You need to make sure there is enough liquidity (not borrowed) in order to withdraw, if this is not the case, you need to wait for more liquidity from suppliers or borrowers repaying.
Additionally, the [Aave Labs Interface](https://app.aave.com/) has a “Withdraw & Switch” feature to enable withdrawing into other tokens.

## Can I opt-out of my asset being used as a collateral?
Yes. After supplying your assets, you are able to unselect the asset so that it will not be used as collateral. The opt-out is available in the "Supply" section within your dashboard. Simply switch the "use as collateral" button on the asset you would prefer to opt-out from being used as a collateral.
You can withdraw your assets without opting out of using them as collateral, as long as those funds are not actively being used to borrow and provided the withdrawal amount would not cause a liquidation on your borrow positions.

# Borrowing

## How do I borrow?
Before borrowing you need to supply approved asset to be used as collateral (check out the Supplying & Earning FAQ section for more info). After this, you can execute a borrow from the Aave smart contracts or a user interface. On the [Aave Labs Interface](https://app.aave.com/), head to the Borrow section and click on “Borrow” for the asset you want to borrow. Adjust the amount you need based on the available collateral balance, and confirm the transaction in your wallet.

## How much can I borrow?
The maximum amount you can borrow depends on the value you have supplied, the available liquidity, and the asset borrow cap. For example, you can’t borrow an asset if there is not enough liquidity or if your health factor doesn’t allow you to. You can find all collateral available and their specific borrow parameters in the [risk parameters dashboard](https://aave.com/docs/resources/parameters).

## Why would I borrow instead of selling my assets?
Selling your assets means closing your position on that particular asset. Hence, if you are long on the asset, you would not be entitled to the potential upside value gain. By borrowing you are able to obtain liquidity (working capital) without selling your assets. Users are mainly borrowing for unexpected expenses, leveraging their holdings or for new investment opportunities.

## How do I repay my borrow position?
Borrow positions can be repaid through Aave smart contracts or a user interface. On the [Aave Labs Interface](https://app.aave.com/), go to the Borrowings section of your dashboard and click on the "Repay" button for the asset you borrowed and want to repay. Select the amount to repay and confirm the transaction.
You repay your borrow position in the same asset you borrowed. For example, if you borrow 1 GHO you will pay back 1 GHO + interest accrued. The [Aave Labs Interface](https://app.aave.com/) also integrates a repay with collateral feature, which uses flashloans and DEX integrations to allow borrow positions to be repaid with aTokens.

## How much would I pay in interest?
The interest rate you pay for borrowing assets depends on the supply and demand ratio of the asset and interest rate curve parameters determined by Aave Governance.
You can find the current borrow rate for each borrowable token in the Markets tab of the [Aave Labs Interface](https://app.aave.com/markets). Historic rates can be viewed by clicking on individual tokens to view their corresponding reserve details page.

## When do I need to pay back the borrow position?
There is no fixed time period to pay back the borrow position. As long as your position is properly collateralised, you can borrow for an undefined period. However, as time passes, the accrued interest will grow making your health factor decrease, which might result in your supplied assets becoming more likely to be liquidated.

# Liquidations

## What is Health Factor?
Health factor is the numeric representation of the safety of a borrow position, calculated as:
Total Collateral Value * Weighted Average Liquidation Threshold / Total Borrow Value
Liquidation Threshold is a parameter determined by Aave Governance for each collateral asset, which is the maximum percentage of value that can be borrowed against a collateral asset. A health factor below 1 represents a borrow position that is eligible for liquidation.
For example, if you supply $10,000 in ETH with an 80% threshold and borrow $6,000 in USDC, your health factor = 10000 * 0.8 / 6000 = 1.333.

## What happens when my health factor is reduced?
Depending on the value fluctuation of your supplies, the health factor will increase or decrease. If your health factor increases, it will improve your borrow position by making the liquidation threshold more unlikely to be reached. In the case that the value of your collateralised assets against the borrowed assets decreases, your health factor is also reduced, resulting in increased liquidation risk.

## What are liquidations?
A liquidation is a process that occurs when a borrower's health factor goes below 1 because their collateral value does not properly cover their borrow value. This can happen when the collateral value decreases and /or when the borrow position value increases beyond the liquidation threshold of the collateral assets.
In a liquidation, up to 50% of a borrower's debt is repaid and that value + the liquidation fee is taken from the collateral available, so after a liquidation that amount liquidated from your borrow position is repaid.
Liquidations are a permissionless feature of the Aave Protocol. If a borrow position has insufficient collateral to cover the liquidation threshold, then any address on the network is able to initiate a liquidation transaction.

## How much is the liquidation penalty?
The liquidation penalty (or bonus for liquidators) depends on the asset used as collateral. You can find every asset's liquidation fee in the [risk parameters dashboard](https://aave.com/docs/resources/parameters).

## Can you give an example of liquidation?
Example 1
Bob supplies 10 ETH and borrows 5 ETH worth of GHO. If Bob’s Health Factor drops below 1 his borrow position will be eligible for liquidation. A liquidator can repay up to 50% of a single borrowed amount = 2.5 ETH worth of GHO. In return, the liquidator can claim a single collateral which is ETH (5% bonus).

The liquidator claims 2.5 + 0.125 ETH for repaying 2.5 ETH worth of GHO.

Example 2
Bob supplies 5 ETH and 4 ETH worth of YFI, and borrows 5 ETH worth of GHO. If Bob’s Health Factor drops below 1 his borrow position will be eligible for liquidation. A liquidator can repay up to 50% of a single borrowed amount = 2.5 ETH worth of GHO. In return, the liquidator can claim a single collateral, as the liquidation bonus is higher for YFI (15%) than ETH (5%) the liquidator chooses to claim YFI.

The liquidator claims 2.5 + 0.375 ETH worth of YFI for repaying 2.5 ETH worth of GHO.

What is a good Health Factor?
Health Factor represents the ratio of collateral to borrow value. There is not an exact answer as to what constitutes a "safe" health factor as it depends on the volatility and correlation of collateral and borrow asset prices.
Each collateral and borrow asset has a corresponding oracle that reports the price of the token with respect to a base currency (typically USD). In general, if the collateral and borrow assets are highly correlated with respect to the base currency (such as supplying and borrowing only stablecoins or ETH-correlated assets), a lower health factor can be considered safe compared to a position where assets are not correlated.
[Simulation tools](https://defisim.xyz/) can be used to estimate the effects of price movements and accrued interest on health factor.

## What is my liquidation price?
The liquidation price of an account is a point at which the balances and oracle prices of the collateral and borrow positions results in a health factor < 1.0. Health factor depends on the balances and oracle prices of all collateral and borrow tokens, so liquidation price is not a single point, it is a curve of combinations.
[Simulation tools](https://defisim.xyz/) can be used to estimate the effects of price movements and accrued interest on health factor, and estimate the most likely combinations that can result in liquidation.


## How can I avoid getting liquidated?
To avoid liquidation you can raise your health factor by supplying more collateral assets or repaying part of your borrow position. By default, repayments increase your health factor more than supplies. Also, it's important to monitor your health factor and keep it high to avoid a liquidation. Keeping your health factor over 2, for example, gives you more of a margin to avoid a liquidation.
Tools that can help you with this:
You can simulate Health Factor movements using [DeFi Simulator](https://defisim.xyz/).
You can auto liquidate your borrow position using [DeFi Saver](https://app.defisaver.com/aave).
You should be mindful of stablecoin price fluctuations due to market conditions and how it might affect your Health Factor. For example, the market price of USDC 1.00 might not equal exactly USD 1.00, but USD 0.95, for example. The price fluctuations of stablecoins, like any assets, affects your Health Factor.

# Governance

## What is Aave Governance?
The Aave Protocol is governed by the AAVE token holder community through procedures, voting, and smart contract execution, collectively known as Aave Governance.
All instances of the Aave Protocol are governed by the AAVE, stkAAVE, and aAAVE token holders on Ethereum mainnet.
The [Governance Process](https://aave.com/docs/primitives/governance) guide details the proposal lifecycle from idea to execution, which includes phases for discussion → temp check voting → onchain voting and execution.

## What do I need to vote?
In order to vote you need to have AAVE, stkAAVE (Staked AAVE), or aAAVE (AAVE supplied to Ethereum V3 market) tokens on Ethereum mainnet. Voting power is the sum of token balances and incoming delegations.

## How do I vote?
Voting occurs through Aave Governance smart contracts. There are multiple interfaces that can be used to access voting such as the [Aave Labs](https://app.aave.com/governance), [BGD Labs](https://vote.onaave.com/), and [Tally](https://www.tally.xyz/gov/aave) governance interfaces.

## What is the voting threshold?
The threshold is dynamic and can change based on the quorum + differential of votes for/against an AIP.
If there are very few votes against an AIP, the threshold will remain the same. However, if the votes against the AIP are more substantial, then the threshold can be moved up so there must be more votes in favor for the AIP to pass. This is to validate that an AIP has overwhelming approval before it is implemented.
For example:
If the quorum is 20%, the differential is 15% and 2% of the total votes are against the AIP, the threshold would remain at 20% (because 15+2 = 17 < 20).
If the quorum is 20%, the differential is 15% and 6% of the total votes are against the AIP, then the threshold would be raised to 21% (because 15+6=21), so more "yae" votes would be required for the AIP to pass.

## What is the Aave Treasury?
The Aave Treasury is a smart contract instance on each network where the protocol is deployed, controlled by Aave Governance.
Each borrowable reserve in an Aave market has a parameter called reserve factor, which is the percentage of borrow interest accumulated to the treasury and is determined on a per-asset basis by Aave Governance.

## Is it mandatory to participate in Aave Governance?
Participation in Aave Governance is optional. Users can access the Aave Protocol without participating in governance.

# Safety Module

## What is the Safety Module?
The Aave Safety Module is a mechanism designed to protect the protocol in case of a shortfall event. Users can stake AAVE (stkAAVE), GHO (stkGHO), or AAVE/wstETH liquidity pool tokens (stkABPT) in the Safety Module to act as a backstop, earning rewards in return. This helps to maintain the stability and security of the Aave ecosystem.

## What is staking?
Staking consists of supplying supported tokens within the protocol [Safety Module](https://aave.com/help/safety-module). The purpose of staking is to act as a mitigation tool in case of a shortfall event. As an incentive for this, Safety Module stakers will receive Safety Incentives.

## What is staking?
Staking consists of supplying supported tokens within the protocol [Safety Module](https://aave.com/help/safety-module). The purpose of staking is to act as a mitigation tool in case of a shortfall event. As an incentive for this, Safety Module stakers will receive Safety Incentives.

## What is the risk of staking?
In the case of a shortfall event, Aave Governance can initiate a transaction to utilize Safety Module funds up to the maximum slashing percentage to cover the deficit.
The maximum slashing percentage for each staking token is determined by Aave Governance, currently 33% for stkAAVE / stkABPT and 99% for stkGHO.

## What is the incentive for staking?
Stakers within the Safety Module receive incentives with assets and emission rates determined by Aave Governance.
Current emission rates can be viewed as an annual percentage on the [Aave Labs Interface.](https://app.aave.com/staking/)

## How do I start staking?
Staking can be performed through the [Aave Labs Interface](https://app.aave.com/) Staking section. Over the staking section select 'stake', input the amount to stake and click on 'stake'. Then proceed to send 2 transactions to stake your AAVE:
Approve: This is a required transaction prior to the staking that allows the staking contract to move your AAVE tokens. This transaction won't be required if you perform additional staking actions unless you revoke the approval.
Stake AAVE: This transaction performs the action to stake AAVE tokens. When confirmed, your tokens will be staked in the Safety Module.

## How do I stop staking?
If you want to stop staking, head over to the [Aave Labs Interface](https://app.aave.com/) in the Staking section. Over the staking section select 'Unstake', input the amount and click on 'unstake'.
If you did not activate the cooldown period, you will need to activate it. This consists of 1 transaction to activate the cooldown. When the cooldown period finishes, you will be able to unstake by following the next step.
Unstake AAVE: This transaction performs the action to unstake AAVE tokens. When confirmed, your AAVE tokens will be back in your wallet!
After the cooldown period passes there is a 2-day window to unstake. If you do not unstake during that period you will need to activate the cooldown again.

## What is the cooldown period?
The cooldown period is the time required prior to unstaking your tokens. You must start the cooldown period before you can unstake your tokens. You can start the cooldown period by going to the staking section, select 'unstake' and click on 'activate cooldown'. It will require one transaction to be sent.
The cooldown period is currently 20 days, but could be modified in the future by an Aave Governance proposal.
IMPORTANT: After the cooldown period is complete, you have a 2-day window where you can unstake. If you do not unstake during that period, you will have to start the cooldown process over again.
Example:
If the cooldown period was activated 20 days and 4 hours ago, you can unstake.
If the cooldown period was activated 22 days and 2 hours ago, you can not unstake, and you will need to start the 20-day cooldown period again.

## Can I add stkAAVE or stake more AAVE while in cooldown period?
You can stake more AAVE tokens in the Safety Module or receive stkAAVE, but that would increase your cooldown period based on the amount received. Even if the amount received is big enough, it will reset your cooldown period requiring you to activate it again before you can unstake.

## How do I claim my rewards?
You can claim your rewards at any time on the staking section by clicking on "Claim". The AAVE tokens from the reward will be in your connected wallet as soon as the transaction is confirmed.

# GHO Stablecoin

## What is GHO?
GHO is a decentralised, overcollateralised stablecoin that is fully backed, transparent, and native to the Aave Protocol.
The [GHO Documentation](https://aave.com/docs/developers/gho) is a comprehensive resource that explains the core mechanics of how the GHO stablecoin operates.

## How do I mint GHO?
Borrowers and suppliers can mint GHO using assets they have supplied into V3 as collateral on Ethereum markets, while continuing to earn interests on their underlying assets.

## How do I borrow GHO?
The GHO pool functions differently from existing assets, but borrowing it will work similarly as other available assets on the different markets in the protocol.
Supply Collateral
Borrow GHO
Repay GHO and Accrued Interest (real-time)
Repaid interest will be redirected to the DAO, rather than an asset supplier, contributing to the DAO treasury.

## Which assets can be used as collateral to borrow GHO?
Assets that are available in the Aave Protocol can be used to back GHO. Initially, the Ethereum V3 pool will be the first facilitator to launch because of V3’s extensive risk-mitigation features, including e-mode, isolation mode, and supply caps.

## Who manages the GHO supply?
The Aave DAO manages the supply of GHO, the interest rates and determine risk parameters.

## How does GHO benefit the Aave Treasury?
With 100% of repaid interest being redirected to the DAO, rather than the asset suppliers, these repaid interest contribute to the DAO treasury.

## How is GHO different from the other assets listed on the Aave markets?
Unlike many stablecoins, the oracle price for GHO is fixed. Decentralised stablecoins such as GHO are transparent and cannot be changed. Interest rates are defined by Aave DAO and repaid interest is redirected to the DAO instead of the asset suppliers. Discounts are available to borrowers staking AAVE in the Safety Module.

## Can you explain more about the discount model for GHO?
Users who have staked AAVE tokens in the Safety Module (stkAave) are eligible for a discount on GHO.
For each stkAave there is a discount on the borrowing rate for 100 GHO. The discount model is interchangeable and can be redesigned and replaced if needed by The Aave DAO.

## Is only stkAAVE used for discount or is aBPT eligible?
Currently only stkAAVE holders are eligible for the borrow rate discount.

## Can GHO be flashloaned?
GHO has a Flashmint Facilitator, that functions similarly to flashloan functionality of all other Aave Protocol reserves, and can be used to borrow GHO tokens for use cases requiring liquidity that is borrowed and returned within a single block.

## How can I bridge GHO to other networks?
Aave Governance has the ability to approve GHO facilitators that allow liquidity to be bridged to other networks. A facilitator utilizing Chainlink CCIP has been approved which enables tokens to be bridged to the Arbitrum network.
Bridging can be performed on the [Aave Labs Interface](https://app.aave.com/) by using the “Bridge GHO” feature in the top navigation bar.

# Developers

## How do I integrate Aave functionality?
Aave is a collection of smart contracts deployed to Ethereum and other blockchain networks. Aave functionality can be integrated into an application by interacting with the protocol smart contracts.
[Aave contract documentation](https://aave.com/docs/developers/smart-contracts) contains references for available functions, and the [Aave Utilities JavaScript SDK](https://github.com/aave/aave-utilities) is an example of a commonly used library to integrate into frontend applications.

## How do I query Aave data?
Aave data can be queried directly through view functions. The [Aave Docs](https://aave.com/docs/developers/aave-v3) contain details on available functions, and all protocol addresses can be viewed and integrated through the [Aave Address Book](https://github.com/bgd-labs/aave-address-book/).
Historical data for protocol data such as parameters, rates, balances can be queried through contract events or indexed data sources. A breakdown of all core protocol events can be found [here](https://github.com/aave/protocol-subgraphs/blob/main/templates/v3.subgraph.template.yaml). The [Aave Protocol subgraphs](https://github.com/aave/protocol-subgraphs) are an example of an indexed data source that maps Aave contract events to a GraphQL endpoint.

# Other Features

## What is a Flash Loan?
Flash loans are a feature designed for developers, due to the technical knowledge required to execute one. Flash Loans allow you to borrow any available amount of assets without putting up any collateral, as long as the liquidity is returned to the protocol within one block transaction. To do a Flash Loan, you will need to build a contract that requests a Flash Loan. The contract will then need to execute the instructed steps and pay back the Flash Loan + fee (0.07% in Aave V2, 0.05% in Aave V3) all within the same transaction.
If you would like to develop a Flash Loan smart contract, check out the developer [documentation](https://aave.com/docs/developers/flash-loans).
Aave community developers are also available in the official [Discord](https://aave.com/discord) channel to help with the process.

## Is it possible to use Flash Loans without coding?
Yes, there are tools allowing users to utilize Flash Loans to access liquidity in the background for advanced features such as repay with collateral, collateral switch, and more.
Example interfaces that integrate Flash Loans are the [Aave Labs interface](https://app.aave.com/), [DeFi Saver](https://defisaver.com/), [Instadapp](https://instadapp.io/), and [Furucombo](https://furucombo.app/).

## What is Isolation Mode?
Isolation mode allows Aave Governance to list new assets as isolated assets, which have a specific debt ceiling. Only certain assets can be borrowed in isolation mode—specifically, approved stablecoins. In order for an asset to become approved for borrowing, assets are voted on through Aave Governance process.
The debt ceiling for an isolated asset is represented as the maximum amount in USD that can be borrowed against the user’s collateral with two decimals of precision.
Entering isolation mode is specific to certain isolated assets that are voted on and approved by Aave Governance. You cannot utilize non-isolated assets as collateral to enter isolation mode.

## What is E-Mode?
The E-mode (efficiency mode) feature maximizes capital efficiency when collateral and borrowed assets have correlated prices. For example, DAI, USDC, USDT are all stablecoins pegged to USD. These stablecoins are all within the same E-mode category. Accordingly, a user supplying DAI in E-mode will have higher collateralisation power when borrowing assets like USDC or USDT.
Only assets of the same category (for example stablecoins) can be borrowed in E-mode. E-mode does not restrict the usage of other assets as collateral. Assets outside of the E-mode category can still be supplied as collateral with normal LTV and liquidation parameters.

## Can I move my funds between V2 and V3 markets?
Supply and borrow positions can be migrated between Aave V2 and V3 by using the migration tool, or by manually withdrawing from an Aave V2 markets and supplying to an Aave V3 market.
The migration tool can be accessed through the [Aave Labs Interface](https://app.aave.com/) by navigating to an Aave V2 market, pressing the “Migrate to V3” button next to the market selector, and following the prompts to migrate selected supply and borrow positions.

## How do I switch my supplied asset?
In order to switch your assets you just need to go to the Switch section and follow these steps:
Select the asset you want to switch and the amount in the left side (From).
Select the asset you want to switch to in the right side (From).
Make sure to check the exchange rate and check the slippage. You can edit it based on your preferences. Depending on the slippage, the expected rate might differ and the transaction might even fail if you set it too low. After this click on Continue.
In the next step you will need to send the approval and submit the transaction. The approval transaction will only be required the 1st time you do this step, unless you revoke the approval.
Make sure to have enough ETH for the transaction cost. After sending both transactions your switch will be complete.

## How do I repay with my collateral?
In order to repay with your assets you just need to go to the Dashboard and follow these steps:
1. Click on repay on the debt you want to repay.
2. Choose repay "With your current collateral".
3. Select the asset you want to repay and amount in the left side (Borrowed Asset).
4. Select the asset you want to use to repay to in the right side (Select Collateral).
5. Make sure to check the exchange rate and check the slippage. You can edit it based on your preferences. Depending on the slippage, the expected might differ and the transaction might even fail if you set it too low. After this click on Continue.
6. In the next step you need to send the approval and submit the transaction. The approval transaction will only be required the 1st time you do this step, unless you revoke the approval.
7. Make sure to have enough ETH for the transaction cost. After sending both transactions your repayment will be done.

# Brand

##  How do I use the logo?
The Aave logo should be used in its original form without any modifications. It should be clearly visible and not distorted. The logo should also maintain a minimum clear space around it to ensure it stands out.

## Can I use Aave brand elements for my own project?
You can use the Aave logo on your website or promotional materials, provided your usage doesn't misrepresent the Aave brand. Visual assets should not be altered, combined with other logos, or used in a way that misrepresents the Aave brand.

## Can I create my own assets using the Aave brand elements?
Yes, we encourage you to stay true to the Aave brand while creating your own assets. Start with one of the derivative logos.
