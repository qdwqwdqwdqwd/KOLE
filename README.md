# KOLE - KOL Misconduct Exposure Platform

The KOLE repository curates documentation and structured data for a decentralized platform that records and exposes Key Opinion Leader (KOL) misconduct. This project emphasises verifiable evidence handling, transparent governance, and bilingual (English/Chinese) communication.

## Overview
KOLE combines Solana smart contracts with IPFS storage to maintain tamper-resistant misconduct records. This repository contains the canonical whitepapers, community playbooks, and release metadata that define the ecosystem.

## Repository Structure
- `docs/` – Source of truth for the English and Chinese whitepapers plus community procedure guides.
- `data/` – Machine-readable knowledge base (`知识库.json`) with versioning, release history, and governance parameters.
- `AGENTS.md` / `CLAUDE.md` – Agent-specific contributor guidance.
- `.env` – Local development variables; do not commit real credentials.

## Key Documents
| Resource | Description |
| --- | --- |
| `docs/KOL Misconduct Exposure Platform Whitepaper.md` | English specification of the platform goals, architecture, and roadmap. |
| `docs/KOL劣迹曝光平台白皮书.md` | Chinese translation of the whitepaper for local stakeholders. |
| `docs/社区资料.md` | Detailed community governance, submission processes, and reward rules. |
| `data/知识库.json` | Structured metadata used to sync versions, release notes, and tokenomics. |

## Quick Start
1. Clone the repository and switch into the project directory.
2. Install Markdown linting (`npm install -g markdownlint-cli`) and ensure `jq` is available.
3. Run `npx markdownlint-cli README.md docs/**/*.md` to validate Markdown style.
4. Run `jq '.' data/知识库.json` before committing changes to the knowledge base.
5. Preview documentation locally with `python3 -m http.server 8000` and open `http://localhost:8000`.

## Data & Versioning
- Update `metadata_version` and `last_updated` in `data/知识库.json` whenever publishing new releases.
- Keep whitepaper version strings aligned with the metadata file.
- Record major roadmap shifts inside both the whitepaper and the knowledge base for consistency.

## Contributing
- Review `AGENTS.md` for repository-wide workflows and validation steps.
- Coordinate bilingual updates by editing the English and Chinese documents in tandem.
- Use imperative, concise commit messages (e.g., `Update governance incentive table`).
- Open pull requests with a summary of affected files, validation commands executed, and any localisation follow-ups needed.

## Status & Roadmap
The current whitepaper version is 1.2 (September 2025), outlining phases from foundational evidence submission through DAO-driven governance and cross-chain expansion. Refer to the roadmap section of each whitepaper for milestone details.

## Disclaimer
KOLE remains under active development. Documentation in this repository is informational and may change as the smart contracts, incentive models, and governance processes evolve.
