# MCF Labs - 3D Visualization Suite

![MCF Labs](https://img.shields.io/badge/MCF-Labs-00ff88?style=for-the-badge)
![Visualizations](https://img.shields.io/badge/Visualizations-48-blue?style=for-the-badge)
![Tech](https://img.shields.io/badge/Tech-Plotly.js-purple?style=for-the-badge)

**Institutional-Grade 3D Trading Analytics** | Built by [Maximus Fay](https://github.com/LUGIAAAAA)

---

## 🚀 **Live Demo**

Start here: **[Open index.html](./index.html)** or **[MCF ULTRA Suite](./mcf_ultra_suite.html)**

---

## 📊 **What's Inside**

**48 interactive 3D visualizations** for quantitative trading analysis:

- 🔬 **MCF ULTRA Core** - 5 advanced institutional analytics
- 🧠 **IROS Neural Architecture** - AI model topology visualizations  
- 📈 **Regime Analysis** - Multi-timeframe market state detection
- 🌐 **TDA Suite** - Topological Data Analysis for bubble detection
- 💎 **Risk Intelligence** - Kelly Criterion & risk geometry
- 📉 **Backtest Animations** - Walk-forward equity curves
- ⚡ **Live Dashboards** - Real-time market intelligence

---

## 🎯 **Featured Visualizations**

### 🔥 MCF ULTRA Suite
The crown jewels of quant analytics:

1. **[Regime Dynamics Surface](./mcf_regime_surface.html)** - 3D MCF score across volatility/returns
2. **[TDA Bubble Landscape](./mcf_tda_bubble.html)** - Topological bubble detection
3. **[Signal Strength Manifold](./mcf_signal_manifold.html)** - 3D tradeable signal regions
4. **[HMM Transition Topology](./mcf_hmm_topology.html)** - Hidden Markov state transitions
5. **[Equity-Regime Correlation](./mcf_equity_regime.html)** - Backtest with regime overlays

### 🧠 IROS Neural Architecture
AI model visualizations:

- **[IROS Neural INSANE](./iros_neural_insane.html)** - Volumetric neural network rendering
- **[IROS Neural 3D](./iros_neural_3d.html)** - 32B parameter hierarchical architecture

### 🌐 Topological Data Analysis
Advanced market topology:

- **[Takens Embedding](./tda_takens.html)** - Phase space reconstruction
- **[Persistence Diagram](./tda_persistence.html)** - Topological feature birth/death
- **[Betti Curves](./tda_betti.html)** - Homology evolution
- **[Stability Index](./tda_stability.html)** - Bubble signals over time

---

## 💻 **Tech Stack**

- **Plotly.js** - 3D rendering engine
- **HTML5/CSS3** - Pure web standards (no build process)
- **Vanilla JavaScript** - Zero dependencies beyond Plotly
- **Responsive Design** - Works on desktop, tablet, mobile

---

## 🎨 **Design Philosophy**

**Cyberpunk Institutional** - Bloomberg Terminal meets MIT Research Lab

- Dark backgrounds for eye comfort during late-night analysis
- Neon accents (cyan/green/pink) for data hierarchy
- Glass morphism UI elements
- Smooth animations and transitions
- Interactive 3D controls (rotate, zoom, pan, hover)

---

## 📦 **File Structure**

```
/
├── index.html                    # Main dashboard hub
├── mcf_ultra_suite.html          # MCF ULTRA entry point
├── iros_neural_insane.html       # Featured neural viz
│
├── /regime/                      # Market regime analysis
│   ├── regime_3d_scatter.html
│   ├── regime_3d_clusters.html
│   ├── regime_3d_evolution.html
│   └── regime_state_surface.html
│
├── /tda/                         # Topological analysis
│   ├── tda_takens.html
│   ├── tda_persistence.html
│   ├── tda_betti.html
│   └── tda_stability.html
│
├── /microstructure/              # Market microstructure
│   ├── mcf_entry.html
│   ├── exit_surface_3d.html
│   └── mcf_vpvr.html
│
└── [40+ additional visualizations]
```

---

## 🚀 **Quick Start**

### **Option 1: Open Locally**
1. Clone this repo
2. Open `index.html` in your browser
3. Navigate to any visualization

```bash
git clone https://github.com/LUGIAAAAA/MCF-3D-GRAPHS.git
cd MCF-3D-GRAPHS
# Open index.html in your browser
```

### **Option 2: Static Hosting**
Upload to any static host:
- **Vercel:** `vercel deploy`
- **Netlify:** Drag folder to Netlify Drop
- **GitHub Pages:** Enable in repo settings
- **Cloudflare Pages:** Connect repo

### **Option 3: Integrate into Your Site**

**Iframe Embed:**
```html
<iframe src="https://your-domain.com/mcf_ultra_suite.html" 
        width="100%" 
        height="800px" 
        frameborder="0">
</iframe>
```

**Direct Link:**
```html
<a href="/visualizations/mcf_ultra_suite.html" target="_blank">
  View MCF ULTRA Suite
</a>
```

**React/Next.js:**
```jsx
// Place files in /public/dashboards/
<Link href="/dashboards/mcf_ultra_suite.html">
  MCF ULTRA Suite
</Link>
```

---

## 📊 **All Visualizations**

### MCF Core Analytics
- `mcf_regime_surface.html` - Regime dynamics 3D surface
- `mcf_tda_bubble.html` - Topological bubble detection
- `mcf_signal_manifold.html` - Signal strength 3D
- `mcf_hmm_topology.html` - HMM state transitions
- `mcf_equity_regime.html` - Equity with regimes
- `mcf_framework_dashboard.html` - Complete MCF framework
- `mcf_neural_flow.html` - Neural flow visualization

### Multi-Timeframe Analysis
- `mcf_mtf.html` - Multi-timeframe alignment
- `mcf_cone.html` - Timeframe cone
- `mcf_crystal.html` - Crystal structure
- `mcf_time_dynamics.html` - Time dynamics

### Market Microstructure
- `mcf_entry.html` - Entry analysis
- `exit_surface_3d.html` - 3D exit surface
- `exit_intelligence_surface.html` - Exit intelligence
- `multishot_entry_surface.html` - Multi-shot entries
- `mcf_vpvr.html` - Volume Profile VR
- `mcf_waterfall.html` - Liquidity waterfall
- `microstructure_combined.html` - Combined microstructure

### Regime Detection
- `regime_3d_scatter.html` - 3D regime scatter
- `regime_3d_clusters.html` - Regime clusters
- `regime_3d_evolution.html` - Evolution animation
- `regime_state_surface.html` - State surface

### IROS Neural
- `iros_neural_insane.html` - Volumetric rendering
- `iros_neural_3d.html` - 3D architecture
- `iros_neural_animated.html` - Animated version
- `iros_neural_architecture.png` - Static render

### Topological Data Analysis
- `tda_takens.html` - Takens embedding
- `tda_persistence.html` - Persistence diagram
- `tda_betti.html` - Betti curves
- `tda_stability.html` - Stability index

### Risk & Kelly
- `kelly_risk_surface.html` - Kelly surface
- `kerr_risk_geometry.html` - Risk geometry
- `risk_intelligence_comparison.html` - Risk comparison

### Advanced Physics-Inspired
- `mcf_zeta_field.html` - Zeta field
- `mcf_hawking_temperature.html` - Hawking temperature
- `volatility_manifold.html` - Volatility manifold
- `multiscale_decomposition.html` - Multiscale analysis

### Backtest & Performance
- `mcf_backtest_2022.html` - 2022 backtest
- `backtest_animation.html` - Equity animation
- `drawdown_animation.html` - Drawdown underwater
- `sharpe_animation.html` - Rolling Sharpe
- `monte_carlo_10k.html` - 10K simulations
- `multi_trade_comparison.html` - Trade comparison

### Live Dashboards
- `mcf_live_dashboard.html` - Real-time market data
- `agent_coordination.html` - Multi-agent tracking

### Combined
- `combined_surfaces.html` - Multiple surfaces

---

## 🎯 **Use Cases**

### For Traders
- Analyze multi-timeframe alignment
- Identify regime shifts before they happen
- Visualize risk/reward in 3D space
- Understand market microstructure

### For Quants
- Validate backtests with regime overlays
- Detect bubbles using topological methods
- Optimize Kelly position sizing
- Study HMM state transitions

### For Researchers
- Publication-quality visualizations
- Advanced topology & manifold analysis
- Neural network architecture viz
- Custom algorithm validation

### For Educators
- Interactive teaching tools
- Intuitive 3D explanations
- Real-time market dynamics
- Institutional-grade examples

---

## 🔧 **Customization**

All visualizations can be customized:

1. **Data:** Replace inline data arrays with your own
2. **Colors:** Modify color scales in each file
3. **Layout:** Adjust camera angles, margins, fonts
4. **Interactivity:** Add custom click/hover handlers

Example:
```javascript
// In any HTML file, find the Plotly.newPlot() call:
Plotly.newPlot('myDiv', data, layout, config);

// Modify layout:
layout.scene.camera.eye = {x: 2, y: 2, z: 1.5};
layout.coloraxis.colorscale = 'Viridis';
```

---

## 📈 **Performance**

- **File Sizes:** 100KB - 50MB (data embedded inline)
- **Load Times:** 1-5 seconds on modern hardware
- **Rendering:** 60 FPS on discrete GPU
- **Browser Support:** Chrome, Firefox, Safari, Edge (latest)

**Optimization Tips:**
- Serve from CDN for production
- Enable gzip compression
- Consider lazy loading for many visualizations
- Extract data to API for dynamic updates

---

## 🤝 **Contributing**

Want to add your own visualizations?

1. Fork this repo
2. Create a new HTML file following the existing style
3. Add it to `index.html` or `mcf_ultra_suite.html`
4. Submit a pull request

**Guidelines:**
- Use Plotly.js for consistency
- Follow dark theme aesthetic
- Include formula/description
- Make it interactive
- Test on multiple browsers

---

## 📄 **License**

**Proprietary** - © 2026 MCF Labs

These visualizations are proprietary to MCF Labs. For licensing inquiries, contact:
- **Website:** [mcfenterprise.com](https://mcfenterprise.com)
- **Email:** Contact via website

---

## 🌟 **Built By**

**Maximus Fay** - Forbes at 18, Founder of MCF Labs

- Featured in Forbes for trading education innovation
- 500,000+ community members across platforms
- 79.17% average student win rate
- Built everything you see here (no agencies, no outsourcing)

**Connect:**
- **X/Twitter:** [@MaximusFays](https://twitter.com/MaximusFays)
- **YouTube:** [@marketmakermax](https://youtube.com/@marketmakermax)
- **Telegram:** [t.me/marketmakermax](https://t.me/marketmakermax)

---

## 🔗 **Related Projects**

- **[MCF-Project](https://github.com/LUGIAAAAA/MCF-Project)** - Complete MCF trading framework
- **[IROS Terminal](https://github.com/LUGIAAAAA/IROS_Lives)** - AI-powered trading assistant
- **[Research-Viz](https://github.com/LUGIAAAAA/Research-visualization)** - Visualization toolkit

---

## 🙏 **Acknowledgments**

Built with:
- **Plotly.js** - Incredible 3D graphing library
- **HTML5/CSS3** - Web standards that just work
- **Countless hours at 4am** - The polymath grind

Inspired by:
- Bloomberg Terminal aesthetics
- MIT Research Lab visualizations
- Quant research papers
- The 0.0001% mindset

---

## 📊 **Stats**

- **48 HTML Visualizations** + 1 PNG
- **~500MB Total** (data embedded)
- **Plotly.js 3D Engine**
- **100% Self-Contained** (no backend required)
- **Built Solo** (no dev team)

---

<div align="center">

**⭐ Star this repo if these visualizations helped you!**

**Built with obsession. Shared with purpose.**

**MCF Labs | Institutional Quant Research | 2026**

</div>

