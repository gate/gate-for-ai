# Gate for AI

🤖 **AI 原生加密基础设施**

Gate for AI 是一个 AI 原生加密基础设施，通过 MCP（模型上下文协议）和模块化 AI 技能，使 AI 智能体能够进行交易、分析市场、管理钱包和查询链上数据。

🌐 **语言**: [English](README.md) | **简体中文**

---

## 概述

Gate for AI 赋予 ChatGPT、Claude 和 OpenClaw 等 AI 智能体无缝访问 CEX（中心化交易所）和 DEX（去中心化交易所）的能力。通过模型上下文协议（MCP）和模块化 AI 技能，AI 智能体可以：

- 📈 **交易** - 在现货和期货市场执行交易
- 🔍 **分析** - 执行深度市场分析和筛选
- 💼 **管理** - 监控钱包和投资组合表现
- 📰 **监测** - 实时跟踪新闻和情绪
- 🔗 **查询** - 访问链上数据和分析

---

## 五大核心模块

Gate for AI 由覆盖整个加密生态系统的五大核心模块组成：

| 模块 | 描述 | 主要特性 |
|------|------|----------|
| **Gate Exchange for AI** | CEX 交易智能 | 现货和合约市场、资金费率、强平数据 |
| **Gate DEX for AI** | DEX 聚合（即将推出） | 多 DEX 路由、流动性池、收益耕作 |
| **Gate Wallet for AI** | 钱包管理（即将推出） | 多链跟踪、安全分析、盈亏统计 |
| **Gate News for AI** | 新闻与情绪（即将推出） | 新闻聚合、AI 情绪、市场影响 |
| **Gate Info for AI** | 市场分析（即将推出） | 链上数据、项目研究、风险评级 |

📖 **完整文档**: [English](README.md) | [中文](README_ZH.md)

---

## MCP 集成

Gate for AI 基于**模型上下文协议（MCP）**构建，这是 AI 工具通信的开放标准。

### Gate MCP 服务器

📁 **仓库**: `https://github.com/gate/gate-mcp`

Gate MCP 服务器为 AI 智能体提供 20 多个交易和市场数据工具：

**现货市场工具**：
- `list_currencies` / `get_currency` - 币种信息
- `list_currency_pairs` / `get_currency_pair` - 交易对信息
- `get_spot_tickers` - 市场行情
- `get_spot_order_book` - 订单簿深度
- `get_spot_candlesticks` - K 线/历史数据
- `get_spot_trades` - 成交记录

**合约市场工具**：
- `list_futures_contracts` / `get_futures_contract` - 合约规格
- `get_futures_tickers` - 合约行情
- `get_futures_order_book` - 合约订单簿
- `get_futures_candlesticks` - 合约 K 线
- `get_futures_funding_rate` - 资金费率历史
- `list_futures_liq_orders` - 强平记录

📖 **完整 MCP 文档**: [Gate MCP 服务器](https://github.com/gate/gate-mcp)

---

## 技能生态系统

### 什么是技能？

**技能**是扩展 AI 智能体能力的模块化包，为特定领域提供专业知识、工作流程和工具。

### Gate 技能市场

📁 **仓库**: `https://github.com/gate/gate-skills`

目前可用的技能：

| 技能 | 描述 | 状态 |
|------|------|------|
| [gate-exchange-market](https://github.com/gate/gate-skills/tree/main/skills/gate-exchange-market) | 单币种深度分析和多币种筛选 | ✅ 活跃 |
| [gate-mcp-installer](https://github.com/gate/gate-skills/tree/main/skills/gate-mcp-installer) | 一键 Gate MCP 设置和配置 | ✅ 活跃 |

📖 **完整技能文档**: [Gate 技能](https://github.com/gate/gate-skills)

---

## 快速开始

### 先决条件

- Node.js >= 18（用于 MCP 客户端）
- 支持 MCP 的 AI 智能体（Claude、Cursor 等）

### 安装

1. **安装 Claude CLI**：
   ```bash
   brew install claude-code
   ```

2. **添加 Gate MCP**：
   ```bash
   claude mcp add --transport http Gate https://api.gatemcp.ai/mcp
   ```

3. **验证**：
   ```bash
   claude mcp list
   ```

4. **开始使用**：
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

- **网站**: [https://www.gate.com/gate-for-ai](https://www.gate.com/gate-for-ai)
- **Discord**: [加入 Gate 开发者社区](https://discord.gg/gateio)
- **Twitter**: [@gate_io](https://twitter.com/gate_io)
- **开发者支持**: `developer@gate.com`

---

## 贡献

欢迎贡献！详情请参阅我们的[贡献指南](CONTRIBUTING.md)。

---

## 许可证

本项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件。

---

<p align="center">
  <strong>由 Gate.io 构建。为加密社区服务。</strong>
</p>

<p align="center">
  <a href="https://www.gate.com/gate-for-ai">网站</a> •
  <a href="https://github.com/gate/gate-mcp">MCP 服务器</a> •
  <a href="https://github.com/gate/gate-skills">技能</a> •
  <a href="https://discord.gg/gateio">Discord</a>
</p>
