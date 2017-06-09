# Pericloin

![text](https://user-images.githubusercontent.com/2636451/26962199-9d3a3524-4cb2-11e7-93a8-cfd2ff0ab4cc.png)

Welcome to the Official Pericloin code repository.

Here you will find everything you need to install a Pericloin node and wallet to start mining and trading.
## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Installing

Dependencies
---------------------

These dependencies are required:

 Library     | Purpose          | Description
 ------------|------------------|----------------------
 libssl      | Crypto           | Random Number Generation, Elliptic Curve Cryptography
 libboost    | Utility          | Library for threading, data structures, etc
 libevent    | Networking       | OS independent asynchronous networking

Optional dependencies:

 Library     | Purpose          | Description
 ------------|------------------|----------------------
 miniupnpc   | UPnP Support     | Firewall-jumping support
 libdb4.8    | Berkeley DB      | Wallet storage (only needed when wallet enabled)
 qt          | GUI              | GUI toolkit (only needed when GUI enabled)
 protobuf    | Payments in GUI  | Data interchange format used for payment protocol (only needed when GUI enabled)
 libqrencode | QR codes in GUI  | Optional for generating QR codes (only needed when GUI enabled)
 univalue    | Utility          | JSON parsing and encoding (bundled version will be used unless --with-system-univalue passed to configure)
 libzmq3     | ZMQ notification | Optional, allows generating ZMQ notifications (requires ZMQ version >= 4.x)

For the versions used in the release, see [release-process.md](release-process.md) under *Fetch and build inputs*.

Dependency Build Instructions: Ubuntu & Debian
----------------------------------------------
Build requirements:

    sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils

Options when installing required Boost library files:

1. On at least Ubuntu 14.04+ and Debian 7+ there are generic names for the
individual boost development packages, so the following can be used to only
install necessary parts of boost:

        sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev

2. If that doesn't work, you can install all boost development packages with:

        sudo apt-get install libboost-all-dev

BerkeleyDB is required for the wallet.

To Build
---------------------

```bash
aclocal
automake --add-missing
./configure --with-incompatible-bdb
make
```
## Authors

* **Alessandro Ricottone** - *Lead Hoodie Collector* - [GitHub](https://github.com/ricott2)
* **Carlos Gonzalez Oliver** - *Head of Github Repository Creation* - [GitHub](https://github.com/cgoliver)
* **Simon Bernard** - *Out for injuries* 
* **Simon Sehayek** - *Head of Pokemon Department* 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* This code was shamelessfuly copied by the bitcoin project
