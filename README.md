Contract myToken
This is a simple Solidity contract for a token called "Meta" with the abbreviation "MTA". The contract has two public variables, tokenName and tokenAbbrv, which store the name and abbreviation of the token, respectively. The totalSupply variable stores the total number of tokens in circulation.

Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.The contract also has a mapping variable.The contract has two functions: mint and burn. The mint function takes in an address and a value, and adds the value to the total supply and to the balance of the specified address. The burn function takes in an address and a value, and subtracts the value from the total supply and from the balance of the specified address, if the balance is greater than or equal to the value.

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the following code into the file: javascript pragma solidity ^0.8.18;

contract MyToken {

string public tokenName = "Meta";
string public tokenAbbrv = "MTA";
uint public totalSupply = 0;

mapping(address => uint) public balances;

function mint(address _address, uint _value) public {
    totalSupply += _value;
    balances[_address] += _value;
}

function burn(address _address, uint _value) public {
    if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile contract mytoken.sol" button. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "contract mytoken" contract from the dropdown menu, and then click on the "Deploy" button.

Authors
Sahil Kumar

License
This project is licensed under the MIT License - see the LICENSE.md file for details
