# 📊 KOLE Platform Diagrams Viewer Guide

## 🚨 Mobile Viewing Issues

If you're viewing this on mobile and diagrams aren't rendering, here are your options:

### Quick Solutions:

1. **🖥️ Switch to Desktop Mode**
   - On mobile browser: Menu → "Request Desktop Site"
   - This enables full GitHub rendering

2. **💻 Use a Computer**
   - Best experience for viewing technical documentation
   - All diagrams will render properly

3. **🔗 Use These Direct Links**
   - [Mermaid Live Editor - View All Diagrams](https://mermaid.live)
   - Copy the Mermaid code and paste it there

4. **📱 Alternative Mobile Apps**
   - **GitHub Desktop** (if available for your device)
   - **Working Copy** (iOS)
   - **MGit** (Android)

## 📸 Static Diagram Versions

Since Mermaid diagrams don't render on mobile, here are text descriptions:

### 1. System Architecture (README.md)
```
Frontend Layer:
├── Web Application (React + TypeScript)
├── Mobile App (React Native)
└── REST API (Node.js)
    ↓
Service Layer:
├── Authentication Service
├── Review Engine
├── Reward Distribution
└── IPFS Service
    ↓
Blockchain Layer:
├── Smart Contracts (Rust/Solana)
├── KOLE Token (SPL Standard)
└── DAO Governance
    ↓
Storage Layer:
├── IPFS (Evidence Storage)
├── Solana (Metadata & Hashes)
└── Redis Cache (Performance)
```

### 2. Evidence Submission Flow (Whitepaper)
```
User Flow:
1. User discovers KOL misconduct
2. Collects evidence materials
3. Choose submission method:
   → Anonymous: Generate anonymous ID
   → Real-name: Verify identity
4. Upload evidence files to IPFS
5. Generate unique hash
6. Fill in event details
7. Submit to review pool
8. System assigns 3 reviewers
9. Independent review:
   → All pass: Evidence stored on-chain → Distribute KOLE rewards
   → Any reject: Return with modification suggestions
10. Public exposure record
```

### 3. Token Distribution (TOKEN_ECONOMICS.md)
```
KOLE Token Distribution (1 Billion Total):
• Community Rewards: 40% (400M KOLE)
• Lucky Draw Pool: 40% (400M KOLE)
• Ecosystem Development: 10% (100M KOLE)
• Team & Advisors: 10% (100M KOLE)
```

### 4. Development Roadmap (ROADMAP.md)
```
2025-2026 Timeline:
Q1 2025: Foundation ✅
├── Whitepaper
├── Team Formation
├── Architecture Design
└── Smart Contracts

Q2 2025: Launch ✅
├── Mainnet Deployment
├── Beta Testing
├── Website Launch
└── Token Generation

Q3 2025: Expansion 🚀
├── DEX Listings
├── Community Growth
├── Mobile Apps
└── Partnerships

Q4 2025: Globalization 📅
├── Multi-language
├── Cross-chain Bridges
├── AI Review System
└── DAO Activation

2026: Future Vision 🔮
├── Industry Standards
├── Regulatory Framework
├── Web3 Identity
└── Metaverse Platform
```

### 5. Data Model ER Diagram (TECHNICAL_DOCS.md)
```
Database Structure:
USER
├── Creates → SUBMISSION
├── Performs → REVIEW
├── Receives → REWARD
└── Holds → STAKE

SUBMISSION
├── Contains → EVIDENCE
├── Undergoes → REVIEW
└── Generates → TRANSACTION

EVIDENCE
└── Stores → IPFS_FILE

KOL
├── Subject of → SUBMISSION
└── Has → MISCONDUCT

Key Relationships:
• Users submit evidence about KOLs
• Evidence stored on IPFS
• Reviews done by multiple reviewers
• Rewards distributed via blockchain
• Governance through DAO voting
```

## 🛠️ How to Generate Static Images

If you want to create static images from Mermaid diagrams:

### Option 1: Mermaid Live Editor
1. Visit [https://mermaid.live](https://mermaid.live)
2. Paste the Mermaid code
3. Click "Actions" → "Download PNG"

### Option 2: Command Line (for developers)
```bash
# Install mermaid-cli
npm install -g @mermaid-js/mermaid-cli

# Generate PNG from markdown
mmdc -i input.mmd -o output.png
```

### Option 3: VS Code Extension
1. Install "Mermaid Preview" extension
2. Right-click on diagram
3. Select "Export as PNG"

## 📲 Best Mobile Viewing Experience

### Recommended Settings:
1. **Browser**: Chrome or Safari
2. **Mode**: Desktop mode enabled
3. **Orientation**: Landscape for diagrams
4. **Zoom**: Pinch to zoom for details

### Alternative Viewers:
- **Obsidian** (Mobile app with Mermaid support)
- **Notion** (Import markdown with Mermaid)
- **HackMD** (Online markdown editor)

## 🔍 View Raw Mermaid Code

To see the raw Mermaid code on mobile:
1. Open the file (README.md, etc.)
2. Click "Raw" button
3. Search for ` ```mermaid`
4. Copy the code between ` ```mermaid` and ` ``` `

## 💡 Pro Tips

1. **Save for Offline**: Screenshot the diagrams when on desktop
2. **Share Links**: Send desktop viewers the direct GitHub links
3. **PDF Export**: Use browser print → Save as PDF (on desktop)
4. **Bookmark**: Save [Mermaid Live Editor](https://mermaid.live) for quick access

## 🆘 Still Having Issues?

Contact us:
- **Website**: [https://kolexposure.com](https://kolexposure.com)
- **Telegram**: [https://t.me/kolexposure](https://t.me/kolexposure)
- **Twitter/X**: [@kolexposure](https://x.com/kolexposure) | [@TODO_dream](https://x.com/TODO_dream)
- **Email**: support@kolexposure.com
- **Discord**: [Join our server](https://discord.com/invite/sZf44CseTf)

---

*Note: GitHub is working on improving mobile Mermaid support. This guide will be updated when mobile rendering is available.*