# project eaGle nest : smartContract Lottery

## what it has ?
- Chainlink VRF
- Robust UI
- really a Seamless experience for users
- verifiablity of each steps

### steps initiated:
- wrote Lottery.sol
- downloading dependency for chainlink contract, npm i @chainlink/contracts --save
- creating `.env` and setting up configuration (through truffle-config.js)
- for accessing account setting up private keys and properties of the network to which to deploy all like did in brownie.
- now create file in migrations - '2_deploy_contracts.js'.

> ### [lottery address](`https://rinkeby.etherscan.io/tx/${0x0x5be55a3f443A068d615fB59593d6E4E1e6DC7454}`) (not verified though)

Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 30000000 (0x1c9c380)
2_deploy_contracts.js



   Replacing 'Lottery'
   -------------------
   > transaction hash:    0xec68aa0bf37e238dd5c855f64dee64e33f1652746b189bd82766334c11d62493\
   > Blocks: 2            Seconds: 21\
   > contract address:    0x5be55a3f443A068d615fB59593d6E4E1e6DC7454\
   > block number:        block no.\
   > block timestamp:     block timestamp\
   > account:             MY ACCOUNT ADDRESS\
   > balance:             MY ACCOUNT BALANCE\
   > gas used:            1213798 (0x128566)\
   > gas price:           2.500000008 gwei\
   > value sent:          0 ETH\
   > total cost:          0.003034495009710384 ETH\

   Pausing for 2 confirmations...

   -------------------------------
   > confirmation number: 1 (block: 11435563)
   > confirmation number: 2 (block: 11435564)
   > Saving artifacts
   -------------------------------------
   > Total cost:     0.003034495009710384 ETH

Summary
=======
> Total deployments:   1
> Final cost:          0.003034495009710384 ETH


### Go back to client
- now to glue userInterface with blockchain, we need `contract_abi` alongwith its `address` as you know already.
- since multiple contracts are involved here and no one knows why but I want to get abi for dependency contracts even. So, installing.. solc: ^0.8.11
(simply you may edit the package.json and hit npm i, so to avoid any possible version mismatch).
`Later found to be having some discrepancies in abi from deploy and from solc but only solc one was working.`
- So to use `solc lib.` you need to hit command so just edit scripts (`package.json`) and hit command but since you don't have `@chainlink/contracts` dependencies installed, install them first.

> truffle migrate --network rinkeby\
> npm run compile
