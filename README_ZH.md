# Gate for AI

🤖 **AI 原生加密基础设施**

Gate for AI 是一个 AI 原生加密基础设施，让 AI Agent 能够进行交易、分析行情、管理钱包和查询链上数据。通过 MCP（模型上下文协议） 和模块化 AI Skills，集成 ChatGPT, Claude, 和 OpenClaw ，获得 CEX + DEX全部能力。

**官方网站**: <a href="https://www.gate.com/zh/gate-for-ai" target="_blank">https://www.gate.com/zh/gate-for-ai</a>

🌐 **语言**: [English](README.md) | **简体中文**

---

## 概述

Gate for AI 赋予 Claude Code、OpenClaw、Codex、ChatGPT 和 Cursor 等 AI 智能体无缝访问 CEX（中心化交易所）和 DEX（去中心化交易所）的能力。通过模型上下文协议（MCP）和模块化 AI 技能，AI 智能体可以：

- 📈 **交易** - 在现货和期货市场执行交易
- 🔍 **分析** - 执行深度市场分析和筛选
- 💼 **管理** - 监控钱包和投资组合表现
- 📰 **监测** - 实时跟踪新闻和情绪
- 🔗 **查询** - 访问链上数据和分析

---

## 五大核心模块

Gate for AI 由覆盖整个加密生态系统的五大核心模块组成：

### Gate Exchange for AI
**CEX + TradFi，Agent 全能调用**
现货、合约、理财、Launchpad、资产管理等全线产品 — 均以结构化 API 暴露，Agent 可直接调用，无需爬取 UI，无需脆弱的变通方案。

### Gate DEX for AI
**Web3 链上交易引擎**
通过 MCP & Skills 提供 Web3 平台能力，包括行情数据、Swap、Perps 和 Meme 交易，让 Agent 直接操作链上 DEX。

### Gate Wallet for AI
**为 AI Agent 而生的 Web3 基础设施**
安全不妥协，交互不繁琐。原生 Wallet 专注极简高效，PluginWallet 打通全生态 DApp 连接，Keygenix 以企业级标准守护资产安全。TEE 物理隔离技术贯穿底层，智能调用与链上资产，始终坚不可摧。

### Gate News for AI
**实时加密资讯推送**
通过 MCP & Skills 提供加密资讯与动态能力，支持 Agent 订阅、搜索和分析最新市场信息。

### Gate Info for AI
**全面的链上数据查询**
加密信息查询能力，包括币种资料、项目信息、区块数据与地址信息，为 Agent 提供结构化信息与链上数据访问。

📖 **完整文档**: [English](README.md) | [中文](README_ZH.md)

---

## MCP 集成

MCP（模型上下文协议）让 AI 模型能够调用外部系统。在 Web3 中，MCP 使 Agent 能够通过稳定、结构化的端点访问交易所、钱包和链上服务。

### Gate MCP 服务器

📁 **仓库**: [gate/gate-mcp](https://github.com/gate/gate-mcp) · **端点**: `https://api.gatemcp.ai/mcp`

Gate MCP 服务器让 AI 智能体能够与 Gate 加密货币交易所交互，支持市场数据查询、交易执行和账户管理。

- 🔍 **现货 & 合约行情** — Ticker、深度、成交、K 线、资金费率、清算历史
- 💹 **交易** — 创建/取消/修改现货及合约订单
- 💼 **账户 & 钱包** — 余额、划转、充值、提现、子账户
- 🔐 **OAuth2** — 通过 Gate 账号安全授权（所有工具均需认证）

#### 可用工具

| 分类 | 工具 |
|------|------|
| **市场数据** (`market`) | list_currencies, get_currency, list_currency_pairs, get_currency_pair, get_spot_tickers, get_spot_order_book, get_spot_trades, get_spot_candlesticks, list_futures_contracts, get_futures_contract, get_futures_tickers, get_futures_order_book, get_futures_trades, get_futures_candlesticks, get_futures_funding_rate, get_futures_premium_index, list_futures_liq_orders |
| **现货交易** (`trade`) | create_spot_order, create_spot_batch_orders, cancel_spot_order, cancel_all_spot_orders, cancel_spot_batch_orders, amend_spot_order, amend_spot_batch_orders, get_spot_accounts, list_spot_orders, get_spot_order, list_spot_my_trades, get_spot_fee |
| **合约交易** (`trade`) | create_futures_order, create_futures_batch_orders, cancel_futures_order, cancel_all_futures_orders, amend_futures_order, get_futures_accounts, list_futures_positions, list_futures_orders, update_futures_position_leverage, update_futures_position_margin |
| **钱包 & 账户** (`wallet` / `account`) | get_total_balance, create_transfer, list_deposits, list_withdrawals, get_unified_accounts, list_sub_accounts, create_sub_account, list_sub_account_keys, create_sub_account_key |

📖 **完整 MCP 文档**: [Gate MCP 服务器](https://github.com/gate/gate-mcp)

---

## 技能生态系统

### 什么是技能？

**技能**是模块化工具（如获取价格、下单、签名交易、获取资讯）。Gate for AI 将技能打包在五大模块中，让 Agent 能够安全地组合工作流。

### Gate 技能市场

📁 **仓库**: [gate/gate-skills](https://github.com/gate/gate-skills)

目前可用的技能：

| 技能 | 描述 | 状态 |
|------|------|------|
| [gate-mcp-cursor-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-cursor-installer) | 一键安装 Gate MCP 和 Skills（适用于 Cursor） | ✅ 活跃 |
| [gate-mcp-openclaw-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-openclaw-installer) | Gate.com MCP 服务器完整安装器（适用于 OpenClaw） | ✅ 活跃 |
| [gate-mcp-claude-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-claude-installer) | 一键安装 Gate MCP 和 Skills（适用于 Claude Code / Claude CLI） | ✅ 活跃 |
| [gate-mcp-codex-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-codex-installer) | 一键安装 Gate MCP 和 Skills（适用于 Codex） | ✅ 活跃 |
| [gate-exchange-marketanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-marketanalysis) | 市场盘口分析：流动性、动量、清算、资金套利、基差、操纵风险、订单簿解释、滑点模拟、突破及周末与工作日对比 | ✅ 活跃 |
| [gate-exchange-futures](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-futures) | USDT 永续合约交易：开仓/平仓、取消/修改订单 | ✅ 活跃 |
| [gate-exchange-spot](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-spot) | Gate 现货交易：买入/卖出、订单管理、账户查询及资产兑换 | ✅ 活跃 |
| [gate-dex-market](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-market) | Gate DEX 市场数据（OpenAPI 模式）：代币信息、K 线、排名、安全审计 | ✅ 活跃 |
| [gate-dex-trade](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-trade) | Gate DEX 交易：MCP + OpenAPI 双模式，智能路由 Swap 执行 | ✅ 活跃 |
| [gate-dex-wallet](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-wallet) | Gate DEX 综合钱包：认证、资产查询、转账、DApp 交互 | ✅ 活跃 |

📖 **完整技能文档**: [Gate 技能](https://github.com/gate/gate-skills)

---

## 快速开始

### 先决条件

- Node.js & npm
- 支持 MCP 的 AI 智能体（Cursor、OpenClaw、Claude Code、Codex 等）

### 一键安装

通过安装器技能，几秒钟即可开始：

| 平台 | 安装器技能 | 命令 |
|------|-----------|------|
| **Cursor** | `gate-mcp-cursor-installer` | `bash skills/gate-mcp-cursor-installer/scripts/install.sh` |
| **OpenClaw** | `gate-mcp-openclaw-installer` | `./skills/gate-mcp-openclaw-installer/scripts/install.sh` |
| **Claude Code** | `gate-mcp-claude-installer` | `bash skills/gate-mcp-claude-installer/scripts/install.sh` |
| **Codex** | `gate-mcp-codex-installer` | `bash skills/gate-mcp-codex-installer/scripts/install.sh` |

或直接对 AI 助手说：

```
"帮我自动安装 Gate Skills 和 MCPs: https://github.com/gate/gate-skills"
```

### 开始使用

安装完成后，使用自然语言向 Agent 提问：

```
"分析比特币市场状况"
"检查 ETH 资金费率"
"找出交易量前 10 的币种"
```

---

## 文档

- 📖 [English](README.md)
- 📖 **简体中文**（当前页面）
- 🔧 [Gate MCP 服务器](https://github.com/gate/gate-mcp)
- 🛠️ [Gate 技能](https://github.com/gate/gate-skills)

---

## 资源

- **网站**: <a href="https://www.gate.com/zh/gate-for-ai" target="_blank">https://www.gate.com/zh/gate-for-ai</a>
- **Twitter**: [@gate_io](https://twitter.com/gate_io)
- **开发者支持**: `developer@gate.com`

---

## 许可证

本项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件。

---

<p align="center">
  <strong>由 Gate.com 构建。为加密社区服务。</strong>
</p>

<p align="center">
  <a href="https://www.gate.com/zh/gate-for-ai">网站</a> •
  <a href="https://github.com/gate/gate-mcp">MCP 服务器</a> •
  <a href="https://github.com/gate/gate-skills">技能</a>
</p>
