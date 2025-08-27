
# Gemini Code Development Guide

This document provides a comprehensive guide for developing the TradingAgentsWeb project. It outlines the project structure, workflow, libraries, components, and development process.

## Package Management

This project uses [uv](https://github.com/astral-sh/uv) as a package manager. `uv` is an extremely fast Python package installer and resolver, written in Rust.

## Project Structure

The project is organized into the following directories:

```
C:\Users\swarfte\Desktop\Coding\TradingAgentsWeb\
├───.env.example
├───.gitignore
├───.python-version
├───LICENSE
├───main.py
├───pyproject.toml
├───README.md
├───setup.py
├───uv.lock
├───assets\
├───cli\
└───tradingagents\
```

- **`.env.example`**: An example file for environment variables.
- **`.gitignore`**: A file that specifies which files and directories to ignore in a Git repository.
- **`.python-version`**: A file that specifies the Python version to use for this project.
- **`LICENSE`**: The license for the project.
- **`main.py`**: The main entry point of the application.
- **`pyproject.toml`**: A file that contains the project's dependencies and other metadata.
- **`README.md`**: The main README file for the project.
- **`setup.py`**: A file that contains the project's setup script.
- **`uv.lock`**: A file that contains the project's locked dependencies.
- **`assets`**: A directory that contains the project's assets, such as images and icons.
- **`cli`**: A directory that contains the project's command-line interface.
- **`tradingagents`**: The core directory of the project.

### `tradingagents` Directory

The `tradingagents` directory is organized into the following subdirectories:

- **`agents`**: This directory contains the different types of agents involved in the trading process, such as analysts, researchers, managers, risk management, and traders.
- **`dataflows`**: This directory is responsible for fetching and processing data from various sources like Finnhub, Google News, Reddit, and Yahoo Finance.
- **`graph`**: This directory contains the logic for the trading graph, including conditional logic, propagation, reflection, and signal processing. `trading_graph.py` defines the main `TradingAgentsGraph` class.

## Workflow

The project's workflow is as follows:

1.  The `main.py` file is the main entry point of the application.
2.  It initializes the `TradingAgentsGraph` class from `tradingagents/graph/trading_graph.py`.
3.  The `TradingAgentsGraph` class creates a graph of trading agents.
4.  The `propagate` method of the `TradingAgentsGraph` class is called to propagate information through the graph and make a trading decision.
5.  The `reflect_and_remember` method of the `TradingAgentsGraph` class is called to memorize mistakes and reflect on the trading decision.

## Libraries

The project uses the following libraries:

- **`akshare`**: A library for financial data.
- **`backtrader`**: A library for backtesting trading strategies.
- **`chainlit`**: A library for creating conversational AI applications.
- **`chromadb`**: A library for creating and managing vector databases.
- **`eodhd`**: A library for financial data.
- **`feedparser`**: A library for parsing RSS feeds.
- **`finnhub-python`**: A library for financial data.
- **`langchain-anthropic`**: A library for using Anthropic models with LangChain.
- **`langchain-experimental`**: A library for experimental features in LangChain.
- **`langchain-google-genai`**: A library for using Google Generative AI models with LangChain.
- **`langchain-openai`**: A library for using OpenAI models with LangChain.
- **`langgraph`**: A library for creating and managing graph-based applications.
- **`pandas`**: A library for data analysis.
- **`parsel`**: A library for parsing HTML and XML.
- **`praw`**: A library for interacting with the Reddit API.
- **`python-dotenv`**: A library for managing environment variables.
- **`pytz`**: A library for working with timezones.
- **`questionary`**: A library for creating interactive command-line prompts.
- **`redis`**: A library for interacting with Redis.
- **`requests`**: A library for making HTTP requests.
- **`rich`**: A library for creating rich and beautiful command-line interfaces.
- **`setuptools`**: A library for creating Python packages.
- **`stockstats`**: A library for calculating stock statistics.
- **`tqdm`**: A library for creating progress bars.
- **`tushare`**: A library for financial data.
- **`typing-extensions`**: A library for providing runtime support for type hints.
- **`yfinance`**: A library for financial data.

## Components

The project is composed of the following components:

- **Agents**: The agents are responsible for performing specific tasks in the trading process.
- **Dataflows**: The dataflows are responsible for fetching and processing data from various sources.
- **Graph**: The graph is responsible for orchestrating the trading process.

## Development

To develop this project, you will need to have the following installed:

- Python 3.13 or higher
- `uv`

To install the project's dependencies, run the following command:

```
uv pip install -r requirements.txt
```

To run the project, run the following command:

```
python main.py
```

## How to Contribute

To contribute to this project, please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your changes.
3.  Make your changes and commit them.
4.  Push your changes to your fork.
5.  Create a pull request.
