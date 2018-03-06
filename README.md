+ADwAPAA8ADwAPAA8ADw- HEAD
DOWNLOAD
+AD0APQA9AD0APQA9AD0APQ-

+ACo- URKOIN +AFs-URK+AF0- Source code on github https://github.com/urkoin/urkoin-wallet
+ACo- URKOIN +AFs-URK+AF0- Download Releases https://github.com/urkoin/urkoin-wallet/releases/
+ACo- Algo YeScrypt https://password-hashing.net/wiki/doku.php/yescrypt


Useful links
+AD0APQA9AD0APQA9AD0APQA9AD0APQA9-

+ACo- Mining Pool http://pool.urkoin.io fee 0+ACU-.
+ACo- Exchanges http://urkoin.exchange/
+ACo- BlockExplorer http://explorer.urkoin.io/
+ACo- Faucet http://faucet.urkoin.io/
+ACo- FileSharing Service https://urkoin.download/
+ACo- Cloud Mining https://urkoinhash.com/

+ACo- RoadMap: http://urkoin.io/roadmap/
+ACo- Website: http://urkoin.io/
+ACo- BitcoinTalk/RU: https://bitcointalk.org/index.php?topic+AD0-3019189
+ACo- BitcoinTalk/EN: https://bitcointalk.org/index.php?topic+AD0-3019643
+ACo- BitcoinTalk/DE: https://bitcointalk.org/index.php?topic+AD0-3019862
+ACo- BitcoinTalk/ES: https://bitcointalk.org/index.php?topic+AD0-3019743
+ACo- Twitter https://twitter.com/urkoin


Urkoin Core integration/staging tree
+AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0-

+ACo- Copyright (c) 2017-     Urkoin Core Developers
+ACo- Copyright (c) 2009-2017 Bitcoin Core Developers
+ACo- Copyright (c) 2013-2017 Dash Developers (DarkGravityWave3)
+ACo- Copyright (c) 2014-2017 Alexander Peslyak (Yescrypt Original)



How to build console wallet on Ubuntu 16.04
+AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0APQA9AD0-
 
    sudo apt-get install build-essential
    sudo apt-get install libtool autotools-dev autoconf
    sudo apt-get install libssl-dev
    sudo apt-get install libboost-all-dev
    sudo apt-get install pkg-config
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install libdb4.8-dev
    sudo apt-get install libdb4.8dev

    git clone https://github.com/urkoin/urkoin-wallet.git
    cd urkoin
    ./autogen.sh
    ./configure --enable-upnp-default --without-gui --disable-tests
    make

Development tips and tricks
----------------------------

+ACoAKg-compiling for debugging+ACoAKg-

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS+AD0AIg--g -ggdb -O0+ACI- or whatever debug flags you need.

+ACoAKg-debug.log+ACoAKg-

If the code is behaving strangely, take a look in the debug.log file in the data directory+ADs-
error and debugging message are written there.

The -debug+AD0-... command-line option controls debugging+ADs- running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category +ACI-qt+ACI-: run with -debug+AD0-qt
to see it.

+ACoAKg-testnet and regtest modes+ACoAKg-

Run with the -testnet option to run with +ACI-play bitcoins+ACI- on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand+ADs- see qa/rpc-tests/ for tests
that run in -regest mode.

+ACoAKg-DEBUG+AF8-LOCKORDER+ACoAKg-

Bitcoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG+AF8-LOCKORDER (configure
CXXFLAGS+AD0AIg--DDEBUG+AF8-LOCKORDER -g+ACI-) inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.



License
-------

Urkoin Core is released under the terms of the MIT license. See +AFs-COPYING+AF0-(COPYING) for more
information or see http://opensource.org/licenses/MIT.



+AD0APQA9AD0APQA9AD0-
+ACM- urkoin
Urkoin cryptocurrency
+AD4APgA+AD4APgA+AD4- adbd92448b661e09273147f9ed57a2f065772df5
