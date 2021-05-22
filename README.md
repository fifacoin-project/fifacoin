Fifacoin integration/staging tree
================================

![banner](https://user-images.githubusercontent.com/84254341/119240528-75890f00-bb26-11eb-8c02-2a9925f0976e.png)

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2021 Fifacoin Developers

What is Fifacoin?
----------------

Fifacoin is a lite version of Litecoin using scrypt as a proof-of-work algorithm.
 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2016 blocks to retarget difficulty

License
-------

Fifacoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Fifacoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/fifacoin-project/fifacoin/tags) are created
regularly to indicate new official, stable release versions of Fifacoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./fifacoin-qt_test

##Starting wallet Fifacoin linux

VM@USER$
sudo apt-get install git

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

VM@USER$ cd Desktop/

sudo git clone https://github.com/fifacoin-project/fifacoin.git

VM@USER/Desktop$ cd fifacoin/

VM@USER/Desktop/fifacoin$ qmake

VM@USER/Desktop/fifacoin$ make

VM@USER/Desktop/fifacoin$ cd src/

VM@USER/Desktop/fifacoin/src$ make -f makefile.unix

VM@USER/Desktop/fifacoin/src$ cd ..

VM@USER/Desktop/fifacoin$ ./fifacoin-qt
