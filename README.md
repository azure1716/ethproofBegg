##Project title
AZURE Token (AZUR)

#Simple Overview
The AZURE Token (AZUR) is a basic ERC-20-like token implemented on the Ethereum blockchain. It includes functionalities to mint and burn tokens, while also providing a secure way to manage token balances.

#Description
The AZURE Token (AZUR) project is a straightforward smart contract developed using Solidity, designed to demonstrate fundamental concepts of token creation and management on the Ethereum blockchain. This project aims to provide a basic understanding of how tokens work, focusing on the core functionalities of minting and burning tokens.

The contract includes public variables to store the token's name, abbreviation, and total supply, allowing for easy access to this information. It also uses a mapping to keep track of the balance of each address. The mint function enables the contract owner to increase the total supply and the balance of a specified address, simulating the creation of new tokens. Conversely, the burn function allows any address to destroy a specified amount of tokens from their balance, provided they have sufficient tokens, thereby reducing the total supply.

Security and access control are integral parts of the contract. Only the owner of the contract has the authority to mint new tokens, ensuring that token creation is controlled and secure. The use of Solidity's require statement ensures that token burns can only occur if the address has enough tokens to burn, preventing unauthorized token destruction.

Overall, the AZURE Token (AZUR) project serves as an educational tool for understanding token economics and smart contract development on the Ethereum blockchain. It provides a simple yet effective foundation for anyone interested in exploring the world of decentralized finance (DeFi) and blockchain technology.

##Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a.sol extension (e.g., project.sol). Copy and paste the following code into the file:


// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {

    // public variables here
    string public tokenName="AZURE";
    string public tokenAbbrv="AZUR";
    uint public totalSupply= 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address add, uint val) public {
        totalSupply += val;
        balances[add] += val;
    }

    // burn function
    function burn (address add, uint val) public {
        if(balances[add] >= val){
            totalSupply -= val;
            balances[add] -= val;
        }
    }

}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.7" (or another compatible version), and then click on the "Compile project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling both the functions.

##Author
HARSH KUMAR SHARMA STUDENT CHANDIGARH UNIVERSITY
