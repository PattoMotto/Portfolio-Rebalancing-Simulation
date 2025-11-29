# QuantSim: Portfolio Rebalancing Simulation

A professional browser-based portfolio rebalancing simulation engine that compares dynamic rebalancing strategies against buy-and-hold approaches using stochastic pricing models.

## 🎯 Features

- **Multiple Pricing Models**
  - Geometric Brownian Motion (GBM) - Standard drift-diffusion model
  - Ornstein-Uhlenbeck (OU) - Mean-reverting process for range-bound markets
  - Jump Diffusion - Models sudden market shocks and crashes

- **Dynamic Allocation Strategies**
  - Fixed Target - Maintain constant portfolio allocation
  - RSI-Based - Contrarian strategy that buys dips and sells rallies
  - ADX-Based - Trend-following strategy that increases exposure during strong trends

- **Flexible Rebalancing**
  - Threshold-based rebalancing (trigger on allocation drift)
  - Time-based rebalancing (periodic intervals)
  - Customizable transaction fees

- **Comprehensive Analytics**
  - Performance comparison (Strategy vs. Buy & Hold)
  - Maximum drawdown tracking
  - Transaction cost analysis
  - Real-time visualization of trades and allocations

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/PattoMotto/portfolio-rebalancing-simulation.git
   cd portfolio-rebalancing-simulation
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to the local development URL (typically `http://localhost:5173`)

## 📊 Usage

### Quick Setup Presets

Use the preset buttons to quickly configure common market scenarios:

- **Bull Trend** - Rising market with moderate volatility
- **Bear Trend** - Declining market with higher volatility
- **Range (OU)** - Sideways market with mean reversion
- **Crash Risk** - Market with sudden downside shocks
- **High Volatility** - No trend, high uncertainty

### Market Parameters

Configure the underlying asset price simulation:

- **Pricing Model** - Choose between GBM, OU, or Jump Diffusion
- **Duration** - Simulation period in days (30-1000)
- **Volatility** - Annual volatility (5%-200%)
- **Model-specific parameters** - Drift, mean reversion speed, jump intensity, etc.

### Strategy Configuration

Customize your rebalancing strategy:

- **Initial Capital** - Starting portfolio value
- **Allocation Mode** - Fixed, RSI-based, or ADX-based
- **Target Allocation** - Desired asset weight (for fixed mode)
- **Rebalance Trigger** - Threshold or time-based
- **Transaction Fees** - Cost per trade as percentage

## 🏗️ Architecture

This is a fully client-side application built with:

- **React** - UI framework
- **TypeScript** - Type-safe development
- **Recharts** - Data visualization
- **Tailwind CSS** - Styling
- **Vite** - Build tool and dev server

All simulations run entirely in the browser using pure JavaScript implementations of stochastic processes and technical indicators.

## 📈 Technical Details

### Pricing Models

1. **Geometric Brownian Motion (GBM)**
   - Models: `dS = μS dt + σS dW`
   - Best for: Trending markets with constant volatility

2. **Ornstein-Uhlenbeck (OU)**
   - Models: `dX = θ(μ - X) dt + σ dW`
   - Best for: Mean-reverting, range-bound markets

3. **Jump Diffusion**
   - Combines GBM with Poisson jump process
   - Best for: Markets with sudden shocks or crashes

### Technical Indicators

- **RSI (Relative Strength Index)** - Momentum oscillator for contrarian signals
- **ADX (Average Directional Index)** - Trend strength indicator
- **SMA (Simple Moving Average)** - Trend direction filter

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

## 🔗 Links

- [GitHub Repository](https://github.com/PattoMotto/portfolio-rebalancing-simulation)
- [Live Demo](https://pattomotto.github.io/portfolio-rebalancing-simulation/)

## 📝 Notes

This is a simulation tool for educational and research purposes. It does not constitute financial advice. Past performance does not guarantee future results.
