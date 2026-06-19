# Scavenger Hunt — Smart Contracts

Cairo smart contracts powering the on-chain game logic for the StarkNet scavenger hunt. This includes puzzle management, player progress, NFT rewards, challenge management, referral rewards, zero-knowledge proof verification, and real-time event emission.

## Tech Stack

- **Language:** Cairo
- **Blockchain:** StarkNet
- **Package Manager:** Scarb
- **Testing Framework:** Starknet Foundry (`snforge`)

## Contracts

| Contract | Description |
|----------|-------------|
| `PuzzleNFT` | ERC-721 NFT minting and management for puzzle rewards |
| `PuzzleSystem` | Core puzzle mechanics — solving, scoring, state management |
| `SystemIntegration` | Coordinates interactions between all contracts |
| `challenge_manager` | Creates, manages, and tracks on-chain challenges |
| `game_management` | Top-level game state, seasons, and configuration |
| `nft_rewards` | NFT reward distribution logic for completed challenges |
| `player_progress` | Tracks per-player puzzle completions and scores |
| `puzzle_event_emitter` | Emits StarkNet events for puzzle and challenge actions |
| `referral_rewarder` | Manages referral codes and distributes referral rewards |
| `social_metadata` | Stores social/profile metadata linked to players |
| `zk_verifier` | Verifies zero-knowledge proofs for solution submissions |

## Getting Started

### Prerequisites

- [Scarb](https://docs.swmansion.com/scarb/) (Cairo package manager)
- [Starknet Foundry](https://foundry-rs.github.io/starknet-foundry/) (`snforge` / `sncast`)

### Build

```bash
scarb build
```

### Running Tests

```bash
snforge test
```

## Project Structure

```
src/
├── lib.cairo                   # Module declarations
├── PuzzleNFT.cairo             # NFT contract
├── PuzzleSystem.cairo          # Core puzzle logic
├── SystemIntegration.cairo     # Cross-contract coordinator
├── challenge_manager.cairo     # Challenge lifecycle
├── game_management.cairo       # Game state & seasons
├── nft_rewards.cairo           # Reward distribution
├── player_progress.cairo       # Player on-chain progress
├── puzzle_event_emitter.cairo  # Event emission
├── referral_rewarder.cairo     # Referral rewards
├── social_metadata.cairo       # Player social data
└── zk_verifier.cairo           # ZK proof verification

tests/
├── test_challenge_manager.cairo
├── test_game_management.cairo
├── test_nft_rewards.cairo
├── test_player_progress.cairo
├── test_puzzle_system.cairo
├── test_referral_rewarder.cairo
├── test_system_integration.cairo
└── test_zk_proof.cairo
```

## Related Repositories

- [scavenger-hunt-backend](https://github.com/LadderMine/scavenger-hunt-backend) — NestJS API server
- [scavenger-hunt-frontend](https://github.com/LadderMine/scavenger-hunt-frontend) — Next.js web interface

## License

MIT