# SolidityFunctionsAndErrors
Project Purpose
The solidity-functions-and-errors project demonstrates the use of require, assert, and revert statements for error handling in Solidity smart contracts. This project aims to provide a clear example of how these statements can be utilized to enforce input validation and ensure the integrity of contract state.

Functionality
The core functionality of the FunctionsAndErrors contract is to increment a counter (evenCount) only when an even number is provided as input. The contract includes three methods to handle the input validation:

requireEvenNumber(uint number):

Uses the require statement to check if the input number is even.
Reverts the transaction with a custom error message if the number is odd.
Increments evenCount if the input is even.
assertEvenNumber(uint number):

Uses the assert statement to ensure the input number is even.
Reverts the transaction if the number is odd.
Increments evenCount if the input is even.
revertEvenNumber(uint number):

Uses an if statement combined with revert to check if the input number is even.
Reverts the transaction with a custom error message if the number is odd.
Increments evenCount if the input is even.

