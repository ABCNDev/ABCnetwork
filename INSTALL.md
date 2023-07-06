# Running ABCN on Ubunut 20.04

## Server Requirements:

- Operating System: Ubuntu 20.04
- Type: Secured VPS 
- RAM: 8 Gigs RAM
- Cores: 4 Processing Core
- Disk: 100 GB SSD

## 1. Downloading and installing geth:

```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/geth-alltools-linux-amd64.tar.xz && tar -xvf geth-alltools-linux-amd64.tar.xz && cd geth-alltools-linux-amd64 && cp * /usr/local/bin cd ../ && rm -rf geth-alltools-linux-amd64 && rm geth-alltools-linux-amd64.tar.xz
```



## 2.1 Download MainNet Genesis File:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network.json
```


or (if running testnet)


## 2.2 Download TestNet Genesis File:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network.json
```



## 3.1 Initialising Data Directory for MainNet:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network.json && geth --datadir "/root/.abcn" init ace_blockchain_crypto_network.json
```


or (if running testnet)


## 3.2 Initialising Data Directory for TestNet:
```sh
wget https://github.com/ABCNDev/ABCnetwork/releases/download/v1.0/ace_blockchain_crypto_network_testnet.json && geth --datadir "/root/.abcnTN" init ace_blockchain_crypto_network_testnet.json
```



## 4.1 Running ABCN MainNet:
```sh
screen geth --datadir "/root/.abcn" --networkid 6198  --port 6755 --syncmode 'full' --bootnodes enode://db2f8c313d77235ea36cdd09092cdce4a7c2ace6da6946b5e3f5a253524a851f6ce60b5388c76d804bfac9556c5248af64934ec53466a2edec2d56b6a3860cbe@139.177.194.24:0?discport=30301 2>>/root/.abcn/chain.log &
```

or (if running testnet)


## 4.2 Running ABCN TestNet:
```sh
screen geth --datadir "/root/.abcnTN" --networkid 16198  --port 16755 --syncmode 'full' --bootnodes enode://a9d9b2b1a98c333df8b58a8f40d464f35a22defbf89775f438f8810fcd01be7e9442199e797ff7f6e84da4beccd3cf927801d704082d012a9647a930179b5dc9@172.104.216.154:0?discport=30301  2>>/root/.abcnTN/chain.log &
```




### Web3 Documentation:

https://web3js.readthedocs.io/en/v1.2.2/getting-started.html#adding-web3-js


### RPC Documentation:

https://ethereum.github.io/execution-apis/api-documentation
