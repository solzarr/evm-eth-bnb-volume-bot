
```markdown
# Volume Bot on EVM Chains

## Supported Chains
- BSC
- Ethereum Mainnet
- (Any EVM-compatible chain)

## Technology

- Language: Typescript, Solidity
- Type: Bot Script

## How to Use the Bot

1. Install Node modules:
```bash
npm i
```

2. Edit the contents of the `.env` file. The project includes a pre-configured `.env` file with your wallet details.

3. Input your wallet address and private key:
```plaintext
ETH_BASE_WALLET_ADDRESS="Your wallet address"
ETH_PRIVATE_KEY="Your private key of your base wallet"
```

4. The `.env` file contains RPC addresses; they are not paid versions. If you have a good RPC provider, replace them with your own.

5. Review the `config.json` file, which contains the main configuration settings. Comments are included for clarity. Example:
```js
// Random amount for wallet
export const amountMax = 0.003; // Ether balance
export const amountMin = 0.001; // Should be more than 0.001

// Fee balance that must remain in the wallet
export const fee = 0.001; // Must be greater than 0.001
```

6. Adjust the configuration as needed. For example:
```js
// Random time interval of buy and sell
export const maxInterval = 30000; // milliseconds
export const minInterval = 5000;  // milliseconds

// Wallet settings
export const amountMax = 0.03; // Ether balance
export const amountMin = 0.01; // Should be more than 0.001

// Fee to keep in wallet
export const fee = 0.005; // Greater than 0.001

// Number of sub-wallets
export const subWalletNum = 20;

// Chain ID (e.g., BSC, Ethereum)
export const CHAINID: ChainId = ChainId.BSC;
```

Your wallet should have enough funds to cover `(amountMax + fee) * subWalletNum`. For example, with the above settings, approximately `0.7 BNB/ETH` is needed.

**Tip:** Use a higher fee value like 0.01 to ensure successful transactions and fund collection in case of errors.

7. Run the bot:
```bash
npm run dev
```

## Features
- Generating random wallets
- Funding wallets to simulate real traders
- Randomized trading actions (buy/sell)
- Collecting funds after trading

## Example

![Example Image](https://github.com/user-attachments/assets/ac6e55f6-7ece-4cad-8dc7-883423c32f4e)

## Transaction Links
- [BSCScan TX 1](https://bscscan.com/tx/0x581cda788080b52fbd5db8c4d3500c22a6c136a07b73e2311d1fc29330d48fe5)
- [BSCScan TX 2](https://bscscan.com/tx/0x8c870cf1721c2c765b45d2b13731bf384ec2e8020552aafb0436c01ded98f2ab)
- [BSCScan TX 3](https://bscscan.com/tx/0xb46d289c48d04dc6cc74849ecd9ef4fff6bf86aa3b16fc231d019b82c7789bc2)

## Future Plans
- Randomizing trading amounts
- Randomizing trading frequency (buy/sell)
- Randomizing trading pools

---

## Contact Information

For support, questions, or contributions, please contact me:

- **Twitter:** [solzarr](https://x.com/0xmarcus0401)  
- **Telegram:** [solzarr](https://t.me/solzarr)  

Feel free to reach out for collaboration or suggestions!
```
