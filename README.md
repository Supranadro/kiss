Kiss (fork of PIVX Core) integration/staging repository
======================================




***

Quick installation of the Kiss daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/KissNetwork/Kiss.git
    cd Kiss
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip kissd
    sudo strip kiss-cli
    sudo strip kiss-tx
    cd ..

Running the daemon:

    kissd 

Stopping the daemon:

    kiss-cli stop

Demon status:

    kiss-cli getinfo
    kiss-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:



P2P port: 2003, RPC port: 2003
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.

Credits:
Dash
Bitcoin
PIVX
Peercoin
Blocknode
ALQO
LPC
# Kisscore
