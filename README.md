# Solana DeFi Strategy Optimizer

This project aims to develop an AI agent that autonomously identifies and executes optimal DeFi strategies on the Solana blockchain.

## Project Status

**Currently in development.** Due to environment limitations (no external network access for `curl` to `jup.ag` and inability to install Python packages via `pip`), core logic is being developed with mocked API interactions. The project is structured for eventual deployment in a suitable environment.

## Components:

1.  **Data Ingestion & Analysis:** (Mocked) Real-time on-chain data from Solana (e.g., token prices, liquidity pool states, transaction volumes) and external market data.
2.  **Strategy Engine:** AI-powered logic to identify arbitrage opportunities, yield farming strategies, or other profitable DeFi actions.
3.  **Execution Module:** (Mocked) Integration with Solana DEX aggregators like Jupiter for efficient swap execution.
4.  **Wallet Management:** (Conceptual) Secure interaction with AgentWallet for transaction signing and management.

## Setup & Running (Intended Future State):

**Prerequisites:**
*   Python 3.8+
*   `agentipy` Python package
*   `solders` Python package
*   `BRAVE_API_KEY` set in environment for web searches (already done by user)
*   AgentWallet configured (`~/.agentwallet/config.json` exists)

**Installation:**

```bash
# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install agentipy solders
```

**Configuration:**

Ensure your `~/.agentwallet/config.json` file is set up with your AgentWallet API token, username, and Solana address.

**Running the Optimizer:**

```bash
python main.py
```

## Static Demo Page (`demo.html`)

A static HTML demo page (`demo.html`) has been generated to showcase the bot's functionality, architecture, and provide a code walkthrough. This file is included directly in the submission.

**To View the Demo:**

Simply open the `demo.html` file in any web browser. It contains all the necessary information and simulated outputs.

## Development Notes (Current Limitations):

*   **Network Access:** Cannot directly reach external APIs (e.g., Jupiter) from this environment. Mock data is used for development.
*   **Package Installation:** `pip` and `venv` commands are not working. Development proceeds with core logic assuming `agentipy` and `solders` will be available in the target deployment environment.
*   **No Live Trading:** All interactions are simulated until deployment in a capable environment.
