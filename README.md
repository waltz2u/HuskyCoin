# HuskyCoin
HuskyCoin is forked from SimpleCoin. It's purpose is only to open to people who join this project for learning and experimenting blockchain.

## How to run it

First, install ```requirements.txt```.

```
pip install -r requirements.txt
```

Then you have 2 options:

- Run ```miner.py``` to become a node and start mining
- Run ```wallet.py``` to become a user and send transactions (to send transactions you must run a node, in other words, you must run ```miner.py``` too)

> Important: DO NOT run it in the python IDLE, run it in your console. The ```miner.py``` uses parallel processing that doesn't work in the python IDLE.

## How this code work?

There are 2 main scripts:

- ```miner.py```
- ```wallet.py```

### Miner.py

This file is probably the most important. Running it will create a node (like a server). From here you can connect to the blockchain and process transactions (that other users send) by mining. As a reward for this work, you recieve some coins. The more nodes exist, the more secure the blockchain gets.

```miner.py``` has 2 processes running in parallel:

1. The first process takes care of mining, updating new blockchains and finding the proof of work.

2. The second process runs the flask server where peer nodes and users can connect to ask for the entire blockchain or sumbmit new transactions.

> Parallel processes don't run in python IDLE, so make sure you are running it from the console.

![miner](https://k60.kn3.net/3/B/3/F/E/C/013.png)

### Wallet.py

This file is for those who don't want to be nodes but simple users. Running this file allows you to generate a new address, send coins and check your transaction history (keep in mind that if you are running this in a local server, you will need a "miner" to process your transaction).
When creating a wallet address, a new file will be generated with all your security credentials. You are supposed to keep it safe.

![wallet](https://k60.kn3.net/6/F/E/3/8/2/887.png)
