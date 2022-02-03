# 🚀 Solana SPL Tutorial
This repository contains full tutorial on Solana SPL token

## Table of Contents
- [Prerequisites](#prerequisites)
- [Creating Solana Wallet](#creating-solana-wallet)
- [Creating SPL Tokens](#creating-spl-tokens)
- [Creating SPL NFTs](#creating-spl-nfts)
- [Further Resources](#further-resources)
- [License](#license)

### Prerequisites

#### 1. Solana CLI

**MacOS & Linux**

```sh
sh -c "$(curl -sSfL https://release.solana.com/v1.9.5/install)"
```

**Windows**

```sh
curl https://release.solana.com/v1.9.5/solana-install-init-x86_64-pc-windows-msvc.exe --output C:\solana-install-tmp\solana-install-init.exe --create-dirs
```

#### 2. SPL CLI

```sh
cargo install spl-token-cli
```

#### 3. Solana Wallet

For this tutorial, we're going to use a Filesystem wallet. This is sufficient for testing, but not recommended for production purpose.

```sh
solana-keygen new --no-outfile
```

#### 4. Configure Solana Cluster

Check your Solana Cluster configuration

```sh
solana config get
```

Set the Solana Cluster to Testnet

```sh
solana config set --url https://api.devnet.solana.com
```

#### 5. SOL Balance

To check you SOL balance

```sh
solana balance
```

To get some testnet SOL

```
solana airdrop 1
```

### Creating SPL Tokens

First, create the token

```sh
spl-token create-token
```

Using the unique token identifier, we can create an account to store our balance data

```sh
spl-token create-account <token-identifier>
```

Once the account is created, we can mint some SPL tokens.

```sh
 spl-token mint <token-identifier> <token-amount>
```

To check the total supply of the token, use the following command

```sh
spl-token supply <token-identifier>
```

To check the balance of the token, use the following command

```sh
spl-token balance <token-identifier>
```


### Creating SPL NFTs

```sh
spl-token create-token --decimals 0
```

### Further Resources
- [Solana Docs](https://docs.solana.com/introduction)
- [SPL Token Program](https://spl.solana.com/token)
- [Metaplex Docs](https://docs.metaplex.com/candy-machine-v1/introduction)

### License

[MIT License](https://github.com/YosephKS/solana-spl-tutorial/blob/main/LICENSE)
