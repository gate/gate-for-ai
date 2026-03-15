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

📁 **Repository**: [gate/gate-mcp](https://github.com/gate/gate-mcp)

A Gate MCP server that enables AI agents to interact with the Gate cryptocurrency exchange for market data, trading, wallet, DEX, info, and news.

- 🔍 **Public Market Data** — Spot, futures, margin, options, delivery, earn, alpha tickers, order books, K-line, funding rate, liquidation history (**no auth required**)
- 💹 **Trading** — Create/cancel/amend spot, futures, options, delivery orders; price-triggered orders; trail orders
- 💼 **Account & Wallet** — Balances, transfers, deposits, withdrawals, sub-accounts, unified account
- 📊 **Margin & Earn** — Margin loans, earn products, flash swap
- 🌍 **TradFi, CrossEx, OTC, P2P** — Traditional finance, cross-exchange, OTC, P2P trading
- 🌐 **DEX** — On-chain wallet, swap (single-chain & cross-chain), token info, market data across 20+ chains
- 📰 **Info** — Coin info, market snapshots, technical analysis, on-chain data, compliance checks
- 📢 **News** — Real-time crypto news, exchange announcements, social sentiment
- 🔐 **OAuth2** — Secure authorization for trading and private tools

#### MCP Endpoints

| Endpoint | Auth | Tools |
|----------|------|-------|
| `https://api.gatemcp.ai/mcp` | None | Public market data (51 tools: spot, futures, margin, options, delivery, earn, alpha) |
| `https://api.gatemcp.ai/mcp/exchange` | OAuth2 | CEX trading & account (300+ tools: spot/futures/options/delivery/margin trading, wallet, unified account, sub-accounts, earn, flash swap, rebate, TradFi, CrossEx, OTC, P2P, Alpha) |
| `https://api.gatemcp.ai/mcp/dex` | Google OAuth | DEX wallet & swap (25 tools: on-chain wallet, swap, token info, market data across 20+ chains) |
| `https://api.gatemcp.ai/mcp/info` | None | Coin info & analysis (10 tools: market snapshots, technical analysis, on-chain data, compliance) |
| `https://api.gatemcp.ai/mcp/news` | None | News & sentiment (3 tools: news search, exchange announcements, social sentiment) |

#### Available Tools

**Public MCP** (`/mcp` — no auth, 51 tools)

| Business | Tools | Description |
|----------|-------|-------------|
| **Spot** | 9 | Currencies, trading pairs, tickers, order book, trades, candlesticks |
| **Futures** | 13 | Contracts, order book, trades, candlesticks, tickers, funding rate, premium index, liquidation |
| **Margin** | 3 | Currency pairs, margin tiers |
| **Options** | 12 | Underlyings, expirations, contracts, settlements, order book, tickers, candlesticks, trades |
| **Delivery** | 8 | Contracts, order book, trades, candlesticks, tickers, insurance, risk limit tiers |
| **Earn** | 3 | Dual investment plans, structured products, uni currencies |
| **Alpha** | 3 | Alpha currencies, tickers, tokens |

**Private MCP** (`/mcp/exchange` — OAuth2, 300+ tools)

| Business | Scope | Key Tools |
|----------|-------|-----------|
| **Spot** | profile / trade | Accounts, orders, trades, batch orders, price-triggered orders, countdown cancel, cross liquidate |
| **Futures** | profile / trade | Accounts, positions, orders, trades, dual positions, trail orders, price-triggered, BBO orders |
| **Margin** | profile / trade | Margin accounts, loans, auto-repay, uni loans |
| **Options** | profile / trade | Account, positions, orders, MMP settings |
| **Delivery** | profile / trade | Accounts, positions, orders, price-triggered orders |
| **Wallet** | wallet | Total balance, transfers, deposits, withdrawals, deposit address, SA balances, small balance convert |
| **Unified** | account | Unified accounts, mode, loans, risk units, borrowable, collateral, leverage config |
| **Sub-account** | account | Create/list/lock/unlock sub-accounts, API keys |
| **Account** | account | Account detail, main keys, rate limit, debit fee, STP groups |
| **Rebate** | profile | Agency/partner/broker commission history, user info |
| **Flash Swap** | profile / trade | Currency pairs, orders, create/preview |
| **Earn** | profile / trade | Dual/structured/uni products, orders, lend records |
| **Alpha** | profile / trade | Alpha accounts, orders, quote/place |
| **TradFi** | profile / trade | Categories, symbols, MT5 account, assets, orders, positions |
| **CrossEx** | profile / trade | Rule symbols, account, positions, orders, transfers, convert |
| **OTC** | profile / trade | Bank list, OTC orders, stable coin orders, quote/place/cancel |
| **P2P** | profile / trade | User info, ads, chats, transactions, confirm payment/receipt |

**DEX MCP** (`/mcp/dex` — Google OAuth, 25 tools)

| Category | Key Tools |
|----------|-----------|
| **Authentication** | Google OAuth login, session management |
| **Wallet** | Addresses, token balances, total assets, sign message/transaction |
| **Chain & Transactions** | Chain config, gas estimation, transfer preview, swap quote, one-shot swap, transaction history |
| **Market Data** | K-line, trading stats, liquidity, token info, token ranking, new token discovery, security audit |

**Info MCP** (`/mcp/info` — no auth, 10 tools)

| Category | Key Tools |
|----------|-----------|
| **Coin & Market** | Coin info, market snapshot (price, K-line summary, market cap, FDV, fear & greed) |
| **Trend & Technical** | K-line with indicators, historical indicator series (RSI, MACD, MA), multi-timeframe signals |
| **On-chain Data** | Address info & labels, address transactions, transaction details, token on-chain data (holders, smart money) |
| **Compliance** | Token security check (risk tier, taxes, open source, holders) |

**News MCP** (`/mcp/news` — no auth, 3 tools)

| Category | Key Tools |
|----------|-----------|
| **News & Sentiment** | News search by keyword/coin/time, exchange announcements (listings, delistings), social sentiment |

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
| [gate-mcp-openclaw-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-openclaw-installer) | Complete Gate MCP server installer for OpenClaw | ✅ Active |
| [gate-mcp-claude-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-claude-installer) | One-click installer for Gate MCP and Skills for Claude Code (Claude CLI) | ✅ Active |
| [gate-mcp-codex-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-codex-installer) | One-click installer for Gate MCP and Skills for Codex | ✅ Active |
| [gate-exchange-marketanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-marketanalysis) | Market tape analysis: liquidity, momentum, liquidation, funding arbitrage, basis, manipulation risk, order book explainer, slippage simulation, breakout, and weekend vs weekday | ✅ Active |
| [gate-exchange-futures](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-futures) | USDT perpetual futures trading: open/close position, cancel/amend order | ✅ Active |
| [gate-exchange-spot](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-spot) | Gate spot trading: buy/sell, order management, account queries, and asset swaps | ✅ Active |
| [gate-exchange-subaccount](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-subaccount) | Gate sub-account management: query status, list, create, lock/unlock (write ops need confirmation) | ✅ Active |
| [gate-exchange-assets](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-assets) | Gate Exchange asset queries: total balance, spot holdings, account valuation, account book (read-only) | ✅ Active |
| [gate-exchange-dual](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-dual) | Gate dual investment: product discovery, settlement simulation, position summary, balance (read-only) | ✅ Active |
| [gate-exchange-staking](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-staking) | Gate staking (earn): positions, rewards, products, order history (read-only) | ✅ Active |
| [gate-exchange-tradfi](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-tradfi) | Gate TradFi (traditional finance) read-only queries: orders, positions, market data, assets and MT5 account info | ✅ Active |
| [gate-exchange-simpleearn](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-simpleearn) | Gate Simple Earn (Uni) flexible earn queries: positions, interest, top APY rate lookup (subscribe/redeem not supported) | ✅ Active |
| [gate-exchange-affiliate](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-affiliate) | Gate Exchange affiliate/partner program: commission, volume, net fees, customer count, trading users query and application guidance | ✅ Active |
| [gate-exchange-unified](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-unified) | Gate unified account: equity, borrow/repay, loan & interest, mode switch, leverage & collateral | ✅ Active |
| [gate-dex-market](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-market) | Gate DEX market data via OpenAPI: token info, K-line, rankings, security audit | ✅ Active |
| [gate-dex-trade](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-trade) | Gate DEX trading: MCP + OpenAPI dual mode, smart routing for Swap execution | ✅ Active |
| [gate-dex-wallet](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-wallet) | Gate DEX comprehensive wallet: authentication, assets, transfers, DApp interactions | ✅ Active |
| [gate-info-coinanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-info-coinanalysis) | Single-coin comprehensive analysis: fundamentals, technicals, news, sentiment | ✅ Active |
| [gate-info-addresstracker](https://github.com/gate/gate-skills/tree/master/skills/gate-info-addresstracker) | On-chain address tracking: profile, transaction history, fund flow analysis | ✅ Active |
| [gate-info-coincompare](https://github.com/gate/gate-skills/tree/master/skills/gate-info-coincompare) | Multi-coin comparison with multi-dimensional analysis table | ✅ Active |
| [gate-info-marketoverview](https://github.com/gate/gate-skills/tree/master/skills/gate-info-marketoverview) | Crypto market overview: sector rankings, DeFi, events, macro summary | ✅ Active |
| [gate-info-riskcheck](https://github.com/gate/gate-skills/tree/master/skills/gate-info-riskcheck) | Token & contract risk assessment: honeypot, rug pull, tax, holder concentration | ✅ Active |
| [gate-info-trendanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-info-trendanalysis) | Trend & technical analysis: K-line, RSI, MACD, multi-timeframe signals | ✅ Active |
| [gate-news-briefing](https://github.com/gate/gate-skills/tree/master/skills/gate-news-briefing) | Crypto news briefing: major events, trending news, social sentiment | ✅ Active |
| [gate-news-eventexplain](https://github.com/gate/gate-skills/tree/master/skills/gate-news-eventexplain) | Event attribution & explanation: why did X crash/pump, impact chain analysis | ✅ Active |
| [gate-news-listing](https://github.com/gate/gate-skills/tree/master/skills/gate-news-listing) | Exchange listing/delisting tracker with fundamental supplements | ✅ Active |

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
  <strong>Built by Gate. Built for the crypto community.</strong>
</p>

<p align="center">
  <a href="https://www.gate.com/gate-for-ai">Website</a> •
  <a href="https://github.com/gate/gate-mcp">MCP Server</a> •
  <a href="https://github.com/gate/gate-skills">Skills</a>
</p>
