Token creation:-

This Solidity program is a simple "Token_creation" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to create a token contract and add two function which will add and burn the token.It simply provides a basic view of how a token contract can be created and implemented.
## Description

This program is a simple token contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two function first to add value to the receiver side and second to burn the token from the sender side. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by right click ad the new file. Save the file with a .sol extension (e.g., Token_creation.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;
contract MyToken {
    string public tokenName = "Ruchi";
    string public tokenAbbrv = "MTA";
    uint public totalSupply=0;
    mapping(address => uint) public balances;

    function mint(address add,uint value) public 
    {
        totalSupply += value;
        balances[add] += value;
    }
    function burn(address add,uint value) public 
    {
        if(balances[add] >= value)
        {
            totalSupply -= value;
            balances[add] -= value; 
        }
        
    }

}
````

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.0" (or another compatible version), and then click on the "Compile Token-creation.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function or the burn function. Click on the "Token" contract in the left-hand sidebar, and then click on the "mint" function. Finally, click on the "transact" button to execute the function and add the value to the balance.Smae goes with the "burn" function but instead of adding the value it will subtract the value from the balamce of the sender.

