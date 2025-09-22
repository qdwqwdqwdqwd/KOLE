# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**KOLE (KOL Exposure Platform)** - A decentralized blockchain-based platform for exposing and documenting misconduct by Key Opinion Leaders (KOLs).

### Key Technologies
- **Blockchain**: Solana for immutable record storage
- **Storage**: IPFS for distributed evidence storage
- **Token**: KOLE token for platform governance and incentives
- **Language**: Platform documentation in Chinese (劣迹曝光平台) and English

## Repository Structure

```
/
├── data/           # Platform data and knowledge base
│   └── 知识库.json  # Structured knowledge base with platform metadata
├── docs/           # Platform documentation
│   ├── whitepapers/                     # Whitepaper documents
│   │   ├── Whitepaper_CN.md            # Chinese whitepaper
│   │   ├── Whitepaper_EN.md            # English whitepaper
│   │   └── Whitepaper_*.md             # Other language whitepapers
│   └── 社区资料.md                      # Detailed community mechanisms
└── .history/       # Version control history for sensitive files
```

## Core Platform Mechanisms

### 1. Evidence Submission & Review System
- **Anonymous/Real-name submission** of KOL misconduct evidence
- **Decentralized review panel** with 3+ independent reviewers
- **Consensus-based approval** requiring unanimous agreement
- **1-5 severity rating system** for misconduct classification

### 2. Blockchain Storage Architecture
- **IPFS integration** for evidence file storage with unique hash generation
- **Solana smart contracts** for metadata and review records
- **Immutable on-chain records** including:
  - Evidence hash references
  - KOL information and event descriptions
  - Review results and timestamps
  - Reviewer identifications

### 3. Token Economy (KOLE)
- **Reward Distribution**:
  - First report: 100,000 KOLE
  - Supplementary evidence: 20,000 KOLE
  - Review participation: 50,000 KOLE
- **Token burning mechanism** for deflationary supply
- **Governance voting** requires KOLE staking

### 4. Community Governance
- **DAO structure** for platform decisions
- **Reviewer election** through community voting
- **Threshold-based decision making** (e.g., 80% approval for major changes)

## Development Guidelines

### Working with Documentation
- Primary documentation is in **Chinese (中文)**
- English translations available for whitepapers
- Use `知识库.json` as the single source of truth for platform metadata

### Key Data Structures
The `data/知识库.json` contains:
- Platform metadata and versioning
- Technical architecture details
- Token economics specifications
- Governance rules and thresholds
- Development roadmap milestones

### Git Remote Configuration
- **origin**: AI-OCR-BOOK repository (legacy)
- **kole**: Primary KOLE platform repository at `https://github.com/qdwqwdqwdqwd/KOLE.git`

Use `git push kole main` to push changes to the KOLE repository.

## Important Considerations

### Security & Privacy
- Platform supports **anonymous submissions** to protect whistleblowers
- Evidence files stored on **IPFS** are public but tamper-proof
- Review process uses **blind evaluation** to prevent bias

### Blockchain Integration
- **Solana** chosen for high throughput and low transaction costs
- Smart contracts handle:
  - Evidence hash storage
  - Token distribution
  - Governance voting
  - Review result recording

### Platform Phases
1. **Phase 1**: Core submission and review system
2. **Phase 2**: Token economy implementation
3. **Phase 3**: Full DAO governance activation
4. **Phase 4**: Cross-chain expansion and API development

## Common Tasks

### Updating Platform Documentation
1. Edit markdown files in `/docs/` directory
2. Update `知识库.json` if structural changes are made
3. Maintain bilingual consistency between Chinese and English versions

### Working with Platform Data
- JSON knowledge base at `data/知识库.json` contains all platform specifications
- Use this file for consistent platform information across all documentation

### Version Control
- The `.history/` directory tracks sensitive file changes
- Use meaningful commit messages describing platform feature updates