# AmitERC20 Token Contract

## OVERVIEW
The "AmitERC20" token is a simple, ERC20-compliant token built with OpenZeppelin's secure smart contract library.
It includes basic functionalities such as minting new tokens by the owner, burning tokens by any holder, and transferring ownership to a new address.
The token has a fixed decimal value of 10, ensuring precise transactions of the user.
## FEATURES
Minting: Owner can mint new tokens, increasing the supply.
Burning: Token holders can burn their tokens, reducing the supply.
Ownership Transfer: Owner can transfer ownership to a new address.
Decimals: Token has a fixed decimal value of 10 for precise transactions.
ERC20 Compliance: Fully compliant with the ERC20 standard for compatibility.
Event Logging: Emits events for minting, burning, and ownership transfers.
# CONTRACT DETAILS

## VARIABLES
address public owner: Stores the address of the contract owner.
## MODIFIER
onlyOwner: Restricts access to certain functions to only the contract owner.
## CONSTRUCTOR
constructor() ERC20("AMIT", "AJ") {
    owner = msg.sender;
    _mint(owner, 100 * 10**decimals());
}
Initializes the contract: Sets the deployer as the owner.
Mints initial supply: Mints 100 tokens with 10 decimals to the owner's address
## FUNCTION
constructor(): Initializes the contract, setting the deployer as the owner and minting an initial supply of tokens.
decimals(): Returns the number of decimal places the token uses (fixed at 10).
mintTokens(address to, uint256 value): Allows the owner to mint new tokens to a specified address.
burn(uint256 amount): Allows token holders to burn a specified amount of their tokens.
transferTokens(address to, uint256 amount): Transfers tokens from the caller to a specified address.
transferOwnership(address newOwner): Allows the owner to transfer contract ownership to a new address.
transfer(address to, uint256 amount): Overrides the ERC20 transfer function to include custom logic.
transferFrom(address from, address to, uint256 amount): Overrides the ERC20 transferFrom function to include custom logic.
# USAGE

## DEPLOYEMENT
Deploy the contract using your preferred method (e.g., Remix, Truffle, Hardhat).
Provide the initialSupply as a constructor argument.
## MINTING TOKEN
The contract owner can mint new tokens to any address using the mint function.
mint(address to, uint256 amount);
## BURNING TOKEN 
Any token holder can burn their own tokens using the burn function.
burn(uint256 amount);
## TRANSFERING TOKEN
Tokens can be transferred using the standard ERC20 transfer function or the custom transferAmount function.
transfer(address to, uint256 amount);
transferAmount(address to, uint256 amount);
# LICENCE
This project is licensed under the MIT License.


