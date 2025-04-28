# Blockchain-Based Voting Poll

## Project Title
Blockchain-Based Voting Poll

## Project Description
A decentralized voting system built on the Stellar blockchain using Soroban smart contracts. This platform allows users to create polls, cast votes, and view results in a transparent, secure, and immutable manner. The system ensures that each eligible voter can only vote once per poll, and all voting activities are recorded on the blockchain for maximum transparency and security.

## Project Vision
Our vision is to transform traditional voting systems by leveraging blockchain technology to address key challenges in current voting methods. By implementing a decentralized voting platform, we aim to eliminate voter fraud, reduce administrative costs, increase accessibility, and provide transparent, tamper-proof record keeping.

The Blockchain-Based Voting Poll project strives to set a new standard for democratic processes by ensuring that every vote is securely recorded, easily verifiable, and immune to manipulation. This system can be applied to various scenarios ranging from organizational decision-making to public elections, providing a trustless mechanism for collective choice.

## Key Features

| Feature | Description |
|---------|------------|
| **Poll Creation** | Users can create new polls with custom titles, descriptions, and multiple voting options |
| **Secure Voting** | Each voter is authenticated through their blockchain address, ensuring one vote per address per poll |
| **Transparency** | All votes are recorded on the blockchain and can be independently verified |
| **Real-time Results** | Poll results can be viewed in real-time as votes are cast |
| **Immutable Records** | Once recorded, votes cannot be altered or deleted, ensuring integrity of the voting process |
| **Poll Management** | Poll creators can manage the lifecycle of their polls, including closing polls when voting periods end |

## Technical Implementation

The smart contract is implemented using Soroban SDK, which provides a robust framework for developing smart contracts on the Stellar blockchain. The core components include:

- **Poll Structure**: Stores poll metadata including title, description, options, and voting status
- **Vote Structure**: Records individual votes with voter address and chosen option
- **Vote Counting**: Maintains accurate counts of votes per option for each poll
- **Authentication**: Uses Soroban's authentication system to verify voter identity and prevent duplicate voting

## Contract Functions

1. **create_poll**: Creates a new poll with specified title, description, and options
2. **cast_vote**: Allows a user to cast a vote for a specific option in a poll
3. **end_poll**: Enables the poll creator to close voting on a specific poll
4. **get_poll**: Retrieves details about a specific poll
5. **get_poll_results**: Returns the current vote counts for each option in a poll

## Getting Started

### Prerequisites
- Soroban CLI
- Stellar development environment

### Installation
1. Clone the repository
2. Install dependencies
3. Build the smart contract
4. Deploy to the Stellar testnet or mainnet

### Usage Examples
```rust
// Create a new poll
let poll_id = client.create_poll(
    creator_address,
    "Should we implement feature X?",
    "Deciding on the next feature to implement in our product roadmap.",
    vec!["Yes", "No", "Needs more discussion"]
);

// Cast a vote
client.cast_vote(voter_address, poll_id, 0); // Vote for the first option

// Get poll results
let results = client.get_poll_results(poll_id);
```

## Security Considerations

The contract implements several security measures:
- Authentication requirements for poll creation and voting
- Prevention of duplicate votes
- Creator-only access for ending polls

## Future Enhancements

- Anonymous voting mechanism
- Time-limited polls
- Delegate voting rights
- Multi-signature poll creation
- Integration with identity verification systems
- Support for weighted voting

## Contract Details
Contract Address: CDD5BY64APV4ZBABIX3BS2GE7DIP5BPTFJNRPMR6U2NWBFP4IQ3BPQFS

## License
This project is licensed under the MIT License - see the LICENSE file for details.
