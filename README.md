# Create A Token

This Solidity program is used to create a token that demonstrate the data types, mapping, functionality, and conditional statements of a contract. The purpose of this project is to show how to create your own token.

## Description

This program is a contract named MyToken in Solidity. The contract has a public variable that has the details about your coin and it need to have mapping of addresses to balances. The contract has two function, the mint function takes two parameters which is the address and the value. It increases the total supply by that number and increases the balance of the address by that amount. While the burn function also has two parameters the address and the value that will deduct the value from the total supply and from the balance of the address.

## Getting Started

### Executing program

- To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

- Once you are on the Remix website, create a folder  by clicking on the "folder" icon in the left-hand sidebar. Then create a new file and name it,  save the file with a .sol extension. Copy and paste the following code into the file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public TokenName = "Tiffany";
    string public TokenAbbrv = "Tffy";
    uint public TotalSupply = 0;
    
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public{
       TotalSupply += _value;
       balances[_address] += _value;
    }
    // burn function
   function burn (address _address, uint _value) public{
      if (balances[_address] >= _value) {
      TotalSupply -= _value;
      balances[_address] -= _value;
      }
   }
}

```

- To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

- Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

- Once the contract is deployed, you can interact with it by calling the TokenName, TokenAbbrv, TotalSupply, Balances. Click the dropdown of mint and you can copy the sample address in the account and add a number for the value. Finally, click the "transact" button to execute and you will have the total amount of balances of your token.  You can do the same thing with burn function. 
## Authors

Tiffany Faith Dalaya
[8214150@ntc.edu.ph] 

## License

This project is unlicensed.
