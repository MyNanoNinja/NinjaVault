# NOSwallet

NOSwallet is a fully client-side signing wallet for sending and receiving [NOS](https://github.com/NOS-Cash/NOSnode/tree/nos-network) 
on your [desktop](https://github.com/NOS-Cash/NOSvault/releases) or [in your browser](https://my.nos.cash)

![NOSwallet Screenshot](https://s3-us-west-2.amazonaws.com/my.nos.cash/NOSwallet-Preview.png)
___

# Table of Contents
* [Install](#install-noswallet)
* [Bugs/Feedback](#bugsfeedback)
* [Application Structure](#application-structure)
* [Development Prerequisites](#development-prerequisites)
* [Development Guide](#development-guide)
* [Acknowledgements](#acknowledgements)


# Install NOSwallet
NOSwallet is available on your desktop (Windows/Mac/Linux) - just head over to the [releases section](https://github.com/NOS-Cash/NOSvault/releases) and download the latest version for your OS.

You can also use NOSwallet from any device on the web at [my.nos.cash](https://my.nos.cash)


# Bugs/Feedback
If you run into any issues, please use the [GitHub Issue Tracker](https://github.com/NOS-Cash/NOSvault/issues) or head over to our [Discord Server](https://discord.gg/kCeAuJM)!  
We are continually improving and adding new features based on the feedback you provide, so please let your opinions be known!

To get an idea of some of the things that are planned for the near future, check out the [Road Map](https://github.com/NOS-Cash/NOSvault/wiki/Road-Map).

___

#### Everything below is only for contributing to the development of NOSwallet
#### To download NOSwallet go to the [releases section](https://github.com/NOS-Cash/NOSvault/releases), or use the web wallet at [my.nos.cash](https://my.nos.cash)

___

# Application Structure

The application is broken into a few separate pieces:

- [NOSwallet](https://github.com/NOS-Cash/NOSvault) - The main wallet application (UI + Seed Generation/Block Signing/Etc).
- [NOSwallet-Server](https://github.com/NOS-Cash/NOSvault-server) - Serves the Wallet UI and brokers public communication between the wallet and the NOS Node.
- [NOSwallet-WS](https://github.com/NOS-Cash/NOSvault-ws) - Websocket server that receives new blocks from the NOS node and sends them in real time to the wallet ui.


# Development Prerequisites
- Node Package Manager: [Install NPM](https://www.npmjs.com/get-npm)
- Angular CLI: `npm install -g @angular/cli`


# Development Guide
#### Clone repository and install dependencies
```bash
git clone https://github.com/NOS-Cash/NOSvault
cd noswallet
npm install
```

#### Run the wallet in dev mode
```bash
npm run wallet:dev
```

## Build Wallet (For Production)
Build a production version of the wallet for web:
```bash
npm run wallet:build
```

Build a production version of the wallet for desktop: *(Required for all desktop builds)*
```bash
npm run wallet:build-desktop
```

## Desktop Builds

*All desktop builds require that you have built a desktop version of the wallet before running!*

Run the desktop wallet in dev mode:
```bash
npm run desktop:dev
```

Build the desktop wallet for your local OS (Will be in `dist-desktop`):
```bash
npm run desktop:local
```

Build the desktop wallet for Windows+Mac+Linux (May require dependencies for your OS [View them here](https://www.electron.build/multi-platform-build)):
```bash
npm run desktop:full
```

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

# Acknowledgements
Special thanks to the following!
- [numtel/nano-webgl-pow](https://github.com/numtel/nano-webgl-pow) - WebGL PoW Implementation
- [jaimehgb/RaiBlocksWebAssemblyPoW](https://github.com/jaimehgb/RaiBlocksWebAssemblyPoW) - CPU PoW Implementation
- [dcposch/blakejs](https://github.com/dcposch/blakejs) - Blake2b Implementation
- [dchest/tweetnacl-js](https://github.com/dchest/tweetnacl-js) - Cryptography Implementation

If you have found NOSwallet useful and are feeling generous, you can donate at `nos_318syypnqcgdouy3p3ekckwmnmmyk5z3dpyq48phzndrmmspyqdqjymoo8hj`
