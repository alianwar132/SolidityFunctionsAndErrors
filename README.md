# SchoolGradingSystem Smart Contract

The `SchoolGradingSystem` smart contract manages student grades, allowing the owner to add and update grades, and anyone to view them.

## Description

This contract serves as a simple school grading system. It enables the contract owner to add and update student grades while allowing anyone to retrieve the grade for a specific student. The grades are stored securely on the Ethereum blockchain, ensuring transparency and immutability.

### Key Functionalities

1. **Add Grade**: The contract owner can add a grade for a student.
2. **Update Grade**: The contract owner can update an existing grade for a student.
3. **Get Grade**: Anyone can retrieve the grade of a student by providing their address.

## Contract Details

### State Variables

- `owner`: Stores the address of the contract owner who deployed the contract.
- `students`: A mapping that stores student addresses and their corresponding grades and existence status.

### Events

- `GradeAdded`: Emitted when a new grade is added for a student.
- `GradeUpdated`: Emitted when an existing grade is updated for a student.

### Errors

- `NotOwner()`: Thrown when a non-owner tries to perform owner-restricted actions.
- `StudentNotFound(address student)`: Thrown when attempting to access a non-existent student.
- `GradeOutOfRange(uint256 grade)`: Thrown when a grade outside the range of 0-100 is provided.

### Modifiers

- `onlyOwner`: Ensures that only the contract owner can call specific functions.

### Functions

#### `addGrade(address student, uint256 grade)`

- **Description**: Adds a grade for a student. Only callable by the owner.
- **Parameters**:
  - `student`: The address of the student.
  - `grade`: The grade to be added (must be between 0 and 100).
- **Emits**: `GradeAdded`.

#### `updateGrade(address student, uint256 newGrade)`

- **Description**: Updates the grade for an existing student. Only callable by the owner.
- **Parameters**:
  - `student`: The address of the student.
  - `newGrade`: The new grade to be updated (must be between 0 and 100).
- **Emits**: `GradeUpdated`.

#### `getGrade(address student)`

- **Description**: Retrieves the grade of a student.
- **Parameters**:
  - `student`: The address of the student.
- **Returns**: The grade of the student.
- **Errors**: `StudentNotFound`.

## Usage

### Deploying the Contract

1. Compile the contract using Remix or another Solidity compiler.
2. Deploy the contract to an Ethereum network (e.g., Rinkeby, Ropsten) using a deployment tool like Remix or Hardhat.

### Interacting with the Contract

#### Add a Grade

1. Call the `addGrade` function with the student's address and grade.
2. Example: `addGrade("0x1234567890abcdef1234567890abcdef12345678", 85)`

#### Update a Grade

1. Call the `updateGrade` function with the student's address and the new grade.
2. Example: `updateGrade("0x1234567890abcdef1234567890abcdef12345678", 90)`

#### Get a Grade

1. Call the `getGrade` function with the student's address.
2. Example: `getGrade("0x1234567890abcdef1234567890abcdef12345678")`


