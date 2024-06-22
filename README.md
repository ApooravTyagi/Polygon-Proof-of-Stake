# Polygon-Proof-of-Stake

This repository contains scripts and smart contracts to facilitate the creation, minting, and transfer of an NFT collection using DALLE 2 or Midjourney, stored on IPFS via pinata.cloud. The collection will be deployed on the Goerli Ethereum Testnet as ERC721 or ERC1155 tokens. Additionally, there are scripts to batch mint NFTs, transfer them to the Polygon Mumbai network using the FxPortal Bridge, and verify their presence on Polygon.

### Setup Instructions

1. **Clone Repository**
   ```
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Dependencies**
   ```
   npm install
   ```

3. **Environment Variables**
   - Create a `.env` file based on `.env.example` and fill in the required variables.

4. **Configure Pinata**
   - Sign up on [Pinata](https://pinata.cloud/) and get your API keys.
   - Update `.env` with your Pinata API keys.

5. **Deploy Smart Contract**
   - Use Hardhat to deploy the smart contract to  Ethereum Testnet.
   ```
   npx hardhat run scripts/deploy.js --network 
   ```

6. **Mint NFTs**
   - Modify `scripts/mint.js` to include your specific image generation logic (using DALLE 2 or Midjourney).
   - Run the script to mint all NFTs.
   ```
   npx hardhat run scripts/mint.js --network 
   ```

7. **Map Collection to Polygon**
   - Use Polygon's token mapper to visualize and track your NFTs on the Polygon network.

8. **Transfer NFTs to Polygon**
   - Write a Hardhat script (`scripts/transferToPolygon.js`) to batch transfer all NFTs from Ethereum to Polygon Mumbai using the FxPortal Bridge.
   ```
   npx hardhat run scripts/transferToPolygon.js --network 
   ```

9. **Testing and Verification**
   - Test the balance of NFTs on the Polygon Mumbai network using appropriate scripts (`scripts/balanceOf.js`).
   ```
   npx hardhat run scripts/balanceOf.js --network mumbai
   ```

### Smart Contract Functions

- **promptDescription**
  - Returns the prompt used to generate the images for the NFTs.

### Scripts Overview

- **deploy.js**: Deploys the ERC721 or ERC1155 smart contract on Goerli Ethereum Testnet.
- **mint.js**: Mints a collection of NFTs based on generated images using DALLE 2 or Midjourney.
- **transferToPolygon.js**: Transfers all minted NFTs from Ethereum to Polygon Mumbai using the FxPortal Bridge.
- **balanceOf.js**: Tests and verifies the balance of NFTs on Polygon Mumbai network.

### Notes

- Ensure all environment variables are correctly set before running any scripts.
- Modify scripts to suit specific needs or integrate additional functionality as required.

### License

This project is licensed under the MIT License - see the LICENSE file for details.

### Acknowledgments

- Thank you to Pinata for providing IPFS pinning services.
- Thanks to Polygon for their network and token mapping capabilities.

### Contact

For questions or support, please contact.

---
