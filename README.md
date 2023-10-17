# CYRILL_CreateAToken
# Project Title
# Creating a Token

Simple overview of use/purpose.
A token is established on a blockchain in order to represent, share, and manage various digital assets or rights in a distributed, secure, and open manner. This makes a variety of applications across sectors possible.

## Description

An in-depth paragraph about your project and overview of use.
Making tokens on a blockchain means making a digital item with a name, a short name, and a total amount. To make and give out these items, you need a special function, and to get rid of them, you need another special function. It's crucial that the second function checks if there are enough items to get rid of so that we don't mess up the total number of items.

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```
code blocks for commands
```
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

After you've arrived at the Remix website, start by making a fresh file. You can do this by tapping on the "+" symbol found on the left side of the screen. Make sure to save this file with a .sol extension, like "HelloWorld.sol." Below, you'll find a sample of my token's code:

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
string public tokenName = "CYRILL";
string public tokenAbbrv = "CY";
uint public totalSupply = 0;
    // mapping variable here
mapping(address => uint) public balances;
    // mint function
function mint (address token_address, uint token_value) public{
    totalSupply += token_value;
    balances[token_address] += token_value;
}
    // burn function
function burn (address token_address, uint token_value) public{
    if (balances[token_address] >= token_value){
        totalSupply -= token_value;
        balances[token_address] -= token_value;
        }
    }
}


```
To compile your code, navigate to the "Solidity Compiler" tab on the left-hand sidebar, and then select the "Compile [file_name].sol" button. After successfully compiling the code, you can deploy the contract by going to the "Deploy & Run Transactions" tab in the left-hand sidebar. Within the deployed contracts section, you'll find information on the token name, token abbreviation, and the current total supply that you've chosen.

To verify the functionality of your code, make a copy of the default address and paste it into the "mint" field. Specify the desired quantity for minting and proceed by clicking the "transact" button. You can then review the total supply. Additionally, copy the address for the balances.

Next, follow the same procedure to attempt token burning. Afterward, inspect the total supply and balances to ensure that they have decreased by the specified amount.

Finally, test to confirm that you cannot burn more tokens than you possess. In this case, the total supply and balances should remain unchanged.

Thank you!
## Authors

Cyrill James G. Dela Cruz
202010525@fit.edu.ph

