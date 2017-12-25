jpcoin (jpc) is a cryptocurrency.

Installation
===========================

1) Update your Ubuntu 16.04 machine.

sudo apt-get update

sudo apt-get upgrade

2) Install the dependencies to compile from source code.

sudo apt-get install build-essential libssl-dev libdb++-dev git libssl1.0.0-dbg libdb-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev 

3) Create a directory for the source code.

mkdir jpcoin
cd jpcoin 

4) Download source code from repository.

git clone https://github.com/rohanjha1992/jpcoin.git

5) Go to the src directory of your coin.

cd jpcoin/src

6)  Make build_detect_platform is executable.

chmod +x leveldb/build_detect_platform

7) Execute the following command to compile the daemon.

make -f makefile.unix RELEASE=1

8) Run the Coin Server using ./jpcoind command

You will see message to create username and password

9) Create a new configuration file.
sudo nano /root/.jpcoin/jpcoin.conf

10) Paste the following lines in jpcoin.conf file and save it.

rpcuser=rpc_jpcoin

rpcpassword=yourrandompassword

rpcallowip=127.0.0.1

listen=1

server=1

txindex=1

daemon=1

11) Run the Coin Server using ./jpcoind command

List of API call list can be found here : https://en.bitcoin.it/wiki/Original_Bitcoin_client/API_calls_list