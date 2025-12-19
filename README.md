### Stay tuned! 👋
![Fu510nTraderNQ](https://github.com/user-attachments/assets/364c172b-42b8-4915-8f46-c4a55cc07abf)

Python-based trading platform with:
- Simulator with real-time & user-specifiable market replay speeds
- DTN/IQFeed data integration (download & live chart updates)
- Interactive Brokers, Alpaca & CCXT broker integration
- Algo backtesting
- Bar "microscope" (displays ticks for selected bar and prior)
- Strategy optimization engine (with indicator data caching for performance)

# A.V.A. Trading System (Adaptive Velocity/Acceleration)

A sophisticated algorithmic trading platform refactored from Python-based _**Fu510nTrader**_ and legacy TradeStation & MotiveWave automated strategies, combining real-time futures market analysis with advanced visualization and machine learning capabilities. Built with React (TypeScript) and Python, A.V.A. provides a comprehensive suite of tools for market analysis, strategy development, and automated trading execution.

<img width="1920" height="1200" alt="FT_ESNQ" src="https://github.com/user-attachments/assets/4f6b4899-eae7-47d0-84e4-23847890e080" />

## Core Features

### Advanced Market Analysis
- Real-time tick data processing from IQFeed
- Custom Renko bar generation with high/low wicks
- Extensive technical indicator library (20+ indicators including ADX, PPO, MFI, Velocity)
- Order flow analysis with bid/ask aggressor tracking
- Real-time chart data management with AVAContext

### Trading Strategy System
- **Modular Strategy Architecture**: Pluggable strategy system with standardized interfaces
- **Built-in Strategies**: MoneyFlow, ADXBreakout, and extensible framework for developing custom strategies
- **Strategy Factory**: Dynamic strategy creation and management
- **Real-time Execution**: Bar-level and tick-level strategy execution
- **Strategy Validation**: Built-in settings validation and error handling

### Comprehensive Backtesting Engine
- **Real-time Data Integration**: Uses existing chart data and calculated indicators
- **Position Management**: Automatic TP/SL handling, position tracking, and trade recording
- **Multi-Strategy Support**: Execute multiple strategies simultaneously on different charts
- **Performance Analytics**: Win rate, P&L, drawdown, and comprehensive metrics
- **Workspace Integration**: Automatically detects charts with assigned strategies
- **Progress Tracking**: Real-time progress updates with pause/resume functionality

### Machine Learning Integration
- Feature engineering for tick and bar data
- Multiple model implementations (Random Forest, XGBoost, KNN)
- Fractal pattern detection and pivot point analysis
- Physics-inspired market metrics (velocity, acceleration)

### Modern React Frontend
- Interactive charting with **amCharts 5**
- Customizable workspace layouts
- Real-time performance analytics and backtest results
- Advanced sound notification system
- Comprehensive trading controls and parameter management
- **Analytics Panel**: Performance summary, trades list, equity curves, and more

### Robust Backend Architecture
- **SQLite** database for efficient tick data storage
- High-performance data processing with **Polars**
- Parallel strategy testing framework
- Comprehensive backtesting engine
- **TypeScript Backend**: Full TypeScript implementation for type safety
- **Context-based State Management**: React Context API for global state
- **Event-driven Architecture**: Custom DOM events for efficient component communication
- **Modular Component Design**: Reusable components with clear separation of concerns

## Technical Stack

### Frontend
- **React 18** with TypeScript for type safety
- **amCharts 5** for advanced visualization
- **Real-time data streaming** with WebSocket support
- **Modular component architecture** with custom hooks
- **Context API** for global state management
- **Custom event system** for efficient component communication

### Backend
- Python for core processing
- SQLite for data storage
- Polars for high-performance data operations
- Comprehensive testing framework
- **TypeScript** for core processing and type safety
- **React Context** for state management
- **Custom hooks** for reusable logic
- **Strategy pattern** for extensible trading algorithms

### Machine Learning
- scikit-learn for model training
- XGBoost for gradient boosting
- Custom feature engineering pipeline
- Advanced statistical analysis tools

### Testing Framework
- **Vitest** for fast, modern testing
- **Real data integration** using historical market data
- **Integration tests** for backtesting engine
- **Unit tests** for strategies and components
- **Test data loader** for realistic testing scenarios

### Data Integration
- IQFeed integration with real-time & historical market data handling
- Custom tick data processing
- **Local JSON data** for development and testing
- **Real-time chart data** management
- **Indicator calculation** and caching
- **Historical data** processing and storage

## Project Structure

```
ava/
├── src/
│   ├── ui/                    # React TypeScript frontend
│   │   ├── components/        # React components
│   │   │   ├── panels/        # Main UI panels
│   │   │   ├── strategies/    # Trading strategy implementations
│   │   │   ├── backtest/      # Backtesting engine components
│   │   │   └── common/        # Shared UI components
│   │   ├── contexts/          # React Context providers
│   │   ├── hooks/             # Custom React hooks
│   │   ├── services/          # Frontend services
│   │   ├── types/             # TypeScript type definitions
│   │   └── tests/             # Comprehensive test suite
│   ├── features/              # Technical indicators
│   ├── filters/               # Trading filters
│   ├── strategies/            # Trading strategies
│   └── trading_system/        # Core backend
├── data/                      # Market data storage
├── docs/                      # Documentation and diagrams
├── notebooks/                 # Jupyter notebooks
└── public/                    # Static assets and test data
```

## Getting Started

1. Clone the repository
```bash
git clone [repository-url]
cd ava
```

2. Install Python dependencies
```bash
pip install -r requirements.txt
```

3. Install frontend dependencies
```bash
cd src/ui
npm install
```

4. Start the development server
```bash
# Frontend
cd src/ui
npm run dev (or preview)

# Backend (optional)
python src/app.py
```

5. Convert SQLite tick/bar data to JSON (in src/ui/public/data)
```bash
cd src/scripts
python sqlite2json.py ESU5 20250709
```

6. Run tests to verify installation
```bash
# All tests
npm test

# Specific test suites
npm run test:backtest
npm run test:strategies
npm run test:data-loader
```

## Features in Detail

### Technical Indicators
- **ADX** (Average Directional Index)
- **PPO** (Percentage Price Oscillator)
- **MFI** (Money Flow Index)
- **Velocity indicators**
- **Bollinger Bands**
- **EMA** (Exponential Moving Average)
- And many more...

### Trading Strategies
- **MoneyFlow Strategy**: Volume-based momentum analysis
- **ADX Breakout Strategy**: Trend strength and breakout detection
- **Extensible Framework**: Easy to add custom strategies
- **Strategy Validation**: Built-in settings validation
- **Real-time Execution**: Live strategy monitoring

### Backtesting System
- **Real Data Integration**: Uses actual historical market data
- **Position Management**: Automatic TP/SL, position tracking
- **Multi-Chart Support**: Test strategies across multiple symbols
- **Performance Metrics**: Comprehensive analytics and reporting
- **Workspace Integration**: Automatic strategy detection and execution

### Trading Tools
- Real-time order flow analysis
- Custom Renko bar generation
- Fractal pattern detection
- Support/Resistance levels
- Volume profile analysis
- Market depth visualization

### Risk Management
- Dynamic position sizing
- Automated stop-loss management
- Take-profit optimization
- Risk/reward ratio analysis
- Performance analytics
- **Real-time P&L tracking**

### Workspace Management
- Customizable layouts
- Multiple chart configurations
- **Strategy assignment** to charts
- Saved workspace states
- Real-time data synchronization
- Sound notifications

## Development

### Code Style
- TypeScript for frontend type safety
- Python type hints
- **TypeScript** for frontend type safety
- **React best practices** with functional components
- **Custom hooks** for reusable logic
- **Context API** for state management
- Comprehensive documentation
- **Vitest** for modern testing

### Testing
- **Unit tests** for individual components
- **Integration tests** for backtesting engine
- **Strategy tests** with real market data
- **Data loader tests** for realistic scenarios
- **Console output** for debugging

### Contributing
1. Fork the repository
2. Create a feature branch
3. Add tests for new functionality
4. Commit your changes
5. Push to the branch
6. Create a Pull Request

## Recent Updates

### Backtesting Engine (Latest)
- **Real-time data integration** with existing charts
- **Multi-strategy execution** on multiple charts
- **Automatic position management** with TP/SL
- **Comprehensive performance metrics**
- **Progress tracking** and pause/resume functionality

### Strategy System
- **Modular architecture** for easy extension
- **Built-in strategies** with validation
- **Real-time execution** capabilities
- **Workspace integration** for automatic detection

### Testing Framework
- **Vitest integration** for modern testing
- **Real data testing** with historical market data
- **Comprehensive test coverage** for all components
- **Integration testing** for complex workflows

## License

© 2020-2025 Guy Resh. All rights reserved.

## Contact

For questions or support, please contact [contact information].
