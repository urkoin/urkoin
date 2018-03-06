DOWNLOAD
========

* CRYPLY [CRP] Source code on github https://github.com/cryply/cryply-wallet
* CRYPLY [CRP] Download Releases https://github.com/cryply/cryply-wallet/releases/
* Algo YeScrypt https://password-hashing.net/wiki/doku.php/yescrypt


Useful links
============

* Mining Pool http://pool.cryply.io fee 0%.
* Exchanges http://cryply.exchange/
* BlockExplorer http://explorer.cryply.io/
* Faucet http://faucet.cryply.io/
* FileSharing Service https://cryply.download/
* Cloud Mining https://cryplyhash.com/

* RoadMap: http://cryply.io/roadmap/
* Website: http://cryply.io/
* BitcoinTalk/RU: https://bitcointalk.org/index.php?topic=3019189
* BitcoinTalk/EN: https://bitcointalk.org/index.php?topic=3019643
* BitcoinTalk/DE: https://bitcointalk.org/index.php?topic=3019862
* BitcoinTalk/ES: https://bitcointalk.org/index.php?topic=3019743
* Twitter https://twitter.com/cryply


Cryply Core integration/staging tree
=====================================

* Copyright (c) 2017-     Cryply Core Developers
* Copyright (c) 2009-2017 Bitcoin Core Developers
* Copyright (c) 2013-2017 Dash Developers (DarkGravityWave3)
* Copyright (c) 2014-2017 Alexander Peslyak (Yescrypt Original)



How to build console wallet on Ubuntu 16.04
===========================================
 
    sudo apt-get install build-essential
    sudo apt-get install libtool autotools-dev autoconf
    sudo apt-get install libssl-dev
    sudo apt-get install libboost-all-dev
    sudo apt-get install pkg-config
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install libdb4.8-dev
    sudo apt-get install libdb4.8++-dev

    git clone https://github.com/cryply/cryply-wallet.git
    cd cryply
    ./autogen.sh
    ./configure --enable-upnp-default --without-gui --disable-tests
    make

Development tips and tricks
----------------------------

**compiling for debugging**

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging message are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

Run with the -testnet option to run with "play bitcoins" on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand; see qa/rpc-tests/ for tests
that run in -regest mode.

**DEBUG_LOCKORDER**

Bitcoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.



License
-------

Cryply Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see http://opensource.org/licenses/MIT.



