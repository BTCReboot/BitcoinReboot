Bitcoin Reboot
----------------

P2P Port: 8333

RPC Port: 8332

The decentralized, transparent and safe Bitcoin Reboot takes the first step at an equitable starting point.

Build
-----------------
### Linux

Get dependencies:
```{r, engine='bash'}
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
sudo apt-get install libboost-all-dev
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev
sudo apt-get install libminiupnpc-dev
sudo apt-get install libzmq3-dev
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler 
sudo apt-get install libqt4-dev libprotobuf-dev protobuf-compiler
```

Build:
```{r, engine='bash'}
# bitcoind
git clone https://github.com/BTCReboot/BitcoinReboot.git
cd BitcoinReboot
# Build
cd src
make -f makefile.unix

# bitcoin-qt
cd BitcoinReboot
qmake
make
```

If you find bignum.h error, install libssl1.0-dev not libssl-dev.


Shortcuts:
```{r, engine='bash'}
# Checkout
sudo vi ~/.bash_aliases
alias bitcoind='sudo /path/BitcoinReboot/src/bitcoind'
# Press :wq to save.
source ~/.bashrc
# Run the following command when the Bitcoin Reboot node is running anywhere.
bitcoind getinfo
```

Create Config File:
```
mkdir ~/.bitcoin
vi ~/.bitcoin/bitcoin.conf
```

Add following lines to `bitcoin.conf` and be sure to change the rpcpassword:
```
rpcuser=username
rpcpassword=userpassword
#addnode = 35.189.150.224
```

Run:
```
./src/bitcoind
```

About
--------------

When Bitcoin first appeared, people did not know what encrypted money was. So some people only bit coin mined. Bitcoin Reboot is not just a blockchain for some people. Everyone has a chance to get a Bitcoin. In addition to the decentralization of technological meanings, we try to increase the liquidity of the encryption currency by deriving the decentralization of ownership at the beginning of the blockchain.

Website
--------------
[https://www.btcreboot.org](https://www.btcreboot.org/)

Explorer
--------------
[Bitcoin Reboot Explorer](http://35.189.150.224:3001/)

Telegram
--------------
[Bitcoin Reboot Telegram](https://t.me/joinchat/A3j_8xGE7FitrB-y_CKphw)

