# Gate for AI

🤖 **AI-Native Crypto Infrastructure**

Gate for AI is an AI-native crypto infrastructure that enables AI agents to trade, analyze markets, manage wallets, and query on-chain data through MCP (Model Context Protocol) and modular AI Skills. Integrate ChatGPT, Claude, and OpenClaw with CEX + DEX capabilities.

**Website**: <a href="https://www.gate.com/gate-for-ai" target="_blank">https://www.gate.com/gate-for-ai</a>

🌐 **Languages**: [English](README.md) | [简体中文](README_ZH.md)

---

## Overview

Gate for AI empowers AI agents like Claude Code, OpenClaw, Codex, ChatGPT, and Cursor with seamless access to both CEX (Centralized Exchange) and DEX (Decentralized Exchange) capabilities. Through the Model Context Protocol (MCP) and modular AI Skills, AI agents can:

- 📈 **Trade** - Execute trades on spot and futures markets
- 🔍 **Analyze** - Perform deep market analysis and screening
- 💼 **Manage** - Monitor wallets and portfolio performance
- 📰 **Monitor** - Track news and sentiment in real-time
- 🔗 **Query** - Access on-chain data and analytics

---

## Five Core Modules

Gate for AI consists of five core modules that cover the entire crypto ecosystem:

### Gate Exchange for AI
**CEX + TradFi, fully accessible to agents**
Spot, futures, wealth management, Launchpad, asset management and more — all exposed as structured APIs your agent can call directly. No UI scraping, no fragile workarounds.

### Gate DEX for AI
**Web3 On-chain Trading Power**
Provides Web3 platform capabilities including market data, Swap, Perps, and Meme trading through MCP & Skills, enabling Agents to directly operate on-chain DEX.

### Gate Wallet for AI
**Web3 Infrastructure Built for AI Agents**
Uncompromised security, frictionless interaction. Native Wallet focuses on minimalist efficiency, PluginWallet connects the entire DApp ecosystem, and Keygenix safeguards assets with enterprise-grade standards. TEE hardware isolation runs through the foundation — smart invocation and on-chain assets remain impenetrable.

### Gate News for AI
**Real-time Crypto News Feed**
Crypto news and updates capabilities provided through MCP & Skills, supporting Agents to subscribe, search, and analyze the latest market information.

### Gate Info for AI
**Comprehensive On-chain Data Query**
Crypto information query capabilities including coin profiles, project information, block data, and address information, providing Agents with structured information and on-chain data access.

📖 **Full Documentation**: [English](README.md) | [中文](README_ZH.md)

---

## MCP Integration

MCP (Model Context Protocol) lets AI models call external systems. In Web3, MCP enables agents to access exchange, wallet, and on-chain services via stable, structured endpoints.

### Gate MCP Server

📁 **Repository**: [gate/gate-mcp](https://github.com/gate/gate-mcp) · **Endpoint**: `https://api.gatemcp.ai/mcp`

A Gate MCP server that enables AI agents to interact with the Gate cryptocurrency exchange for market data, trading, and account management.

- 🔍 **Spot & Futures Market** — Tickers, order books, trades, K-line, funding rate, liquidation history
- 💹 **Trading** — Create/cancel/amend spot and futures orders
- 💼 **Account & Wallet** — Balances, transfers, deposits, withdrawals, sub-accounts
- 🔐 **OAuth2** — Secure authorization via Gate account login (all tools require auth)

#### Available Tools

| Category | Tools |
|----------|-------|
| **Market Data** (`market`) | list_currencies, get_currency, list_currency_pairs, get_currency_pair, get_spot_tickers, get_spot_order_book, get_spot_trades, get_spot_candlesticks, list_futures_contracts, get_futures_contract, get_futures_tickers, get_futures_order_book, get_futures_trades, get_futures_candlesticks, get_futures_funding_rate, get_futures_premium_index, list_futures_liq_orders |
| **Spot Trading** (`trade`) | create_spot_order, create_spot_batch_orders, cancel_spot_order, cancel_all_spot_orders, cancel_spot_batch_orders, amend_spot_order, amend_spot_batch_orders, get_spot_accounts, list_spot_orders, get_spot_order, list_spot_my_trades, get_spot_fee |
| **Futures Trading** (`trade`) | create_futures_order, create_futures_batch_orders, cancel_futures_order, cancel_all_futures_orders, amend_futures_order, get_futures_accounts, list_futures_positions, list_futures_orders, update_futures_position_leverage, update_futures_position_margin |
| **Wallet & Account** (`wallet` / `account`) | get_total_balance, create_transfer, list_deposits, list_withdrawals, get_unified_accounts, list_sub_accounts, create_sub_account, list_sub_account_keys, create_sub_account_key |

📖 **Full MCP Documentation**: [Gate MCP Server](https://github.com/gate/gate-mcp)

---

## Skills Ecosystem

### What are Skills?

**Skills** are modular tools (e.g., get price, place order, sign tx, fetch news). Gate for AI packages Skills across five modules so agents can compose workflows safely.

### Gate Skills Marketplace

📁 **Repository**: [gate/gate-skills](https://github.com/gate/gate-skills)

Available skills for crypto trading and market analysis:

| Skill | Description | Status |
|-------|-------------|--------|
| [gate-mcp-cursor-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-cursor-installer) | One-click installer for Gate MCP and Skills for Cursor | ✅ Active |
| [gate-mcp-openclaw-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-openclaw-installer) | Complete Gate.com MCP server installer for OpenClaw | ✅ Active |
| [gate-mcp-claude-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-claude-installer) | One-click installer for Gate MCP and Skills for Claude Code (Claude CLI) | ✅ Active |
| [gate-mcp-codex-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-codex-installer) | One-click installer for Gate MCP and Skills for Codex | ✅ Active |
| [gate-exchange-marketanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-marketanalysis) | Market tape analysis: liquidity, momentum, liquidation, funding arbitrage, basis, manipulation risk, order book explainer, slippage simulation, breakout, and weekend vs weekday | ✅ Active |
| [gate-exchange-futures](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-futures) | USDT perpetual futures trading: open/close position, cancel/amend order | ✅ Active |
| [gate-exchange-spot](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-spot) | Gate spot trading: buy/sell, order management, account queries, and asset swaps | ✅ Active |
| [gate-dex-market](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-market) | Gate DEX market data via OpenAPI: token info, K-line, rankings, security audit | ✅ Active |
| [gate-dex-trade](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-trade) | Gate DEX trading: MCP + OpenAPI dual mode, smart routing for Swap execution | ✅ Active |
| [gate-dex-wallet](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-wallet) | Gate DEX comprehensive wallet: authentication, assets, transfers, DApp interactions | ✅ Active |

### How Skills Work

1. **User Request** — Natural language query
2. **Skill Triggered** — Based on keywords/patterns
3. **Instructions Loaded** — SKILL.md content loaded into context
4. **AI Action** — AI executes using MCP tools

📖 **Full Skills Documentation**: [Gate Skills](https://github.com/gate/gate-skills)

---

## Getting Started

### Prerequisites

- Node.js & npm
- An MCP-compatible AI agent (Cursor, OpenClaw, Claude Code, Codex, etc.)

### One-Click Installation

Get started in seconds with our installer skills:

| Platform | Installer Skill | Command |
|----------|----------------|---------|
| **Cursor** | `gate-mcp-cursor-installer` | `bash skills/gate-mcp-cursor-installer/scripts/install.sh` |
| **OpenClaw** | `gate-mcp-openclaw-installer` | `./skills/gate-mcp-openclaw-installer/scripts/install.sh` |
| **Claude Code** | `gate-mcp-claude-installer` | `bash skills/gate-mcp-claude-installer/scripts/install.sh` |
| **Codex** | `gate-mcp-codex-installer` | `bash skills/gate-mcp-codex-installer/scripts/install.sh` |

Or simply ask your AI assistant:

```
"Help me auto install Gate Skills and MCPs: https://github.com/gate/gate-skills"
```

### Start Using

Once installed, ask your agent in natural language:

```
"Analyze Bitcoin market conditions"
"Check ETH funding rates"
"Find top 10 coins by volume"
```

---

## Documentation

- 📖 [Full Documentation (English)](README.md)
- 📖 [完整文档 (中文)](README_ZH.md)
- 🔧 [Gate MCP Server](https://github.com/gate/gate-mcp)
- 🛠️ [Gate Skills](https://github.com/gate/gate-skills)

---

## Resources

- **Website**: <a href="https://www.gate.com/gate-for-ai" target="_blank">https://www.gate.com/gate-for-ai</a>
- **Twitter**: [@gate_io](https://twitter.com/gate_io)
- **Developer Support**: `developer@gate.com`

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <strong>Built by Gate.com. Built for the crypto community.</strong>
</p>

<p align="center">
  <a href="https://www.gate.com/gate-for-ai">Website</a> •
  <a href="https://github.com/gate/gate-mcp">MCP Server</a> •
  <a href="https://github.com/gate/gate-skills">Skills</a>
</p>
