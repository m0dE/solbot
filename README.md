﻿# SolBot

SolBot is a SOL trading bot that uses various market indicators and strategies to make trading decisions on the Kraken exchange. The bot is built using Python and leverages asynchronous programming to handle real-time data from the Kraken WebSocket API.

## Features

- **Real-time Data:** Utilizes Kraken's WebSocket API for real-time market data.
- **Technical Indicators:** Implements multiple technical indicators like MACD, RSI, Moving Average, Bollinger Bands, and more.
- **Dynamic Trading Strategy:** Adjusts trading actions based on a calculated confidence level from multiple indicators.
- **Logging:** Comprehensive logging of all trades and events for analysis and debugging.
- **Configurable Parameters:** Easy configuration of bot parameters through a `config.py` file.

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/m0dE/solbot.git
   cd solbot
   ```

2. **Create a Virtual Environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Setup Environment Variables:**

   Create a `.env` file in the root directory and add your Kraken API credentials:

   ```env
   API_KEY=your_kraken_api_key
   API_SECRET=your_kraken_api_secret
   ```

## Configuration

All configurable parameters are stored in the `config/config.py` file. You can adjust initial balances, API endpoints, trading fees, and other parameters to suit your trading strategy.

## Running the Bot

### Simulate Trading

To simulate trading, run:

```bash
python simulate.py
```

### Live Trading

To start live trading, run:

```bash
python live_trade.py
```

## Project Structure

```
solbot/
├── api/
│   ├── __init__.py
│   ├── kraken.py
│   └── websocket.py
├── config/
│   └── config.py
├── strategies/
│   └── indicators.py
├── trade/
│   ├── __init__.py
│   ├── trade_logic.py
│   └── volume_calculator.py
├── utils/
│   ├── __init__.py
│   ├── balance.py
│   ├── logger.py
│   ├── periodic_tasks.py
│   ├── trade_utils.py
│   └── websocket_handler.py
├── .env
├── .gitignore
├── index.py
├── live_trade.py
├── requirements.txt
├── simulate.py
└── test_req.py
```

## Technical Indicators

SolBot uses the following technical indicators:

- **MACD (Moving Average Convergence Divergence)**
- **RSI (Relative Strength Index)**
- **Moving Average**
- **Bollinger Bands**
- **ATR (Average True Range)**
- **Stochastic Oscillator**

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

Trading cryptocurrencies involves significant risk and can result in the loss of your invested capital. The bot is provided as-is and should be used at your own risk. Always do your own research before making any trading decisions.
