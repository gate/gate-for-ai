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

📁 **Repository**: `https://github.com/gate/gate-mcp`

The Gate MCP Server exposes 20+ trading and market data tools for AI agents:

- **Spot Market Tools** - list_currencies, get_currency, list_currency_pairs, get_currency_pair, get_spot_tickers, get_spot_order_book, get_spot_candlesticks, get_spot_trades
- **Futures Market Tools** - list_futures_contracts, get_futures_contract, get_futures_tickers, get_futures_order_book, get_futures_candlesticks, get_futures_trades, get_futures_funding_rate, get_futures_premium_index, list_futures_liq_orders

### Quick Start with MCP

```bash
# Install Claude CLI
brew install claude-code

# Add Gate MCP
claude mcp add --transport http Gate https://api.gatemcp.ai/mcp

# Start using
claude mcp list
```

📖 **Full MCP Documentation**: [Gate MCP Server](https://github.com/gate/gate-mcp)

---

## Skills Ecosystem

### What are Skills?

**Skills** are modular tools (e.g., get price, place order, sign tx, fetch news). Gate for AI packages Skills across five modules so agents can compose workflows safely.

### Gate Skills Marketplace

📁 **Repository**: `https://github.com/gate/gate-skills`

Available skills for crypto trading and market analysis:

| Skill | Description | Status |
|-------|-------------|--------|
| [gate-exchange-market](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-market) | Single-coin deep analysis & multi-coin screening | ✅ Active |
| [gate-mcp-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-installer) | One-click Gate MCP setup & configuration | ✅ Active |

### How Skills Work

1. **User Request** — Natural language query
2. **Skill Triggered** — Based on keywords/patterns
3. **Instructions Loaded** — SKILL.md content loaded into context
4. **AI Action** — AI executes using MCP tools

📖 **Full Skills Documentation**: [Gate Skills](https://github.com/gate/gate-skills)

---

## Getting Started

### Prerequisites

- Node.js >= 18 (for MCP clients)
- An MCP-compatible AI agent (Claude, Cursor, etc.)

### Installation

1. **Install Claude CLI**:
   ```bash
   brew install claude-code
   ```

2. **Add Gate MCP**:
   ```bash
   claude mcp add --transport http Gate https://api.gatemcp.ai/mcp
   ```

3. **Verify**:
   ```bash
   claude mcp list
   ```

4. **Start Using**:
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
