## Overview:
Our project endeavors to harness the potential of Stacks DeFi by simplifying the process of automatically compounding DIKO rewards into additional LP tokens within the Arkadiko protocol. By removing the need for manual intervention, users can optimize their yield effortlessly.

## Functionality:
To utilize our platform, users first deploy the smart contracts to their wallets and deposit STX-USDA LP tokens into the pool. Upon calling the "compound" function, the smart contracts execute a series of automated actions:

Claim all pending DIKO rewards.
Swap 50% of DIKO rewards to USDA.
Swap the remaining 50% of DIKO rewards to STX.
Obtain STX-USDA LP tokens from the swap.
Stake the new LP tokens back into the pool.

## Improvement Ideas:
Currently, each wallet requires its own deployed contract, leading to higher gas fees and less-than-ideal user experience. We aim to enhance our platform by implementing the following improvements:

Enable a single contract to serve multiple users, allowing for shared deposits and reducing gas fees.
Allow the compound function to be callable by any user.
Introduce a strategist fee, enabling the strategist to earn a percentage of DIKO rewards during each compound action.
Implement a feature allowing the strategist to pause deposits (while still allowing withdrawals) for emergency situations.
Inspiration:
We took inspiration from successful projects like Harvest Finance, which streamline yield optimization through intuitive interfaces. Recognizing the absence of similar offerings in the Stacks ecosystem, we set out to create a comparable experience tailored specifically to Arkadiko.

## Development Process:
Our platform was built using Clarity smart contracts and a user-friendly React web interface developed with Next.js. The clarity folder contains the backend logic implemented in smart contracts, while the app folder hosts the web interface for user interaction.

## Challenges Faced:
A significant challenge we encountered was the inability to conduct local testing due to our reliance on Arkadiko contracts. This necessitated deploying contracts on the mainnet and testing changes, resulting in a lengthier development process.

## Accomplishments:
Despite the challenges, we successfully implemented the contract, enabling users to deploy it and execute LP token compounding with ease within the USDA-STX Arkadiko pool.

## Key Learnings:
Our journey highlighted the composability of DeFi. Rather than relying on external APIs, we crafted our own logic and seamlessly integrated contracts from other projects, deepening our understanding of decentralized finance.

## Next Steps:
Moving forward, we plan to adapt the contract to serve multiple users, improve the user experience, expand to other Arkadiko pools, introduce strategist fees on DIKO rewards, and explore similar implementations in other DeFi projects such as Alex and Stackswap.