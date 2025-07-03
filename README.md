# Zama FHE Protocol Technical Guides
I regularly update this repository with detailed guides on technical tasks related to the Zama protocol.

## Environment
**Linux Ubuntu OS**
* **VPS**: You can use a linux VPS to follow the guide
* **Windows**: Install Linux Ubuntu using WSL by following this [guide](https://github.com/0xmoei/Install-Linux-on-Windows)
* **Codespace**: If you don't have VPS or Windows WSL, you can use [Github Codespace](https://github.com/codespaces), create a blank template and run your codes.

## Deploy FHECounter contract
```
git clone https://github.com/zama-ai/fhevm-hardhat-template
cd fhevm-hardhat-template
```

Install:
```
npm install
```

Replace `hardhat.config.ts` file:
```
curl -o hardhat.config.ts https://raw.githubusercontent.com/SilviuASY/zama-fhe/refs/heads/main/hardhat.config.ts
```

Set Sepolia RPC:
```
npx hardhat vars set SEPOLIA_RPC_URL
```
* It prompts you to enter a Sepolia RPC, you can use `https://ethereum-sepolia-rpc.publicnode.com`

Set Privatekey:
```
npx hardhat vars set PRIVATE_KEY
```
* It prompts you to enter a privatekey, enter without `0x` perfix.

Verify your wallet:
```
npx hardhat accounts --network sepolia
```

Compile and Deploy:
```
# Compile
npx hardhat compile

# Deploy
npx hardhat deploy --network sepolia
```
* It responds with your deployed contract address
