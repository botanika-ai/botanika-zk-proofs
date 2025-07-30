# Botanika ZK-Proofs Repository

## Overview

botanika-zk-proofs is the official public repository for sharing Botanika's research, references, and structural design regarding ZK-STARK-based zero-knowledge proof systems.

**Important**: This repository does not include proprietary proving logic or any internal cryptographic implementation.

Instead, it serves as:

- A reference hub for open-source zk-STARK & zkVM projects
- A documentation portal for how Botanika leverages ZK proofs (PoSA, PoST, PoEr)
- A placeholder for future integrations and third-party collaboration

## Purpose

The Botanika network integrates zero-knowledge proofs to verify:

- Data existence (PoEr: Proof of Erasure)
- Space-time commitments (PoST: Proof of Space-Time)
- Real-time hardware availability (PoSA: Proof of Space Availability)

This repository exists to:

- Share knowledge and build trust through transparency
- Track relevant open-source advancements in the zk ecosystem
- Document the usage and role of ZK within Botanika's infrastructure
- Separate open research from proprietary codebases

## Directory Structure

```
botanika-zk-proofs/
│
├── README.md                   # Repo purpose, disclaimer, usage
├── .gitignore                  # Ignore rules (e.g., internal code)
├── .placeholder                # Marks private code area
│
├── docs/                       # Documentation explaining Botanika ZK integration
│   └── spec.md                 # High-level design of proof types and flows
│
├── zk-reference/               # Forked or linked ZK projects for learning/reference
│   ├── lightprotocol/          # Example ZK Mixer (Solana)
│   ├── nil.foundation/         # zkLLVM tools & circuits
│   ├── aztec/                  # Privacy zk-rollup
│   └── README.md               # Summary & source links
│
└── internal-prover/           # Placeholder for private zk prover engine
    └── .placeholder
```

## Private Code Handling

The actual zk-STARK proof generation, encoding, challenge logic, and Merkle structure computation used in Botanika's production nodes are private and proprietary.

This repository includes:

- `.placeholder` files in `internal-prover/` to indicate reserved space
- `.gitignore` rules to prevent accidental leakage
- Explicit README and doc mentions to avoid confusion

## ZK Project References

The `zk-reference/` directory includes educational or architectural references, either by:

- Forking public zk repositories
- Cloning them with submodule or subtree
- Or linking in a central README.md with descriptions

Examples:

| Project | Focus | Source |
|---------|-------|--------|
| Light Protocol | Solana ZK Mixer | https://github.com/lightprotocol/lightprotocol |
| Aztec Protocol | zk-rollup, privacy circuits | https://github.com/AztecProtocol/aztec-packages |
| zkLLVM (Nil) | zk-STARK toolchain | https://github.com/NilFoundation/zkLLVM |
| Plonky2 | Recursive STARK prover | https://github.com/mir-protocol/plonky2 |

These serve as inspiration and structure reference, not direct implementation in Botanika.

## Documentation: docs/spec.md

This document outlines:

- The 3-tier proof system used by Botanika:
  - PoSA (availability)
  - PoST (space-time)
  - PoEr (erasure)
- The Merkle-based challenge design
- How these proofs tie into:
  - Solana staking program
  - zk-STARK backend verifier
  - Reward & slashing logic
- How Botanika integrates zkProofs into its consensus integrity layer

## Intended Audience

This repository is intended for:

- Researchers and collaborators studying Botanika's approach
- Prospective contributors to zk-related tools or protocol extensions
- Auditors reviewing our proof scheme transparency (minus internal code)
- Anyone interested in zk-STARK-based L2 or storage integrity models

## Not Included

To avoid legal, security, and implementation risk:

- No proving key or STARK parameter setup
- No internal ZK code or circuits
- No deployment of Botanika ZK backend
- No reward distribution logic

## Setup Instructions

If you wish to explore the referenced code:

```bash
git clone https://github.com/botanika-ai/botanika-zk-proofs.git
cd botanika-zk-proofs
cd zk-reference/lightprotocol
# Or use submodules if configured
```

To contribute to docs:

```bash
cd docs/
nano spec.md
```

## Contact

Interested in collaborating, auditing, or learning more?

Reach out:
- Email: zk@botanika.ai
- Website: https://botanika.ai
