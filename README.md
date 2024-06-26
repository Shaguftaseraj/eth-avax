# Title : Comprehensive Error Handling in Solidity: Demonstrating require(), assert(), and revert() Statements.

## Overview :
Using the require(), assert(), and revert() commands, this Solidity smart contract illustrates thorough error handling. It guarantees appropriate balance management and has features that are exclusive to the contract owner for depositing and withdrawing money. The purpose of assert() is to catch unexpected problems by checking invariants, whereas require() statements validate inputs and conditions. Unauthorized ether transfers are rejected by the fallback and receive functions using revert(), whereas the reset method resets the balance to zero. This contract is a useful example of robust error handling in smart contract development, since it also includes a testAssertFailure method that shows how assert() might fail under specified scenarios.

## Key Features :

1. Owner-Only Access Control:

    * Functions like deposit, withdraw, and reset are restricted to the contract owner, enhancing security by ensuring only authorized actions.

2. Comprehensive Error Handling:

   * Utilizes require() to validate inputs and ensure conditions are met before executing functions.
   
   * Uses assert() to enforce invariants, ensuring internal consistency and detecting logic errors.
   
   * Employs revert() in fallback and receive functions to handle and reject unexpected ether transfers.

3. Balance Management:

    * Allows the owner to deposit and withdraw funds, maintaining an internal balance and ensuring it never becomes negative.
    
4. Reset Functionality:

    * Provides a reset function to zero out the contract’s balance, demonstrating control over the contract's state.
      
5. Demonstration of assert() Failure:

    * Includes testAssertFailure to show how assert() can be used to catch conditions that should never occur, serving as a practical example for error detection.
   
6. Fallback and Receive Function Handling:

    * Implements fallback and receive functions to ensure that unauthorized ether transfers to the contract are rejected, preventing unexpected behavior.
  
7. Public View Function:

    * Offers a getBalance function to allow public access to the current balance, demonstrating read-only state inspection.

The code serves as a helpful teaching tool for learning error management in decentralized systems because of these characteristics, which together demonstrate how to construct and handle mistakes
in a Solidity smart contract.

# Start Execution :

Use the Remix IDE Ethereum programming environment or any similar environment to implement this Solidity smart contract. To carry out actions like deposit, withdraw, and reset, confirm that you are the deployer (owner). Utilizing the features offered, keep an eye on balance adjustments and confirm mistake handling.

## Step-by-Step Process : 

1. Open Remix IDE:
   
    * Visit Remix IDE in your web browser.
      
2. Create a New File:
   
   * Click on the "File Explorer" tab on the left panel.
     
   * Click the "+" icon or "Create New File" button.
     
         Name your file (e.g., ErrorHandling.sol).
     
3. Paste the Smart Contract Code:
   
   * Copy the smart contract code and paste it into the newly created file.

   * Click the link ( https://github.com/Shaguftaseraj/eth-avax/blob/main/errorHandling ) and copy paste the code.

4. Compile the Contract:
   
   *  Go to the "Solidity Compiler" tab on the left panel.
     
   * Ensure the correct Solidity version (0.8.9) is selected.
     
   * Click the "Compile ErrorHandling.sol" button. Fix any warnings or errors if they appear.
     
5. Deploy the Contract:
   
     * Navigate to the "Deploy & Run Transactions" tab.
    
     * Ensure "Remix LLondon (VM) " is selected in the "Environment" dropdown.
    
     * Click the "Deploy" button under the ErrorHandling contract.
    
6. Interact with the Deployed Contract:
   
     * Once deployed, the contract instance appears under "Deployed Contracts."
    
7. Expand the contract instance to view available functions:
   
       deposit: Input an amount and click to deposit (only the owner can deposit).
   
       withdraw: Input an amount and click to withdraw (only the owner can withdraw).
   
       reset: Click to reset the balance to zero.
   
       getBalance: Click to view the current balance.
   
       testAssertFailure: Click to test assert() failure (it will fail if the balance is zero).
   
8. Monitor the Output:
    
    * View transaction results in the Remix console and observe balance changes.
    
    * If errors occur (e.g., unauthorized access or invalid operations), check the console for error messages.
    
9 . Testing Fallback and Receive:

   *  Attempt to send ether directly to the contract address from the "Remix London (VM) " environment .
     
   *  Observe the transaction failure due to the revert() statements in the fallback and receive functions.

# Authors :

=> Shagufta Seraj

Github : https://github.com/Shaguftaseraj


# License : 

The Project is licensed under the MIT License - see the link ( https://github.com/Shaguftaseraj/eth-avax/blob/main/LICENSE ) for details.
