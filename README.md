# dicoapp-e
Desktop app to buy CoinCollect coins with Komodo or Bitcoin.
# Installation

## Install dependencies
### On MacOS

First, install basic **dependencies**:

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

    brew install git curl libgconf-2-4

Then, make sure you have the right **node** version:

    brew install nvm

    echo 'export NVM_DIR=~/.nvm' >> ~/.bashrc_profile

    echo 'source $(brew --prefix nvm)/nvm.sh' >> ~/.bashrc_profile

(exit from the current terminal and start another terminal window and enter the following)

    nvm install 9.11.2
    nvm use 9.11.2

Next, install the **yarn** package manager:

    brew install yarn --without-node

```
sudo apt install git curl libc6-i386 libgconf-2-4
```
# Features
- Implements BarterDex for doing decentralized ICO's, dICO's
- Buying CC with KMD or BTC

# Quick Start

```
git clone https://github.com/KomodoPlatform/dicoapp-e
cd dicoapp-e
yarn install
yarn dev
```
## Troubleshooting

### "Network error"

If marketmaker cannot be found and the app gives a "Network error" after filling in & clicking "Login", do the following:

1. Open [marketmaker.js](https://github.com/CoinCollect/dicoapp-e/blob/coincollect/app/main/plugins/marketmaker.js#L43) on your computer
2. On line 43, replace `config.get('paths.marketmaker')` with the full path of your marketmaker binary. For example: `/home/YOURNAME/BarterDEX/assets/bin/linux64/marketmaker`.

### Mac: 'invalid active developer path'

If you get something like:

    xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun

, run:

    xcode-select --install

In case this did still not solve the error, run:

    xcode-select --reset

## Useful links

- [Whitelabel instructions](https://github.com/KomodoPlatform/dicoapp-e/blob/master/docs/whitelabel.md)
