# IROS Terminal - Product Specification

**Institutional-Grade AI Trading Intelligence System**

Version 2.0 | January 2026

---

## Executive Summary

**IROS Terminal** is an institutional-grade AI-powered trading intelligence platform that combines proprietary quantitative models (MCF Engine) with a fine-tuned large language model to deliver real-time market analysis, risk assessment, and trading recommendations.

Unlike generic AI assistants, IROS Terminal integrates live market data, multi-timeframe regime detection, topological analysis, and quantitative risk models to provide actionable trading intelligence comparable to Bloomberg Terminal's analytical capabilities.

---

## Product Overview

### What is IROS Terminal?

IROS (Intelligent Real-time Operations System) Terminal is a conversational AI interface that:

- **Analyzes** live cryptocurrency markets using institutional-grade quantitative models
- **Detects** market regimes and volatility states across multiple timeframes
- **Calculates** optimal position sizing using Kelly Criterion and risk-parity methods
- **Monitors** market microstructure, liquidity flows, and smart money indicators
- **Generates** actionable trading recommendations with precise entry/exit levels
- **Visualizes** complex market dynamics through interactive 3D analytics

### Core Value Proposition

**Problem:** Traders lack access to institutional-grade quantitative analysis tools. Bloomberg Terminal costs $24,000/year. Generic AI chatbots lack market context and real-time data.

**Solution:** IROS Terminal delivers institutional-quality analysis through an intuitive conversational interface, powered by proprietary MCF (Market Context Framework) algorithms and real-time data integration.

**Result:** Retail and professional traders gain access to analysis previously reserved for hedge funds and prop trading desks.

---

## Target Audience

### Primary Users

1. **Active Crypto Traders**
   - Day traders and swing traders
   - Need: Real-time regime detection, entry/exit signals
   - Pain: Overtrading, poor timing, lack of context

2. **Quantitative Traders**
   - Algorithm developers, backtesting analysts
   - Need: Statistical edge validation, regime-aware strategies
   - Pain: Limited tooling for regime detection and microstructure analysis

3. **Professional Fund Managers**
   - Crypto hedge funds, family offices
   - Need: Risk management, portfolio optimization
   - Pain: Lack of institutional-grade crypto analytics

4. **Trading Educators & Mentorship Programs**
   - Trading coaches, education platforms
   - Need: Teaching tools, student analysis validation
   - Pain: Inability to scale personalized feedback

### Secondary Users

5. **Research Analysts**
   - Market researchers, content creators
   - Need: Data-driven insights, visualization tools

6. **Risk Managers**
   - Position monitoring, exposure analysis
   - Need: Real-time risk metrics, drawdown prevention

---

## Core Features

### 1. MCF Engine Integration (Proprietary)

**Multi-Context Framework** - Quantitative scoring system for trade quality

**Components:**
- **Structure Grade** (1-5): Price action quality assessment
- **Volume Confluence**: Smart money vs retail flow analysis
- **Multi-Timeframe Alignment**: Coherence across 15m/1H/4H/Daily/Weekly
- **Volatility Regime**: Expansion vs contraction detection
- **Momentum Quality**: Trend strength and persistence

**Output:** MCF Score (0-10) representing trade quality
- **8-10:** Institutional-grade setups (take max size)
- **6-8:** High-quality setups (standard position)
- **<6:** No trade / invalidated

**Differentiator:** No other platform combines structure, volume, and MTF alignment into a single actionable score.

---

### 2. Real-Time Market Analysis

**Live Data Sources:**
- Binance WebSocket (price, volume, funding rates)
- OrderFlow data (bid/ask imbalance, large orders)
- Options skew and implied volatility
- Funding rates and open interest

**Update Frequency:** Sub-second for price data, 1-minute for derived metrics

**Analysis Capabilities:**
- Current regime state (trending, ranging, volatile, compressed)
- Smart money positioning (institutional accumulation/distribution)
- Liquidity zones (support/resistance with volume confirmation)
- Entry timing (optimal execution windows)

---

### 3. Conversational Intelligence

**Fine-Tuned LLM:** Qwen 2.5 Coder 32B (specialized for trading)

**Training Data:**
- 200+ high-quality trading scenarios
- MCF methodology documentation
- Real trade post-mortems
- Quantitative analysis patterns

**Capabilities:**
- Natural language queries ("Is BTC ready to break out?")
- Context-aware responses (remembers conversation history)
- Structured analysis format (always includes score, direction, risk)
- Explainable reasoning (shows WHY a setup is valid/invalid)

**Response Time:** <500ms average (local inference)

---

### 4. Risk Intelligence Suite

**Kelly Criterion Position Sizing:**
- Optimal fraction calculation based on edge and win rate
- Portfolio value consideration
- Max drawdown constraints

**Risk Metrics:**
- Position size recommendations (in USD and % of portfolio)
- Stop-loss placement (ATR-based and structure-based)
- Take-profit targets (risk-reward optimization)
- Exposure limits (per-trade and portfolio-wide)

**Monte Carlo Simulation:**
- 10,000+ scenario backtests
- Probability distribution of outcomes
- Worst-case drawdown estimation

---

### 5. Topological Data Analysis (TDA)

**Advanced Market Geometry:**
- **Takens Embedding:** Phase space reconstruction of price dynamics
- **Persistence Diagrams:** Topological feature detection
- **Betti Curves:** Homology evolution for bubble detection
- **Stability Index:** Market structure robustness

**Use Case:** Detect regime changes before traditional indicators

**Scientific Basis:** Applied topology methods from academic research

---

### 6. Multi-Timeframe Regime Detection

**Hidden Markov Model (HMM):**
- Probabilistic state detection (trending, ranging, volatile, compressed)
- Transition probability matrix (regime persistence likelihood)
- Forward/backward algorithm for state inference

**WAVE Model:**
- Trend persistence analysis
- Identifies where trends sustain vs where markets chop

**Timeframes Analyzed:**
- 15-minute (micro structure)
- 1-hour (intraday context)
- 4-hour (swing context)
- Daily (position context)
- Weekly (macro trend)

**Alignment Score:** Measures coherence across timeframes (0-100%)

---

### 7. 3D Visualization Suite

**48 Interactive Visualizations:**

**Regime Analysis:**
- 3D scatter plots of market states
- Convex hull cluster boundaries
- Animated evolution through state space

**Signal Intelligence:**
- MCF score surface across volatility/returns
- Signal manifold in factor space
- Entry/exit surface topology

**Risk Geometry:**
- Kelly Criterion 3D surface
- Kerr risk geometry (spacetime analogy)
- Drawdown landscape

**Market Microstructure:**
- Liquidity waterfall (HVN/LVN/fast flow)
- Volume Profile VR
- Multi-shot entry surfaces

**Technology:** Plotly.js (WebGL-accelerated 3D rendering)

---

## Technical Architecture

### System Components

```
┌─────────────────────────────────────────────────────────────┐
│                     FRONTEND (React/Vite)                    │
│  ┌──────────────────┐  ┌─────────────────────────────────┐ │
│  │  IROS Terminal   │  │   3D Visualization Suite        │ │
│  │  Chat Interface  │  │   (48 interactive dashboards)   │ │
│  └──────────────────┘  └─────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────┘
                            │ HTTP/WebSocket
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                  BACKEND (FastAPI/Python)                    │
│  ┌──────────────────┐  ┌─────────────────┐                 │
│  │  API Gateway     │  │  WebSocket Hub  │                 │
│  └──────────────────┘  └─────────────────┘                 │
│  ┌──────────────────┐  ┌─────────────────┐                 │
│  │  MCF Analyzer    │  │  LLM Interface  │                 │
│  └──────────────────┘  └─────────────────┘                 │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                     CORE ENGINES                             │
│  ┌──────────────────┐  ┌─────────────────┐                 │
│  │  MCF Engine V2   │  │  Qwen 2.5 32B   │                 │
│  │  (Quant Logic)   │  │  (Fine-tuned)   │                 │
│  └──────────────────┘  └─────────────────┘                 │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                      DATA SOURCES                            │
│  ┌──────────────────┐  ┌─────────────────┐                 │
│  │  Binance API     │  │  Historical DB  │                 │
│  │  (Live Data)     │  │  (Backtests)    │                 │
│  └──────────────────┘  └─────────────────┘                 │
└─────────────────────────────────────────────────────────────┘
```

### Technology Stack

**Frontend:**
- **Framework:** React 18 + TypeScript
- **Build Tool:** Vite (fast dev server, optimized builds)
- **UI Library:** TailwindCSS (utility-first styling)
- **3D Graphics:** Plotly.js (WebGL rendering)
- **State Management:** React Context + Hooks
- **API Client:** Fetch API with custom error handling

**Backend:**
- **Framework:** FastAPI (async Python web framework)
- **LLM Inference:** Ollama (local model serving)
- **Quant Engine:** Custom Python (NumPy, Pandas, SciPy)
- **WebSocket:** FastAPI WebSocket support
- **Data Processing:** Pandas, NumPy, TA-Lib

**AI Model:**
- **Base Model:** Qwen 2.5 Coder 32B
- **Fine-tuning:** LoRA adapters (200+ examples)
- **Context Window:** 128K tokens
- **Quantization:** 8-bit for optimal inference speed
- **Hosting:** Self-hosted (no API dependencies)

**Data Infrastructure:**
- **Market Data:** Binance WebSocket (real-time)
- **Historical Data:** Parquet files (compressed columnar storage)
- **Caching:** In-memory (Redis-like patterns)

**Deployment:**
- **Frontend:** Vercel (global CDN, instant deployments)
- **Backend:** Self-hosted on Helsinki VM (low-latency data access)
- **LLM:** Local inference on dedicated GPU hardware

---

## Key Differentiators

### vs Bloomberg Terminal

| Feature | Bloomberg Terminal | IROS Terminal |
|---------|-------------------|---------------|
| **Price** | $24,000/year | Subscription-based (affordable) |
| **AI Assistant** | Generic, no trading context | Fine-tuned for trading, MCF-aware |
| **Crypto Focus** | Limited | Native, real-time |
| **Position Sizing** | Manual | Automated (Kelly Criterion) |
| **Regime Detection** | Basic | Multi-timeframe HMM + WAVE |
| **Visualization** | 2D charts | 48 interactive 3D dashboards |
| **Learning Curve** | Steep | Conversational interface |

### vs TradingView

| Feature | TradingView | IROS Terminal |
|---------|-------------|---------------|
| **AI Analysis** | None | Full LLM integration |
| **Quantitative Models** | Manual indicators | Automated MCF scoring |
| **Risk Management** | Manual | Kelly Criterion, Monte Carlo |
| **Multi-Timeframe** | Visual only | Algorithmic alignment scoring |
| **Market Context** | User interpretation | AI-generated narrative |
| **3D Visualization** | None | 48 dashboards |

### vs ChatGPT/Claude for Trading

| Feature | Generic LLMs | IROS Terminal |
|---------|--------------|---------------|
| **Real-Time Data** | None | Live Binance integration |
| **Trading Models** | Generic advice | Proprietary MCF Engine |
| **Position Sizing** | None | Kelly Criterion calculation |
| **Regime Awareness** | None | Multi-timeframe HMM detection |
| **Backtesting** | None | Monte Carlo simulation |
| **Risk Metrics** | Generic | Stop-loss, take-profit, exposure |

---

## Use Cases

### 1. Pre-Trade Analysis

**Scenario:** Trader sees BTC breaking resistance

**IROS Workflow:**
1. User: "Analyze BTC for a long position"
2. IROS fetches live data (price, volume, funding, options skew)
3. MCF Engine calculates score (structure, volume, MTF alignment)
4. LLM generates analysis with:
   - Current regime state
   - MCF score and breakdown
   - Entry price recommendation
   - Position size (Kelly-optimized)
   - Stop-loss placement
   - Take-profit targets
   - Risk assessment

**Output:**
```
BTC/USDT Analysis - LONG BIAS

MCF Score: 7.8/10 (HIGH QUALITY)
Direction: LONG
Regime: TRENDING (4H+), EXPANSION (volatility)

ENTRY: $43,250 - $43,500
STOP: $42,100 (2.8% risk)
TARGET 1: $45,200 (4.2% gain, 1.5R)
TARGET 2: $47,800 (10.5% gain, 3.75R)

Position Size: $5,420 (5.4% of portfolio, Kelly-optimized)

REASONING:
✓ Structure: Grade 4/5 (clean breakout, volume confirmation)
✓ MTF Alignment: 82% (15m/1H/4H/D aligned bullish)
✓ Volume: Smart money accumulation (+18% institutional flow)
✓ Volatility: Expanding (breakout environment)
⚠ Funding: Slightly elevated (monitor for overheating)
```

---

### 2. Risk Monitoring

**Scenario:** Trader has open positions, wants real-time risk assessment

**IROS Workflow:**
1. User: "Monitor my BTC long from $43,300, stop at $42,100"
2. IROS tracks live price and calculates:
   - Distance to stop-loss
   - Current risk percentage
   - Trailing stop recommendations
   - Regime changes (early exit signals)

**Output:**
```
POSITION MONITOR: BTC LONG

Entry: $43,300
Current: $44,180 (+2.03%)
Stop: $42,100 (5.2% below current)

Risk Status: GREEN (price above entry, stop intact)

Regime Update: Still TRENDING (no change)
Suggestion: Consider trailing stop to $43,000 (breakeven + spread)

Next resistance: $45,200 (previous high)
Watch for: Funding rate spike (overheating signal)
```

---

### 3. Post-Trade Review

**Scenario:** Trader closed a losing trade, wants to understand why

**IROS Workflow:**
1. User: "Why did my ETH long from $2,300 fail?"
2. IROS analyzes:
   - MCF score at entry time
   - Regime state during trade
   - Volume profile (institutional flow)
   - Multi-timeframe alignment

**Output:**
```
TRADE POST-MORTEM: ETH LONG ($2,300)

Entry MCF Score: 5.2/10 (BORDERLINE)

Issues Identified:
✗ Structure: Grade 2/5 (choppy, no clear breakout)
✗ MTF Misalignment: 4H bearish, Daily neutral (conflicting)
✗ Volume: Retail-driven (no institutional support)
✓ Volatility: Correct (expansion phase)

Lesson: Entry was below MCF threshold (6.0). 
Structure grade of 2/5 indicated choppy conditions.
4H/Daily misalignment suggested waiting for higher TF confirmation.

Recommendation: Next time, wait for MCF 6.5+ and MTF alignment >70%
```

---

### 4. Market Research

**Scenario:** Analyst preparing market report

**IROS Workflow:**
1. User: "Give me a comprehensive market overview"
2. IROS generates:
   - Regime state across major pairs
   - Volatility landscape
   - Sentiment indicators
   - Key levels and zones

**Output:**
```
MARKET OVERVIEW - Crypto (Jan 19, 2026)

REGIME STATE:
- BTC: TRENDING (Daily+), EXPANSION
- ETH: RANGING (4H), COMPRESSION
- SOL: TRENDING (Weekly+), EXPANSION

VOLATILITY:
- BTC: 45% (elevated, breakout mode)
- ETH: 28% (compressed, coiling)
- SOL: 62% (very high, trending)

SENTIMENT:
- Funding rates: Neutral to slightly bullish
- Options skew: Call bias (bullish)
- Institutional flow: Accumulation phase

RECOMMENDATION:
Focus on BTC and SOL (trending + expansion = tradeable).
Wait on ETH (ranging + compression = chop risk).
```

---

## Performance Metrics

### System Performance

- **Response Time:** <500ms (95th percentile)
- **Uptime:** 99.5% (backend)
- **Data Latency:** <100ms (Binance → IROS)
- **Concurrent Users:** Supports 100+ simultaneous sessions

### Analytical Accuracy

- **MCF Score Correlation:** 0.78 with realized trade outcomes
- **Regime Detection Accuracy:** 84% (validated against manual labels)
- **Kelly Sizing:** Reduces max drawdown by 40% vs fixed sizing

### User Outcomes

- **Average Win Rate Improvement:** +12% (compared to pre-IROS)
- **Risk-Adjusted Returns:** +35% (Sharpe ratio improvement)
- **Overtrading Reduction:** -60% (better trade selection)

*(Metrics based on beta user cohort, n=127, 90-day period)*

---

## Security & Compliance

### Data Privacy

- **No PII Storage:** No email, phone, or personal data collected
- **Trade Data:** Ephemeral (not logged unless user opts in)
- **API Keys:** Encrypted at rest (AES-256)
- **Self-Hosted LLM:** No data sent to third-party AI providers

### API Security

- **Authentication:** JWT tokens (short-lived, auto-refresh)
- **Rate Limiting:** 100 requests/minute per user
- **Input Validation:** All queries sanitized (prevent injection)
- **HTTPS Only:** TLS 1.3 for all communications

### Model Security

- **Local Inference:** No cloud AI dependencies
- **Prompt Injection Defense:** Input filtering and validation
- **Context Isolation:** User sessions don't cross-contaminate

---

## Roadmap & Future Features

### Q1 2026 (Current Release)

- ✅ MCF Engine V2 integration
- ✅ Real-time Binance data
- ✅ Fine-tuned LLM (Qwen 2.5 32B)
- ✅ 48 3D visualizations
- ✅ Kelly Criterion position sizing

### Q2 2026 (Planned)

- 🔄 Multi-asset support (stocks, forex, commodities)
- 🔄 Portfolio-level risk management
- 🔄 Automated trade execution (via API)
- 🔄 Mobile app (iOS/Android)
- 🔄 Voice interface (audio queries)

### Q3 2026 (Planned)

- 🔮 Social trading integration (copy top performers)
- 🔮 Backtesting platform (test strategies)
- 🔮 Custom indicator builder
- 🔮 Institutional API (for hedge funds)

### Q4 2026 (Research)

- 🔮 Reinforcement learning for adaptive strategies
- 🔮 Cross-market regime correlation
- 🔮 DeFi protocol integration (on-chain data)

---

## Pricing Strategy (Proposed)

### Tier 1: IROS Lite
**$49/month**
- 100 queries/day
- Basic MCF analysis
- Real-time data (BTC, ETH only)
- Access to 10 core visualizations

### Tier 2: IROS Pro
**$149/month**
- Unlimited queries
- Full MCF Engine access
- All 48 visualizations
- Kelly sizing and risk management
- Multi-asset support
- Priority support

### Tier 3: IROS Institutional
**$999/month**
- Everything in Pro
- API access (programmatic queries)
- Custom model fine-tuning
- Dedicated infrastructure
- White-label option
- SLA guarantees

### Tier 4: IROS Enterprise
**Custom Pricing**
- Multi-user licenses
- On-premise deployment
- Custom integrations
- Regulatory compliance support
- Dedicated account manager

---

## Success Metrics

### User Acquisition

- **Target:** 1,000 paying users by Q2 2026
- **CAC Target:** <$150 (via content marketing, social)
- **Conversion Rate:** 15% (free trial → paid)

### User Retention

- **Target Churn:** <5% monthly
- **DAU/MAU Ratio:** >40% (sticky product)
- **NPS Score:** >60 (promoter threshold)

### Revenue

- **Q2 2026 Target:** $100K MRR
- **Q4 2026 Target:** $500K MRR
- **LTV/CAC Ratio:** >3.0

### Product Engagement

- **Avg Queries/User/Day:** 15+
- **Session Length:** 12+ minutes
- **Visualization Views:** 5+ per session

---

## Competitive Moat

### 1. Proprietary MCF Engine
- 7 years of development
- Validated across 500K+ community members
- 79.17% average win rate (student outcomes)
- Cannot be easily replicated

### 2. Fine-Tuned LLM
- 200+ high-quality training examples
- Trading-specific knowledge base
- Self-hosted (no API dependencies)

### 3. Real-Time Integration
- Direct Binance WebSocket connection
- Sub-100ms latency
- Live regime detection

### 4. 3D Visualization Suite
- 48 unique dashboards
- Scientific publication quality
- Interactive WebGL rendering

### 5. Network Effects
- User-generated trade reviews improve model
- Community feedback loop
- Social proof from outcomes

---

## Technical Requirements (For Frontend Dev Team)

### Frontend Deliverables

1. **Landing Page**
   - Hero section with IROS Terminal demo
   - Feature showcase (MCF Engine, 3D viz, risk management)
   - Pricing table
   - Testimonials / social proof
   - CTA: "Start Free Trial"

2. **Product Page**
   - Detailed feature breakdown
   - Use case walkthroughs (with screenshots)
   - Integration documentation
   - API reference (for institutional tier)

3. **Dashboard UI**
   - Embedded IROS chat interface
   - Quick access to 3D visualizations
   - Portfolio overview (positions, risk metrics)
   - Settings (API keys, preferences)

4. **Visualization Gallery**
   - Grid view of all 48 dashboards
   - Category filters (regime, risk, microstructure, etc.)
   - Search functionality
   - Embed/share options

5. **Documentation Site**
   - Getting started guide
   - MCF methodology explanation
   - API documentation
   - Video tutorials
   - FAQ

### Design Guidelines

**Brand Aesthetic:**
- **Style:** Cyberpunk institutional (Bloomberg meets Sci-Fi)
- **Colors:** Black (#000000), Electric Blue (#00D4FF), Neon Green (#00FF88)
- **Typography:** Inter (UI), JetBrains Mono (code/terminal)
- **Vibe:** Professional, cutting-edge, data-driven

**UI Principles:**
- Dark mode by default (eye comfort for traders)
- Minimalist (no clutter, data-first)
- Fast (instant page loads, smooth animations)
- Accessible (WCAG 2.1 AA compliance)

**Key Pages:**
- `/` - Landing page
- `/product` - Feature deep-dive
- `/pricing` - Pricing tiers
- `/terminal` - IROS chat interface (auth required)
- `/visualizations` - 3D dashboard gallery
- `/docs` - Documentation
- `/api` - API reference

---

## Integration APIs (For Developers)

### REST API Endpoints

```
POST /api/mcf/analyze
Body: { symbol: "BTCUSDT", direction: "LONG" }
Returns: MCF analysis object

GET /api/mcf/context/{symbol}
Returns: Formatted context for LLM injection

POST /api/chat
Body: { message: "Analyze BTC", context: {} }
Returns: AI response with analysis

GET /api/market/regimes
Returns: Current regime state across all assets

POST /api/risk/kelly
Body: { portfolio_value, win_rate, avg_win, avg_loss }
Returns: Optimal position size

GET /api/visualizations/list
Returns: Available 3D dashboard URLs
```

### WebSocket API

```
ws://api.iros.mcfenterprise.com/live

Subscribe to:
- market.btcusdt (live price updates)
- mcf.score.btcusdt (real-time MCF score changes)
- regime.change.btcusdt (regime shift notifications)
```

---

## Conclusion

**IROS Terminal** represents the convergence of institutional quant finance, cutting-edge AI, and intuitive user experience. By combining proprietary trading models (MCF Engine), real-time market data, and a fine-tuned LLM, IROS delivers analysis previously accessible only to hedge funds and prop trading desks.

**For Frontend Developers:** You're building the interface to a genuinely differentiated product. Every feature has quantitative backing. Every visualization represents real edge. Every analysis is grounded in 7 years of trading methodology development.

**This isn't a ChatGPT wrapper. This is institutional-grade infrastructure.**

---

**Document Version:** 1.0  
**Last Updated:** January 19, 2026  
**Status:** Ready for Frontend Development  
**Contact:** Via MCF Enterprise website for technical inquiries

