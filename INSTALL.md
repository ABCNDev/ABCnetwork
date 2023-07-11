# Running ABCN on Ubunut 20.04

## Server Requirements:

- Operating System: Ubuntu 20.04
- Type: Secured VPS 
- RAM: 8 Gigs RAM
- Cores: 4 Processing Core
- Disk: 100 GB SSD

## 1. Downloading and installing geth:

```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/geth-alltools-linux-amd64.tar.xz && tar -xvf geth-alltools-linux-amd64.tar.xz && cd geth-alltools-linux-amd64 && cp * /usr/local/bin && cd ../ && rm -rf geth-alltools-linux-amd64 && rm geth-alltools-linux-amd64.tar.xz
```



## 2.1 Download MainNet Genesis File:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network.json
```


or (if running testnet)


## 2.2 Download TestNet Genesis File:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network_testnet.json
```



## 3.1 Initialising Data Directory for MainNet:
```sh
geth --datadir "/root/.abcn" init ace_blockchain_crypto_network.json
```


or (if running testnet)


## 3.2 Initialising Data Directory for TestNet:
```sh
geth --datadir "/root/.abcnTN" init ace_blockchain_crypto_network_testnet.json
```



## 4.1 Running ABCN MainNet:
```sh
screen geth --datadir "/root/.abcn" --networkid 6198  --port 6755 --syncmode 'full' --bootnodes enode://fd015398dbadfcdbb3b99bebe062ca71eb0d2d654bac31a1194c603ac5fe20b4fdcadb87fa1e7a6232eebaf66dead928afe61d098419ae0b9ea99837d6b6b4d4@139.177.194.24:6755 2>>/root/.abcn/chain.log &
```

or (if running testnet)


## 4.2 Running ABCN TestNet:
```sh
screen geth --datadir "/root/.abcnTN" --networkid 16198  --port 16755 --syncmode 'full' --bootnodes enode://fd348693a308eeb599a13a26a2f5244b6d46913688727cc649e2d23bbf28fdf2e43dcc506c544cc596bf1963c4e9cf079d782813084b745aab31ac8d1a6e2298@172.104.216.154:16755 2>>/root/.abcnTN/chain.log &
```




### Web3 Documentation:

https://web3js.readthedocs.io/en/v1.2.2/getting-started.html#adding-web3-js


### RPC Documentation:

https://ethereum.github.io/execution-apis/api-documentation
