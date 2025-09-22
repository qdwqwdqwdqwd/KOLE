# KOLE - KOL劣迹曝光平台

KOLE 仓库维护一个去中心化平台的文档与数据，用于记录并曝光 Key Opinion Leader (KOL) 的不当行为。项目核心是可验证证据、透明治理以及中英双语沟通。

## 项目概览
KOLE 通过 Solana 智能合约与 IPFS 存储实现防篡改的劣迹档案。本仓库收录了平台白皮书、社区操作指南以及结构化元数据，定义生态运行方式。

## 目录结构
- `docs/`：白皮书（中英文）与社区机制说明的权威来源。
- `data/`：包含版本信息、治理参数与历史记录的知识库文件 `知识库.json`。
- `AGENTS.md` / `CLAUDE.md`：面向不同智能体的贡献指南。
- `.env`：本地调试环境变量；提交前请替换或移除真实凭据。

## 关键文档
| 文件 | 说明 |
| --- | --- |
| `docs/KOL Misconduct Exposure Platform Whitepaper.md` | 英文版白皮书，介绍平台目标、架构与路线图。 |
| `docs/KOL劣迹曝光平台白皮书.md` | 中文版白皮书，便于本地社区理解与传播。 |
| `docs/社区资料.md` | 社区治理流程、证据提交流程与激励规则。 |
| `data/知识库.json` | 平台的结构化元数据，用于同步版本与发布信息。 |

## 快速上手
1. 克隆仓库并进入项目目录。
2. 安装 Markdown 检查工具（`npm install -g markdownlint-cli`）并确认系统已安装 `jq`。
3. 执行 `npx markdownlint-cli README*.md docs/**/*.md` 检查 Markdown 风格。
4. 在提交前运行 `jq '.' data/知识库.json` 校验 JSON 语法。
5. 通过 `python3 -m http.server 8000` 预览文档，浏览器访问 `http://localhost:8000`。

## 数据与版本管理
- 发布新版本时同步更新 `data/知识库.json` 中的 `metadata_version` 与 `last_updated`。
- 确保白皮书封面上的版本号与知识库记录一致。
- 重大路线调整需同时修改白皮书与知识库条目以保持一致性。

## 贡献指南
- 阅读 `AGENTS.md` 了解仓库工作流程与校验步骤。
- 中英文文档需同步更新，避免内容漂移。
- 使用简洁的祈使句提交信息，如 `Adjust reward distribution table`。
- 提交 Pull Request 时说明影响范围、已执行的校验命令及是否需要后续本地化审查。

## 状态与路线图
当前白皮书版本为 1.2（2025 年 9 月），涵盖从证据提交基础设施到 DAO 治理与跨链扩展的阶段性规划。详情请参阅白皮书中的路线图章节。

## 免责声明
KOLE 仍在积极开发中。仓库中的文档仅供参考，随着智能合约、激励模型与治理流程的迭代，内容可能发生调整。
