# Meetup on Jan 17, 2018: Hands-on with web3.js
The goal of this meetup to make more concrete the concepts like public/private keys and signed transactions 
that we discussed in the [Blockchain 101](https://docs.google.com/presentation/d/1v8ztCnLDqF_C3PQ_fILWjpn_9gW-CQTYJQfADGm3KX4/edit#slide=id.p) meetup held on Jan 7,2018. We will do this by writing some simple JavaScript code. [Click here](https://docs.google.com/presentation/d/1J7tkLJpuyvmh8ZLlfIiLc20E-7Z6cDLGh94ceEZZPAM/edit#slide=id.p) for the meetup presentation.
# What we will cover in this meetup

We will cover how to work with the Ethereum blockchain.

1. Generate a public/private keypair using node.js console (web3 apis as needed).
2. Use web3 to connect to a ethereum testnet like Rinkeby via infura.io with the api keys.
3. Add some eth to the above generated keypair using [ethereum faucet](https://faucet.rinkeby.io/)
4. Create a json object on the node.js console for a eth transfer transaction between one meetup participant and the person sitting next to them or anyone else.
5. Sign it, send it
6. Use etherscan to confirm it. Also use web3 api in the node.js console to confirm it.

# Learn by writing code

Use these [instructions](instructions.md) if you want to learn by typing the code yourself. 

# Learn by running sample scripts

Use these scripts if you don't want to type code. 

```shell

$ export ETHEREUM_NETWORK="https://rinkeby.infura.io/<your-infura-key>"
$ npm install # You can safely ignore the warnings
$ ./generate_keypair_eth.js  --password <your-secret-password>
$ ./check_balance_eth.js --address <your-public-key-address>
```

Your balance will show as zero , as you don't hold any ether. To get test ethereum [see this](https://github.com/Tri-Valley-Blockchain/meetups/blob/master/Jan17-2018-web3.eth/instructions.md#step-2-get-free-ethereum-to-use-later-in-transactions)

Once you acquire some ethereum, find someone to send this ethereum to by asking for their public address. 

```shell
$ ./send_eth.js --key <your-private-key-from-above> --address <your-public-key-from-above> --to <your-friends-public-key>

```

