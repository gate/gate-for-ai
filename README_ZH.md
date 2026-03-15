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

📁 **仓库**: [gate/gate-mcp](https://github.com/gate/gate-mcp)

Gate MCP 服务器让 AI 智能体能够与 Gate 加密货币交易所交互，支持行情数据、交易、钱包、DEX、资讯和新闻。

- 🔍 **公开行情数据** — 现货、合约、杠杆、期权、交割、理财、Alpha 的 Ticker、深度、K 线、资金费率、清算历史（**无需认证**）
- 💹 **交易** — 创建/取消/修改现货、合约、期权、交割订单；条件委托；追踪委托
- 💼 **账户 & 钱包** — 余额、划转、充值、提现、子账户、统一账户
- 📊 **杠杆 & 理财** — 杠杆借贷、理财产品、闪兑
- 🌍 **TradFi、CrossEx、OTC、P2P** — 传统金融、跨所交易、场外交易、P2P 交易
- 🌐 **DEX** — 链上钱包、Swap（单链 & 跨链）、代币信息、20+ 链市场数据
- 📰 **Info** — 币种信息、市场快照、技术分析、链上数据、合规检查
- 📢 **News** — 实时加密新闻、交易所公告、社交情绪
- 🔐 **OAuth2** — 交易和私有工具的安全授权

#### MCP 端点

| 端点 | 认证 | 工具 |
|------|------|------|
| `https://api.gatemcp.ai/mcp` | 无 | 公开行情数据（51 个工具：现货、合约、杠杆、期权、交割、理财、Alpha） |
| `https://api.gatemcp.ai/mcp/exchange` | OAuth2 | CEX 交易 & 账户（300+ 工具：现货/合约/期权/交割/杠杆交易、钱包、统一账户、子账户、理财、闪兑、返佣、TradFi、CrossEx、OTC、P2P、Alpha） |
| `https://api.gatemcp.ai/mcp/dex` | Google OAuth | DEX 钱包 & Swap（25 个工具：链上钱包、Swap、代币信息、20+ 链市场数据） |
| `https://api.gatemcp.ai/mcp/info` | 无 | 币种信息 & 分析（10 个工具：市场快照、技术分析、链上数据、合规检查） |
| `https://api.gatemcp.ai/mcp/news` | 无 | 新闻 & 情绪（3 个工具：新闻搜索、交易所公告、社交情绪） |

#### 可用工具

**公开 MCP**（`/mcp` — 无需认证，51 个工具）

| 业务 | 工具数 | 说明 |
|------|--------|------|
| **现货** | 9 | 币种、交易对、Ticker、深度、成交、K 线 |
| **合约** | 13 | 合约信息、深度、成交、K 线、Ticker、资金费率、溢价指数、清算 |
| **杠杆** | 3 | 交易对、保证金等级 |
| **期权** | 12 | 标的、到期日、合约、结算、深度、Ticker、K 线、成交 |
| **交割** | 8 | 合约、深度、成交、K 线、Ticker、保险基金、风险限额 |
| **理财** | 3 | 双币投资计划、结构化产品、Uni 币种 |
| **Alpha** | 3 | Alpha 币种、Ticker、代币 |

**私有 MCP**（`/mcp/exchange` — OAuth2，300+ 工具）

| 业务 | 权限 | 主要功能 |
|------|------|----------|
| **现货** | profile / trade | 账户、订单、成交、批量下单、条件委托、倒计时撤单、跨仓清算 |
| **合约** | profile / trade | 账户、持仓、订单、成交、双向持仓、追踪委托、条件委托、BBO 委托 |
| **杠杆** | profile / trade | 杠杆账户、借贷、自动还款、Uni 借贷 |
| **期权** | profile / trade | 账户、持仓、订单、MMP 设置 |
| **交割** | profile / trade | 账户、持仓、订单、条件委托 |
| **钱包** | wallet | 总余额、划转、充值、提现、充值地址、子账户余额、小额资产兑换 |
| **统一账户** | account | 统一账户、模式、借贷、风险单元、可借额度、抵押品、杠杆配置 |
| **子账户** | account | 创建/列表/锁定/解锁子账户、API Key |
| **账户** | account | 账户详情、主密钥、频率限制、扣费设置、STP 组 |
| **返佣** | profile | 代理/合伙人/经纪人佣金历史、用户信息 |
| **闪兑** | profile / trade | 交易对、订单、创建/预览 |
| **理财** | profile / trade | 双币/结构化/Uni 产品、订单、借出记录 |
| **Alpha** | profile / trade | Alpha 账户、订单、报价/下单 |
| **TradFi** | profile / trade | 分类、标的、MT5 账户、资产、订单、持仓 |
| **CrossEx** | profile / trade | 规则标的、账户、持仓、订单、划转、兑换 |
| **OTC** | profile / trade | 银行列表、OTC 订单、稳定币订单、报价/下单/取消 |
| **P2P** | profile / trade | 用户信息、广告、聊天、交易、确认付款/收款 |

**DEX MCP**（`/mcp/dex` — Google OAuth，25 个工具）

| 分类 | 主要功能 |
|------|----------|
| **认证** | Google OAuth 登录、会话管理 |
| **钱包** | 地址查询、代币余额、总资产、签名消息/交易 |
| **链 & 交易** | 链配置、Gas 估算、转账预览、Swap 报价、一键 Swap、交易历史 |
| **市场数据** | K 线、交易统计、流动性、代币信息、代币排名、新代币发现、安全审计 |

**Info MCP**（`/mcp/info` — 无需认证，10 个工具）

| 分类 | 主要功能 |
|------|----------|
| **币种 & 市场** | 币种信息、市场快照（价格、K 线摘要、市值、FDV、恐惧贪婪指数） |
| **趋势 & 技术** | 带指标的 K 线、历史指标序列（RSI、MACD、MA）、多周期信号 |
| **链上数据** | 地址信息与标签、地址交易、交易详情、代币链上数据（持有者、聪明钱） |
| **合规** | 代币安全检查（风险等级、税费、开源、持有者） |

**News MCP**（`/mcp/news` — 无需认证，3 个工具）

| 分类 | 主要功能 |
|------|----------|
| **新闻 & 情绪** | 按关键词/币种/时间搜索新闻、交易所公告（上架/下架）、社交情绪 |

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
| [gate-mcp-cursor-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-cursor-installer) | 为 Cursor 提供的一键安装 Gate MCP 与 Skills 脚本 | ✅ 活跃 |
| [gate-mcp-openclaw-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-openclaw-in staller) | 为 OpenClaw 提供的 Gate MCP 完整安装器 | ✅ 活跃 |
| [gate-mcp-claude-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-claude-installer) | 为 Claude Code (Claude CLI) 提供的一键安装 Gate MCP 与 Skills | ✅ 活跃 |
| [gate-mcp-codex-installer](https://github.com/gate/gate-skills/tree/master/skills/gate-mcp-codex-installer) | 为 Codex 提供的一键安装 Gate MCP 与 Skills | ✅ 活跃 |
| [gate-exchange-marketanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-marketanalysis) | 市场盘口分析：流动性、动量、爆仓、资金费套利、基差、操纵风险、订单簿解读、滑点模拟、K线突破、周末与工作日对比 | ✅ 活跃 |
| [gate-exchange-futures](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-futures) | Gate 合约交易：开仓、平仓、撤单、改单 | ✅ 活跃 |
| [gate-exchange-spot](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-spot) | Gate 现货交易：买卖下单、订单管理、账户查询、资产兑换 | ✅ 活跃 |
| [gate-exchange-subaccount](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-subaccount) | Gate 子账户管理：查询状态、列表、创建、锁定/解锁（写操作需确认） | ✅ 活跃 |
| [gate-exchange-assets](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-assets) | Gate 交易所资产查询：总资产、现货持仓、账户估值、账户流水（只读） | ✅ 活跃 |
| [gate-exchange-dual](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-dual) | Gate 双币理财：产品发现、结算模拟、持仓与余额查询（只读） | ✅ 活跃 |
| [gate-exchange-staking](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-staking) | Gate 理财/质押：持仓、收益、产品发现、订单历史（只读） | ✅ 活跃 |
| [gate-exchange-tradfi](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-tradfi) | Gate TradFi（传统金融）只读查询：订单、持仓、行情、资产与 MT5 账户信息 | ✅ 活跃 |
| [gate-exchange-simpleearn](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-simpleearn) | Gate Simple Earn（活期理财）：持仓、利息、Top APY 利率查询（不支持申购/赎回） | ✅ 活跃 |
| [gate-exchange-affiliate](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-affiliate) | Gate 交易所联盟/合伙人计划：佣金、交易量、净手续费、客户数、交易用户数查询与申请指引 | ✅ 活跃 |
| [gate-exchange-unified](https://github.com/gate/gate-skills/tree/master/skills/gate-exchange-unified) | Gate 统一账户：权益、借还、借贷与利息、模式切换、杠杆与抵押币 | ✅ 活跃 |
| [gate-dex-market](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-market) | Gate DEX 行情数据（OpenAPI 模式）：代币信息、K线、排行、安全审计 | ✅ 活跃 |
| [gate-dex-trade](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-trade) | Gate DEX 交易：MCP + OpenAPI 双模式，智能路由执行 Swap | ✅ 活跃 |
| [gate-dex-wallet](https://github.com/gate/gate-skills/tree/master/skills/gate-dex-wallet) | Gate DEX 综合钱包：身份认证、资产查询、转账执行、DApp 交互 | ✅ 活跃 |
| [gate-info-coinanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-info-coinanalysis) | 单币种综合分析：基本面、技术面、新闻、社交情绪 | ✅ 活跃 |
| [gate-info-addresstracker](https://github.com/gate/gate-skills/tree/master/skills/gate-info-addresstracker) | 链上地址追踪：地址画像、交易历史、资金流向分析 | ✅ 活跃 |
| [gate-info-coincompare](https://github.com/gate/gate-skills/tree/master/skills/gate-info-coincompare) | 多币种对比：多维度对比表与总结 | ✅ 活跃 |
| [gate-info-marketoverview](https://github.com/gate/gate-skills/tree/master/skills/gate-info-marketoverview) | 加密市场总览：板块排行、DeFi、事件、宏观摘要 | ✅ 活跃 |
| [gate-info-riskcheck](https://github.com/gate/gate-skills/tree/master/skills/gate-info-riskcheck) | 代币与合约风险评估：蜜罐检测、Rug Pull、税费、持币集中度 | ✅ 活跃 |
| [gate-info-trendanalysis](https://github.com/gate/gate-skills/tree/master/skills/gate-info-trendanalysis) | 趋势与技术分析：K线、RSI、MACD、多周期信号 | ✅ 活跃 |
| [gate-news-briefing](https://github.com/gate/gate-skills/tree/master/skills/gate-news-briefing) | 加密新闻简报：重大事件、热门新闻、社交情绪 | ✅ 活跃 |
| [gate-news-eventexplain](https://github.com/gate/gate-skills/tree/master/skills/gate-news-eventexplain) | 事件归因与解释：价格异动原因追溯与影响链分析 | ✅ 活跃 |
| [gate-news-listing](https://github.com/gate/gate-skills/tree/master/skills/gate-news-listing) | 交易所上架/下架追踪：公告监控与新币基本面补充 | ✅ 活跃 |

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
  <strong>由 Gate 构建。为加密社区服务。</strong>
</p>

<p align="center">
  <a href="https://www.gate.com/zh/gate-for-ai">网站</a> •
  <a href="https://github.com/gate/gate-mcp">MCP 服务器</a> •
  <a href="https://github.com/gate/gate-skills">技能</a>
</p>
