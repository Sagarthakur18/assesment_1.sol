# Create a Token

The Sagar_token contract is a simple ERC-20-like token on the Ethereum blockchain. It allows you to print and burn tokens with public variables to keep track of token names, abbreviations, and shares. It also ensures that addresses are mapped to their respective token balances.

## Description

The Sagar_token contract is a basic implementation of a cryptocurrency token on the Ethereum blockchain. This contract, written in Solidity, allows the creation, management, and destruction of tokens. The key features include:

*Public Variables: The contract stores the token's name (Trustcoin), abbreviation (TRT), and total supply.
*Address Balances: A mapping of addresses to their respective token balances, allowing for easy tracking and management of token holdings.
*Mint Function: Enables the creation of new tokens. When invoked, it increases the total supply and allocates the specified number of tokens to a given address.
*Burn Function: Allows for the destruction of tokens. It decreases the total supply and the balance of the specified address, ensuring that the address has enough tokens to burn before performing the operation.

This contract provides a foundational framework for developing a token system, which can be further expanded with additional features and functionalities as needed.

## Getting Started

### Installing
To download the code, you can visit the following file path:-  [] (https://github.com/Sagarthakur18/assesment_1.sol/blob/main/assesment_1.sol)


### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Meta.sol). Copy and paste the following code into the file: contract MyToken {

// public variables here
string public tokenName = "Trustcoin";
string public tokenAbb = "TRT";
uint public totalSupply = 0;

// mapping variable here
mapping(address=>uint) public bal;

// mint function
function mint(address _address, uint _value) public{
    totalSupply += _value;
    bal[_address] += _value;

}
// burn function
function burn(address _address, uint _value) public{
    if(bal[_address]>= _value){
        totalSupply -= _value;
        bal[_address] -= _value;
    } 

} }


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile Meta.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you will set the value and address in right side under the MyToken contract. After initializing the value use the function mint and burn to check the working of code.



## Authors

Sagar Thakur 
@sagar_thakur_0613





## License

This project is licensed under the MIT License - see the LICENSE.md file for details
