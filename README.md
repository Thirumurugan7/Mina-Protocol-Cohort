# Mina zkApp: 01 Hello World

This template uses TypeScript.

## How to build

```sh
npm run build
```

## How to run tests

```sh
npm run test
npm run testw # watch mode
```

## How to zk proof

```sh
npm run build && node build/src/main.js```

## License

[Apache-2.0](LICENSE)

thiru@THIRUMURUGANs-MacBook-Air minamania % ls
01-hello-world sudoku testhyperoracle
thiru@THIRUMURUGANs-MacBook-Air minamania % cd 01`
bquote>
thiru@THIRUMURUGANs-MacBook-Air minamania % cd 01-hello-world
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % ls
LICENSE build jest.config.js package-lock.json tsconfig.json
README.md config.json keys package.json
babel.config.cjs jest-resolver.cjs node_modules src
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % npm run build && node build/src/main.js

> 01-hello-world@0.1.0 build
> tsc

state after init: 3
state after txn1: 6
Field.assertEquals(): 9 != 12
state after txn2: 6
state after txn3: 12
Shutting down
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % zk deploy thiru
Deploy alias name not found in config.json.
You can add a deploy alias by running `zk config`.
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % ls  
LICENSE build jest.config.js package-lock.json tsconfig.json
README.md config.json keys package.json
babel.config.cjs jest-resolver.cjs node_modules src
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % zk deploy berkeley

Deploy alias name not found in config.json.
You can add a deploy alias by running `zk config`.
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % zk config

┌──────────────────────────────────┐
│ Deploy aliases in config.json │
├────────┬────────┬────────────────┤
│ Name │ URL │ Smart Contract │
├────────┴────────┴────────────────┤
│ None found │
└──────────────────────────────────┘

Enter values to create a deploy alias:
✔ Create a name (can be anything): · thiru
✔ Set the Mina GraphQL API URL to deploy to: · https://proxy.berkeley.minaexplorer.com/graphql
✔ Set transaction fee to use when deploying (in MINA): · 0.001
✔ Choose an account to pay transaction fees: · Use stored account sudoku (public key: B62qpPcKxpqCB5JV9PFBMQKFmtcSd9rjcdPXGKfMJEwGS7tPmTupFma)

✔ Use stored fee payer sudoku (public key: B62qpPcKxpqCB5JV9PFBMQKFmtcSd9rjcdPXGKfMJEwGS7tPmTupFma)
✔ Create zkApp key pair at keys/thiru.json
✔ Add deploy alias to config.json

Success!

Next steps:

- If this is a testnet, request tMINA at:
  https://faucet.minaprotocol.com/?address=B62qpPcKxpqCB5JV9PFBMQKFmtcSd9rjcdPXGKfMJEwGS7tPmTupFma&?explorer=minaexplorer
- To deploy, run: `zk deploy thiru`
  thiru@THIRUMURUGANs-MacBook-Air 01-hello-world % zk deploy thiru
  ✔ Build project
  ✔ Generate build.json
  ✔ Choose smart contract
  Only one smart contract exists in the project: Square
  Your config.json was updated to always use this
  smart contract when deploying to this deploy alias.
  ✔ Generate verification key (takes 10-30 sec)
  ✔ Build transaction
  ✔ Confirm to send transaction

┌─────────────────┬─────────────────────────────────────────────────┐
│ Deploy Alias │ thiru │
├─────────────────┼─────────────────────────────────────────────────┤
│ Fee Payer Alias │ sudoku │
├─────────────────┼─────────────────────────────────────────────────┤
│ URL │ https://proxy.berkeley.minaexplorer.com/graphql │
├─────────────────┼─────────────────────────────────────────────────┤
│ Smart Contract │ Square │
└─────────────────┴─────────────────────────────────────────────────┘

Are you sure you want to send (yes/no)? · yes
✔ Send to network

Success! Deploy transaction sent.

Next step:
Your smart contract will be live (or updated)
as soon as the transaction is included in a block:
https://minascan.io/berkeley/tx/5Jv91aeddfj48qhfW2E8DztWFpw9wM2HcKVsPvJFHo18f7GoWnY2?type=zk-tx
thiru@THIRUMURUGANs-MacBook-Air 01-hello-world %
