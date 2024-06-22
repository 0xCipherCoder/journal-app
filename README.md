# Journal Dapp: An On-Chain CRUD Application on Solana

This project demonstrates a basic CRUD (Create, Read, Update, Delete) dapp, specifically a journal application where you can manage journal entries on the Solana blockchain. The dapp interacts with a Solana program and provides a user-friendly UI for seamless interaction.

<img width="1273" alt="Solana-App" src="https://github.com/0xCipherCoder/journal-app/assets/169297618/25cd6595-725b-4ae5-8ca7-bb88ff2da3d0">


## Project Overview

This project was generated using the `create-solana-dapp` generator and consists of two main components:

1. **Anchor**: A Solana program written in Rust using the Anchor framework.
2. **Web**: A React application that interacts with the Solana program via the Anchor-generated client.

## Getting Started

### Prerequisites

Ensure you have the following software installed:

- **Node.js** v18.18.0 or higher
- **Rust** v1.70.0 or higher
- **Anchor CLI** 0.29.0 or higher
- **Solana CLI** 1.17.0 or higher

### Installation

1. **Clone the Repository**:
   ```bash
   git clone <repo-url>
   cd <repo-name>

#### Install dependencies

```shell
npm install
```

#### Start the web app

```
npm run dev
```

## Apps

### Anchor

This is a Solana program written in Rust using the Anchor framework.

Note: The solana program code for the journal dapp can be found in `anchor/programs/src/lib.rs`

#### Commands

You can use any normal anchor commands. Either move to the `anchor` directory and run the `anchor` command or prefix the command with `npm run`, eg: `npm run anchor`.

#### Sync the program id:

Running this command will create a new keypair in the `anchor/target/deploy` directory and save the address to the Anchor config file and update the `declare_id!` macro in the `./src/lib.rs` file of the program.

You will manually need to update the constant in `anchor/lib/counter-exports.ts` to match the new program id.

```shell
npm run anchor keys sync
```

#### Build the program:

```shell
npm run anchor-build
```

#### Start the test validator with the program deployed:

```shell
npm run anchor-localnet
```

#### Run the tests

```shell
npm run anchor-test
```

#### Deploy to Devnet

```shell
npm run anchor deploy --provider.cluster devnet
```

### Web

This is a React app that uses the Anchor generated client to interact with the Solana program.

#### Commands

Start the web app

```shell
npm run dev
```

Build the web app

```shell
npm run build
```
