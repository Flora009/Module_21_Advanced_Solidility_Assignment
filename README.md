# Unit 21: Martian Token Crowdsale

![alt=""](Images/application-image.png)

## Background

After waiting for years and passing several tests, the Martian Aerospace Agency selected you to become part of the first human colony on Mars. As a prominent fintech professional, they chose you to lead a project developing a monetary system for the new Mars colony. You decided to base this new system on blockchain technology and to define a new cryptocurrency named **KaseiCoin**. (Kasei means Mars in Japanese.)

KaseiCoin will be a fungible token that is ERC-20 compliant. You will launch a crowdsale that will allow people who are moving to Mars to convert their earthling money to KaseiCoin.

## Steps on how to compile, deploy and test


## 1. Compile Results
1. Compile KaseiCoin.sol successfully

![alt=""](Evaluation_Evidence/compile_KaseiCoin_sol_successfully.png)

2. Compile KaseiCoinCrowdsale.sol successfully

![alt=""](Evaluation_Evidence/compile_KaseiCoinCrowdsale_sol_successfully.png)

3. Compile KaseiCoinCrowdsaleDeployer successfully

![alt=""](Evaluation_Evidence/compile_KaseiCoinCrowdsaleDeployer_successfully.png)


### 2. Prepare 3 accounts in metamask
Before deploying the contracts, make sure that you have launched Ganache and loaded at least three accounts into Remix.

1. __`Wallet address`__ (address from where the gas fee for deploying the smart contracts will be paid): 
- Account 10 in metamask

    `0x281C3CAE7Ced1b1bB40e1f8c31984F6b0cBb3f8e`

    initial balance = 100 ETH

2. __`Beneficiaries' addresses (purchasers' addresses)`__: 

- Account 11 in metamask

    `0xCc3c1cB89CC609158d32A8A0D26c020e3c7C329d`
    
    initial balance = 100 ETH

- Account 12 in metamask

    `0x86179a42901401d1e108b0071eeE81cd2F985F5E`
 
    initial balance = 100 ETH

Ganache Accounts Screen Shot: 

![alt=""](Evaluation_Evidence/prepare_3_accounts_in_metamask.png)



### 3. Deploy the KaseiCoinCrowdsaleDeployer, KaseiCoinCrowdsale, and KaseiCoin contracts.

To deploy the contracts, complete the following steps:
1. In the Remix IDE, navigate to the Deploy & Run Transactions pane, and then complete the following steps:
- Select an address from MetaMask (Account 10: 0x281C3CAE7Ced1b1bB40e1f8c31984F6b0cBb3f8e) that you will use to deploy the contracts. 
- Copy the address to the clipboard.
- Select the KaseiCoinCrowdsaleDeployer contract, and then fill in the values for Name and Symbol. Paste the address from the clipboard into the Wallet box.

![alt=""](Evaluation_Evidence/y_account10_deployer.png)


- Click transact, and when the MetaMask dialog box opens, confirm the transaction.

![alt=""](Evaluation_Evidence/y_account10_deployer_click_transact.png)



![alt=""](Evaluation_Evidence/y_account10_deployer_confirm.png)


![alt=""](Evaluation_Evidence/y_account10_deployer_metamask_info_after_deploy.png)



2. Navigate to the Deployed Contracts section, and then open the box that is associated with the KaseiCoinCrowdsaleDeployer contract. Notice that buttons for `kasei_crowdsale_address` and `kasei_token_address` now appear.

![alt=""](Evaluation_Evidence/y_csdeploy_info.png)

`kasei_crowdsale_address`

    0x1183f9a0680F0Ce4A7d174fE169aEdF2E8c8DA92

`kasei_token_address`

    0xB39715f45c944906C4e61B1B91f92C55B06E3606



3. Link the contract that is associated with `kasei_crowdsale_address` to the `KaseiCoinCrowdsale` contract that you previously created by completing the following steps:
-  Copy the address that is associated with kasei_crowdsale_address.
-  Scroll up to the Contract box, and then select the compiled KaseiCoinCrowdsale.
-  Copy the address into the At Address box.
-  Click the At Address button.

![alt=""](Evaluation_Evidence/y_link_cs_add_to_contract_atAddress.png)


4. Notice the deployed KaseiCoinCrowdsale contract in the Deployed Contracts section.

- The deployed KaseiCoinCrowdsale contract address is the same with `kasei_crowdsale_address`: 0x1183f9a0680F0Ce4A7d174fE169aEdF2E8c8DA92


![alt=""](Evaluation_Evidence/y_link_cs_add_deployed_cs_contract_info.png)



5. Repeat the same process (step 3 and 4) with kasei_token_address and the KaseiCoin contract.

- Link the contract that is associated with `kasei_token_address` to the `KaseiCoin` contract that you previously created

-  Copy the address that is associated with kasei_token_address.
-  Scroll up to the Contract box, and then select the compiled KaseiCoin.
-  Copy the address into the At Address box.
-  Click the At Address button.

![alt=""](Evaluation_Evidence/y_link_token_add_to_contract_atAddress.png)




6. Notice the deployed KaseiCoin contract in the Deployed Contracts section.

- The deployed KaseiCoin contract address is the same with `kasei_token_address`: 0xB39715f45c944906C4e61B1B91f92C55B06E3606


![alt=""](Evaluation_Evidence/y_link_token_add_deployed_token_contract_info.png)


### 4. Test the KaseiCoinCrowdsale
Now you will test the KaseiCoinCrowdsale. You will assume the role of a participant seeking to buy Kasei Coins. To do so, complete the following steps:
1. Purchase Kasei Coins from the crowdsale by completing the following steps:
- Select a new account from MetaMask. Notice the new account address in the Account box in the Remix IDE. Copy this account address to the clipboard.

![alt=""](Evaluation_Evidence/y_test_select_acc11.png)

Account 11 in metamask

0xCc3c1cB89CC609158d32A8A0D26c020e3c7C329d

- In the Value box, enter a value of wei to determine the number of tokens for this account to purchase.

![alt=""](Evaluation_Evidence/y_purchase_6Wei.png)

- Navigate to the deployed KaseiCoinCrowdsale contract, paste the address into the buyTokens box, and then click the buyTokens button.

![alt=""](Evaluation_Evidence/y_purchase_input_purchaser_add.png)

![alt=""](Evaluation_Evidence/y_purchase_transact.png)

- When the MetaMask dialog box opens, click Confirm.

![alt=""](Evaluation_Evidence/y_purchase_confirm_1.png)

![alt=""](Evaluation_Evidence/y_purchase_confirm_2.png)

- Confirm that the number of purchased tokens is correctly reflected in Remix by clicking the totalSupply button.

![alt=""](Evaluation_Evidence/y_purchase_confirm_acc11_info.png)

![alt=""](Evaluation_Evidence/y_purchase_6Wei_totalSupply.png)

![alt=""](Evaluation_Evidence/y_purchase_6Wei_weiRaised.png)




2. Repeat the purchase process by using a third MetaMask address. Confirm that the total supply of tokens is correctly reflected in Remix by clicking the totalSupply button.

Purchase Kasei Coins from the crowdsale by completing the following steps:
- Select a new account from MetaMask. Notice the new account address in the Account box in the Remix IDE. Copy this account address to the clipboard.

![alt=""](Evaluation_Evidence/y_test_select_acc12.png)

Account 12 in metamask

0x86179a42901401d1e108b0071eeE81cd2F985F5E

- In the Value box, enter a value of wei to determine the number of tokens for this account to purchase.

![alt=""](Evaluation_Evidence/y_purchase_19Wei.png)




- Navigate to the deployed KaseiCoinCrowdsale contract, paste the address into the buyTokens box, and then click the buyTokens button.

![alt=""](Evaluation_Evidence/y_purchase_input_purchaser_add_acc12.png)

![alt=""](Evaluation_Evidence/y_purchase_transact_19wei.png)

- When the MetaMask dialog box opens, click Confirm.

![alt=""](Evaluation_Evidence/y_purchase_confirm_19wei.png)

- Confirm that the number of purchased tokens is correctly reflected in Remix by clicking the totalSupply button.

![alt=""](Evaluation_Evidence/y_purchase_confirm_acc12_info.png)

![alt=""](Evaluation_Evidence/y_purchase_19Wei_totalSupply.png)

![alt=""](Evaluation_Evidence/y_purchase_19Wei_weiRaised.png)

![alt=""](Evaluation_Evidence/y_transaction_info_in_ganache_after_test.png)

3. Explore other functionality that is associated with this crowdsale application.  

Check rate, token address, wallet address info

![alt=""](Evaluation_Evidence/y_cs_explore_info.png)

Check account 11's balance using balancOf() function
![alt=""](Evaluation_Evidence/y_balanceOf_acc11.png)


Check account 12's balance using balancOf() function

![alt=""](Evaluation_Evidence/y_balanceOf_acc12.png)



Test isMinter() function using kasei_crowdsale_address
![alt=""](Evaluation_Evidence/

y_other_info_crowdsale_address_isMinter.png)


---

20-02-2023
