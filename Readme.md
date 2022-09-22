### steps initiated:
- wrote Lottery.sol
- downloading dependency for chainlink contract, npm i @chainlink/contracts --save
- creating `.env` and setting up configuration (through truffle-config.js)
- - for accessing account setting up private keys and properties of the network to which to deploy.
- now create file in migrations - '2_deploy_contracts.js'.
- 

> [lottery address](`https://rinkeby.etherscan.io/tx/${0x894adcB4f81fF1FaBAbFa926d98C44B235dFAEc3}`)


Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 29999972 (0x1c9c364)


2_deploy_contracts.js
=====================

   Deploying 'Lottery'
   -------------------
   > transaction hash:    0x3f84ec86b871a5b75298dc810347eef283cb951c67d85934784cd83d0905f455
   > Blocks: 1            Seconds: 14
   > contract address:    0x894adcB4f81fF1FaBAbFa926d98C44B235dFAEc3
   > block number:        11425060
   > block timestamp:     1663854791
   > account:             0x3A41745999ad4D2c4F62e006E744Dea5CFFc1415
   > balance:             4.345631139435489559
   > gas used:            1169760 (0x11d960)
   > gas price:           2.500000008 gwei
   > value sent:          0 ETH
   > total cost:          0.00292440000935808 ETH

   Pausing for 2 confirmations...

   -------------------------------
   > confirmation number: 1 (block: 11425061)
   > confirmation number: 2 (block: 11425062)
   > Saving artifacts
   -------------------------------------
   > Total cost:     0.00292440000935808 ETH

Summary
=======
> Total deployments:   1
> Final cost:          0.00292440000935808 ETH


### Go back to client
- now to glue userInterface with blockchain, we need `contract_abi` alongwith its `address`
- since multiple contracts are involved here and no one knows why but I want to get abi for dependency contracts even. So, installing.. solc: ^0.8.11
(simply you may edit the package.json and hit npm i, so to avoid any possible version mismatch)
- so to use solc lib. you need to hit command so just edit scripts(package.json) and hit command but since you don't have @chainlink/contracts dependencies installed, install them first.
- So the `folder` I created named `blockchain` in client dir, was having build(to which contract abi's got saved), contracts(having our sole contract), lottery.js(js script to be written for exporting out direct the contract itself), out of which 2 got filled now write lottery.js
