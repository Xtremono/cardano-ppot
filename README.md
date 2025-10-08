# Cardano Perpetual Powers of Tau Ceremony

## Overview

The **Cardano Perpetual Powers of Tau** is a cryptographic trusted setup ceremony designed to generate secure public parameters for Zero-Knowledge proof systems on the Cardano blockchain. This ceremony constructs partial zk-SNARK parameters for circuits up to depth 2^23 (~8 million constraints) using the **BLS12-381 elliptic curve**, which is the cryptographic foundation used by Cardano.

### Objective

Generate trustworthy public parameters that enable the secure operation of Zero-Knowledge applications in the Cardano ecosystem. The ceremony ensures that no single party controls the final parameters, providing long-term security guarantees for zk-SNARK protocols.

> **Security Principle**: As long as one participant behaves honestly and destroys their secret randomness ("toxic waste"), the entire setup remains secure and trustworthy.

## Contribution Guidelines

You can find more information about how to contribute in our [contribution guidelines](./Docs/Ceremony_&_Contribution_Guidelines.md)

## Registration and Communication

To participate you must:

* Send a request in the [registration form](https://form.typeform.com/to/a5Vo7WI7)
* Join our [Discord Channel](https://discord.gg/zrER4zPF)

## Ceremony Progress

| Round | Participant | Status | Contribution Hash | Attestation |
|-------|-------------|---------|------------------|-------------|
| 0000  | Coordinator | ✅ Complete | `initial_challenge` | [Genesis Parameters](ceremony-transcripts/round_0000.txt) |
| 0001  | TBD | 🕒 Pending | - | - |
| 0002  | TBD | ⏳ Scheduled | - | - |
| 0003  | TBD | ⏳ Scheduled | - | - |
| ...   | ...         | ⏳ Scheduled | - | - |

**Target**: 40+ verified contributions  
**Current**: 1/40 (Genesis only)  
**Timeline**: Q4 2025 - Q1 2025

## Ceremony Process

### 1. **Initialization**
The coordinator generates the initial challenge file containing the starting Powers of Tau parameters.

### 2. **Contribution Phase**
Each participant:
- Downloads the current challenge file (~9GB)
- Adds their secret randomness to extend the tau powers
- Generates a response file with their contribution
- **Destroys their secret input** (critical for security)

### 3. **Verification**
The coordinator verifies each contribution's mathematical correctness before incorporating it into the next challenge.

### 4. **Finalization**
After all contributions, a public beacon (unpredictable randomness source) is applied to ensure that even if all participants colluded, the final parameters remain secure.

### 5. **Final Parameters**
The ceremony produces a Common Reference String (CRS) ready for use in Zero-Knowledge proof systems across the Cardano ecosystem.

## Logistics

### Hardware Requirements
- **RAM**: Minimum 16GB (recommended 32GB)
- **Storage**: 20GB available space
- **CPU**: Multi-core processor (contribution takes 3-4 hours)
- **Network**: Stable internet for 9GB downloads/uploads

### Coordination
- **Communication**: Official Twitter/X updates and GitHub repository
- **Registration**: Public form for contributor sign-up
- **Scheduling**: Organized time slots to prevent overlaps
- **Support**: Technical assistance via official channels

### Reward Structure
- **Regular Contributors**: Receive ADA rewards after ceremony completion
- **Ad-honorem Contributors**: Participate voluntarily to strengthen security
- **Test Transaction**: Reward infrastructure tested before distribution

## Participation

### Prerequisites
- Linux, macOS, or Windows system
- Node.js (≥22.17.1) and pnpm (≥9.0.0)
- GitHub account for contribution records
- Basic command-line familiarity

### Quick Start
```bash
# Install the CLI
git clone https://github.com/NicoSerranoP/brebaje.git
cd brebaje/apps/cli
chmod +x install.sh && ./install.sh

# Configure your identity
brebaje-cli config name "Your Full Name"
brebaje-cli config ceremony-repo https://github.com/YOUR-USERNAME/ceremony-repo-fork

# Contribute automatically (when scheduled)
brebaje-cli ppot auto-contribute ceremony-urls.json
```

### Security Guidelines
- ⚠️ **Critical**: Delete all secret randomness after contributing
- 🔒 Keep your contribution files as proof of participation
- 📱 Share your contribution on social media for transparency
- 🔐 Use secure, unpredictable entropy sources for randomness

## Technical Details

- **Elliptic Curve**: BLS12-381 (Cardano native)
- **Circuit Depth**: 2^24 constraints (~16M)
- **Challenge Size**: ~9GB per round
- **Ceremony Type**: Perpetual (ongoing security)

## Repository Links

- **🏠 Main Repository**: [brebaje](https://github.com/NicoSerranoP/brebaje)
- **📖 CLI Documentation**: [Ceremony Guidelines](./Docs/Ceremony_&_Contribution_Guidelines.md)
- **🔧 CLI Installation**: [Installation Guide](./Docs/Ceremony_&_Contribution_Guidelines.md#installation-instructions)
- **📊 Ceremony Transcripts**: Coming Soon
- **🐛 Issue Tracker**: [Report Issues](https://github.com/NicoSerranoP/brebaje/issues)

## Contributing

1. **Register**: Sign up via the official registration form
2. **Prepare**: Install the CLI and configure your setup
3. **Schedule**: Receive your contribution time slot
4. **Contribute**: Follow the automated contribution process
5. **Verify**: Submit your attestation and pull request

---

## About

This ceremony is organized by the Cardano community to enable the CRS for Zero-Knowledge applications.

**Questions?** Check our [troubleshooting guide](./Ceremony_&_Contribution_Guidelines.md#troubleshooting) or contact the ceremony coordinators.

---

*Last updated: October 2025 | Ceremony Status: In Progress*