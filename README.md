# Deploying Smart Contract - Ceating Crypto currency.
##### _Deploying Smartcontract on Polygon matic network_

#### _Crypto Wallet_
- Install metamask from [Metamask] and create wallet 
- Request test matic tockens from [testnet token] using you address from Metamask
- After 10-15 minutes you will have 1Matic on you wallet on mumbai testnet.
#### _Access to Node on blockchain to deploy our smart contract_
- Sign up for [Moralis] and add speedy node enpoint to metamask(choose polygon network and add mumbai to metamask).

#### _Deploying Smart contract_
- open [Remix] and create a file Token.sol under contracts
- Add below code to Token.sol and replace "Token" text with your cryptotoken name, "TKN" text
your cryptotoken symbol three character text.
- Click on Compile icon and compile the Token.sol code.
- Click on Deploy icon and choose ENVIRONMENT as "Injected Web3" and connect to metamask wallet. 
- Also check the Matic tokan balance on you wallet you should have some balance on the wallet to deploy the Smartcontract.
- Check ACCOUNT detail you should have your wallet ID auto-populated.
- Click on the Deploy button to deploy the Smartcontrat and receive the token to your wallet.
- you will be asked for authenticate transaction through metamask popup and some gas fee will be leaved, pay it from wallet and complete the transaction.
- click on the activity in the metamask wallet and navigate to last transaction and visit the hyperlink this will leed to blockchain explorer and get the created contract address.
- On metamask clik on import token and add contract address and view the tokens on your wallet.
- Now you can send and receive this tokens to any one

Note: This guide helps you in deploy smart contract on test network, to deploy it on main network you just choose Mainnet instead on Mumbai on Metamask and compile and deploy the Smart contract. 
```sh
// SPDX-License-Identifier: MIT
pragma solidity ^0.7.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v3.4.0-solc-0.7/contracts/token/ERC20/ERC20.sol";
contract Token is ERC20 {
    constructor () ERC20("Token", "TKN") {
        _mint(msg.sender, 1000000 * (10 ** uint256(decimals())));
    }
}
```




[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [Remix]: <https://remix.ethereum.org/>
   [Moralis]: <https://moralis.io/>
   [testnet token]: <https://faucet.polygon.technology/>
   [Metamask]: <https://metamask.io/>
   [dill]: <https://github.com/joemccann/dillinger>
