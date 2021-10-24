# Advanced-Solidity-Build-Crowd-Sale
This project involves in the creating of  puppercoin and  crowd sale Deployer.
# Crowdsale

In this Unit, we use advanced solidity concepts to create a CrowdSale of a new token called PupperCoin. The raised funds will be used to track dog breeding activity across the globe in a decentralized way. Our goal is to raise 300 ETH from this Crowdsale by minting ERC20 tokens with the help of OpenZeppelin in Solidity.

## Coding the 3 smart contracts

We have compiled and created 3 smart contracts for this crowdsale. Follow the links to see the source code.

1. [PupperCoin](PupperCoin.sol): This contract will be used to create our PupperCoin token. 

2. [PupperCoinSale](Crowdsale.sol): This contract allows us to buy Tokens, check token balances, finalize the crowdsale and claim refunds amongst other things.

3. [PupperCoinSaleDeployer](Crowdsale.sol): This contract creates two contract addresses: 1 for the token address and another for the token sale address. We can these use these generated contract addresses to deploy the PupperCoin and PupperCoinSale contracts mentioned above. Note that to fill in the cap and goal parameters, I used this [ETH converter](https://eth-converter.com/) to convert 300 ETH to wei. 

------------------------------

## Instructions on Deploying the Contracts

Steps:
1. Compile `PupperCoin.sol` and `Crowdsale.sol` using compiler version 0.5.5

2. Deploy & Run the  `PupperCoin` function from the dropdown, then enter the name,symbol & Inital supply. This should generate your PupperCoin contract.

Below are the screenshots of the deployed smart contracts:

i) Initially Transfer some ether into the account.
<img width="1323" alt="1_Initial Transfer of Ether to Account 2021-10-21 at 1 58 05 PM" src="https://user-images.githubusercontent.com/83980061/138578376-932046eb-100b-4d62-bc73-16abf98cd110.png">

ii) Ether transfered to account
<img width="1408" alt="2_Ether Transfered to Account 2021-10-21 at 2 06 51 PM" src="https://user-images.githubusercontent.com/83980061/138578383-ebf0f088-927f-473a-8304-57bcf461c61b.png">

iii) Compile Puppercoin.sol

<img width="1321" alt="3_Compile_PupperCoin 2021-10-21 at 1 53 58 PM" src="https://user-images.githubusercontent.com/83980061/138578417-19a067c4-d5fb-4cb0-a933-741770b33ffb.png">

iv) Deploy & Run Puppercoin 

<img width="1402" alt="4_Deploy_Puppercoin 2021-10-21 at 2 09 18 PM" src="https://user-images.githubusercontent.com/83980061/138578424-30f1b791-2d5c-4756-82f3-75f9662bea40.png">

v) Successfull Creation of Smart Contract

<img width="1382" alt="5 1_Successfull Creation of SmartContract 2021-10-21 at 2 14 26 PM" src="https://user-images.githubusercontent.com/83980061/138578429-b4298987-07ee-451c-98a9-0b1180215ff8.png">

vi) Puppercoin Transaction log

<img width="1387" alt="6_Puppercoin Transaction log 2021-10-21 at 2 15 50 PM" src="https://user-images.githubusercontent.com/83980061/138578454-3fe25547-002b-42f8-b694-fb3ea23155c3.png">

vii) Sender Account Tokens

<img width="1311" alt="7_USDCOINS In Sender Account_Tokens 2021-10-21 at 2 03 01 PM" src="https://user-images.githubusercontent.com/83980061/138578464-52d9687c-e8df-497a-bf6a-3b68a601061f.png">


3. Deploy `Crowdsale.sol` by choosing the `PupperCoinSaleDeployer` function from the contract dropdown. Fill in the fields for Name (PupperCoin), Symbol  "PUP"  and Wallet (Choose your own wallet created from my crypto), then click on transact. This should generate two contract addresses when you click on the button for token address and token_sale_address

4. Go back to the contract deployment section, choose the `PupperCoinSale` function from the dropdown, then copy and paste the `token_sale_address` from the the previous step into the "At Address" field and click on the "At Address" button. This should generate your Puppercoin sale contract below the first contract. 

5. Below are the screenshots of the deployed smart contracts:

i) Compile CrowdSale

<img width="1394" alt="8_Compile CrowdSale 2021-10-23 at 1 18 37 PM" src="https://user-images.githubusercontent.com/83980061/138578486-788cc515-aecf-48d7-9639-ef02b6c27d9a.png">

ii) Deploy & Run PupperCoin Sale Deployer

<img width="1400" alt="9_Deploy PupperCoin Sale Deployer 2021-10-23 at 7 13 24 PM" src="https://user-images.githubusercontent.com/83980061/138578489-21e21419-99c8-436c-8d90-6ce25a426cc7.png">

iii) Deployed CrowdSale Deployer. Token Addressess are generated.

<img width="1415" alt="11_Deployed CrowdSale Deployer 2021-10-23 at 8 18 03 PM" src="https://user-images.githubusercontent.com/83980061/138578513-c5f8718f-f8be-4f0f-aff0-65e8051be562.png">

iv) Successfull Transaction of CrowdSaleDeployer
<img width="1387" alt="10_Successfull Transaction of CrowdSaleDeploye 2021-10-23 at 7 15 00 PM" src="https://user-images.githubusercontent.com/83980061/138578500-ac70877f-9023-412b-b2c2-a57f1bf4a7fa.png">

## Buying Tokens

In this section, I will show you how to buy tokens with ETH using the contracts we just created. 

- You will need some ETH first since we are doing this in the Ropsten testnet. You can get it from this [Ropsten faucet](https://faucet.ropsten.be/).

- To buy tokens, input the amount of tokens that you want to buy in the "Value" field of Solidity (Note that we have a 1:1 exchange rate of ETH to PUP token), then put the wallet address of the token buyer in the `buyToken` field of the PupperCoin sale contract. 

<img width="1411" alt=" 12_Deploy_CrowdSale_BuyToken Transaction 2021-10-23 at 9 27 52 PM" src="https://user-images.githubusercontent.com/83980061/138578530-23d4b37b-7eb1-4bf5-89b5-f125109a7177.png">


Below you can see the successful transaction hash along with the confirmation from MetaMask

<img width="1405" alt="13_Successful CrowdSale_BuyToken Transaction" src="https://user-images.githubusercontent.com/83980061/138578547-4f92f00a-7139-4992-8f95-405a534016c1.png">



Lastly, Here is my MyCrypto account. Here we can see that MyCrypto found the PUP token we created. At the time of testing and making this particular screenshot, 

<img width="1216" alt=" 14_Token In My Crypto 2021-10-23 at 10 13 12 PM" src="https://user-images.githubusercontent.com/83980061/138578554-74127b9d-bebf-4d7b-bd91-5666f99a9425.png">



-------------------------

