# Mina zkApp: Add

In this example we deploy a zkApp which updates the zkApp state fields every time a transaction is sent to it by 2.
This is done via the `update` method called on the zkApp `Add`

Configuration is set-up to be deployed on berkeley testnet.

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
Before deploying , you must fund the wallet.  There are two key-pairs required/
- zkApp : This keypair is for the zkApp. Located in `keys/berkeley.json`  
- User: This keypair is for user signing & calling zkApp method. Located in `keys/user.json`

You must update these files. 

TODO: Add instructions/code to create keypair

Both wallets must be funded by requesting faucet funds here by providing the public key:
```
https://faucet.minaprotocol.com/
```

### Build Project
Typescript must be compiled to javascript to be executed , this is done via. 
```sh
npm run build
```
This should be run after any changes are made to the project.

### Deploy zkApp to Berkley testnet
Once funded , this command will deploy zkApp `Add` to  `berkeley` testnet. The address of the
zkApp is the public key defined in `keys\berkeley.json`.

```
zk deploy berkeley
```

### Call `update` on `Add` zkApp
This command will call the update method of the zkApp `Add`
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
