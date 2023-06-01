# ERC20_Token_Creation
 A Solidity smart contract for a custom token called "MyToken".

## Description
How to use require, revert and assert methods in SmartContracts. Each examples tries to explain the use of these method through used cases like Vending Machine, Voterlist and others. 

## Getting Started
 Let's go through the code step by step to understand its functionality.
 
**import "@openzeppelin/contracts/token/ERC20/ERC20.sol";** <sub>This line imports the ERC20 contract from the OpenZeppelin library. The ERC20 contract is a widely-used standard for creating fungible tokens on the Ethereum blockchain.</sub>

**import "@openzeppelin/contracts/access/Ownable.sol";:* <sub> This line imports the Ownable contract from the OpenZeppelin library. The Ownable contract provides a basic implementation of access control, allowing the contract owner to restrict certain functions to themselves.</sub>

`contract MyToken is ERC20, Ownable {}:` <sub>This line defines the MyToken contract and specifies that it inherits from both ERC20 and Ownable contracts. This means that the MyToken contract will have all the functionalities of ERC20 and Ownable contracts.</sub>

`constructor(string memory tokenName, string memory tokenSymbol, uint8 tokenDecimals, uint256 initialSupply) ERC20(tokenName, tokenSymbol) {}:`
<sub> This is the constructor function of the MyToken contract. It takes four parameters: tokenName (the name of the token), tokenSymbol (the symbol or ticker of the token), tokenDecimals (the number of decimal places the token supports), and initialSupply (the initial supply of the token). The constructor calls the constructor of the ERC20 contract, passing the tokenName and tokenSymbol as arguments. It then mints the initial supply of tokens and assigns them to the contract deployer's address.</sub>

`function mint(address account, uint256 amount) public onlyOwner {}:`
<sub>This function allows the contract owner to mint new tokens. It takes two parameters: account (the address to which the newly minted tokens will be assigned) and amount (the number of tokens to mint). Only the contract owner (the address that deployed the contract) can call this function, as indicated by the onlyOwner modifier. The function uses the internal _mint function inherited from the ERC20 contract to create new tokens and assign them to the specified account.</sub>

`function transfer(address recipient, uint256 amount) public override returns (bool) {}:`
<sub>This function overrides the transfer function inherited from the ERC20 contract. It allows token holders to transfer their tokens to another address. It takes two parameters: recipient (the address to which the tokens will be transferred) and amount (the number of tokens to transfer). The function calls the internal _transfer function inherited from the ERC20 contract to perform the token transfer and returns a boolean value indicating the success of the transfer.</sub>

`function burn(uint256 amount) public {}:`
<sub>This function allows token holders to burn (destroy) a specific amount of their own tokens. It takes one parameter: amount (the number of tokens to burn). The function calls the internal _burn function inherited from the ERC20 contract to burn the specified amount of tokens owned by the caller.</sub>

### Executing program
* Head on to RemixIDE* https://remix.ethereum.org/
* Install HardHat in local environment* https://hardhat.org/getting-started/#connecting-a-wallet-or-dapp-to-hardhat-network
* Install Local RemixIDE annd Configure it* https://www.npmjs.com/package/@remix-project/remixd
* Select Local host as workspace in file explorer
* Enable Hardhat Compilation in Solidty Compiler
* Deploy and run the Contract Functions

## Help

Connect to me at khanayubchand@gmail.com

## Authors

Contributors names and contact info
Ayub Khan  
Discord: Userid - Aykha#7280


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
