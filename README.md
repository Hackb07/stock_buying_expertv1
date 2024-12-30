


# Stock Buying Expert

This project demonstrates a multi-agent AI system designed to perform financial analysis and web search tasks. The system is implemented using the `phi` library and leverages powerful AI models, including `Groq` and tools for financial data and web search.

## Features

- **Web Search Agent**: 
  - Searches the web for relevant information using DuckDuckGo.
  - Includes sources for all information retrieved.

- **Finance AI Agent**: 
  - Analyzes financial data, including stock prices, analyst recommendations, and fundamentals.
  - Presents data in a user-friendly table format.

- **Multi-Agent System**: 
  - Combines web search and financial analysis capabilities.
  - Allows seamless collaboration between agents to handle complex queries.

## Prerequisites

Ensure the following are installed and configured:

1. **Python 3.10 or higher**
2. **Dependencies**: Install the required Python libraries:
   ```bash
   pip install phi yfinance duckduckgo-search
   ```
3. **Groq API Key**: 
   - Obtain an API key for Groq.
   - Set the environment variable `GROQ_API_KEY`:
     ```bash
     export GROQ_API_KEY="your_api_key_here"  # For Linux/Mac
     set GROQ_API_KEY=your_api_key_here       # For Windows
     ```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Hackb07/stock_buying_expertv1.git
   cd stock_buying_expert
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python main.py
   ```

## Code Structure

- **`main.py`**:
  - Contains the implementation of the multi-agent system.
  - Demonstrates how to query agents for financial analysis and web searches.
  
- **Agents**:
  - **Web Search Agent**: 
    - Uses the DuckDuckGo tool for retrieving web information.
  - **Finance AI Agent**:
    - Leverages YFinance tools for stock data analysis.

## Example Usage

The following command demonstrates a query to the multi-agent system:

```python
multi_ai_agent.print_response("Summarize analyst recommendation and share the latest news for NVDA", stream=True)
```

- **Output**: 
  - Summarized analyst recommendations for NVDA.
  - Latest news, sourced from the web.

## Configuration

Customize the agents in `main.py`:

1. **Web Search Agent**:
   - Modify `instruction` to adjust the behavior.
   - Example:
     ```python
     instruction=["Always include sources", "Use concise language"]
     ```

2. **Finance AI Agent**:
   - Adjust tools or display preferences.
   - Example:
     ```python
     tools=[YFinanceTools(stock_price=True, analyst_recommendations=True)]
     ```

![Alt text](images/logo.png)



## Contributing

Contributions are welcome! Please submit issues or pull requests to improve functionality or documentation.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- [phi](https://phi.readthedocs.io/): For enabling agent-based AI systems.
- [YFinance](https://github.com/ranaroussi/yfinance): For financial data retrieval.
- [DuckDuckGo Search](https://pypi.org/project/duckduckgo-search/): For web search functionality.

