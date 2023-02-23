# Mina zkApp: Add

This template uses TypeScript. In this example we have a zkApp which updates the state fields every time a transaction is sent to it.


## Setup
### Clone the repository 
```
git clone git@github.com:NilFoundation/mina-zkapp-demo.git
cd mina-zkapp-demo
```
### Install dependencies
```
npm install -g zkapp-cli
npm i
```

### Setup keys/Fund wallet
Before deploying , you must fund the wallet.  There are two key-pairs required
- zkApp : This keypair is for the deployed zkApp.  
- User: This keypair is for user signing & calling zkApp.

### Deploy to Berkley testnet

This command will deploy to berkeley testnet
```
zk deploy berkeley
```

### How to build

```sh
npm run build
```

### How to call zkApp
This command will call the update method of the zkApp
```
node build/src/interact.js berkeley
```

## How to run tests

```sh
npm run test
npm run testw # watch mode
```

## How to run coverage

```sh
npm run coverage
```

## License

[Apache-2.0](LICENSE)
