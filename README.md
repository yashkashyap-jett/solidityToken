# Project Title

This solidity program aims at demonstrating the functionality of Tokens using the basic syntax and functionality of the Solidity programming language.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has functions like mint and burn. Mint function is used to increase the total supply by the number passed and increases the balance of the address by that amount. Burn function is used to decrease the total supply by the number passed and decreases the balance of the address by that amount.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;
contract MyToken {

    // public variables here
    string public tokenName;
    string public tokenAbbrv;
    uint public totalSupply;
    constructor()
    {
        tokenName="Ethereum";
        tokenAbbrv="ETH";
        totalSupply=0;
    }
    // mapping variable here
    mapping (address=>uint) public balances;
    // mint function
    function mint(address ad , uint value) public 
    {
        totalSupply+=value;
        balances[ad]+=value;
    }

    // burn function
    function burn(address _ad , uint _value) public 
    {
        if(totalSupply>=_value)
        {
            totalSupply-=_value;
            balances[_ad]-=_value;
        }
    } 
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "MyToken" contract in the left-hand sidebar.

After that you can see the "tokenName", "tokenAbbrv", and the "totalSupply". Then we have "mint" and "burn" function. click on the "mint" or "burn" function and pass the adress and the value by which you want to increase the supply. Finally, click on the "transact" button to execute the function and you will see the changes in the totalSupply and the balance at the particular address. You can check the balance of a particular adress by clicking on "balances" and then passing the address and you will se the balance of that address.

## Authors

Yash Kashyap
https://www.linkedin.com/in/yash-kashyap-3a8a2524b/


