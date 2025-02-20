# Personal-Projects

Financial Sentiment Analysis:

This project performs sentiment analysis on financial market discussions and compares the results with market performance (e.g., SPY ETF price changes).

1. Collect financial news and comments using Scrapy.
2. Use GPT-3 (via OpenAI API) to classify sentiment (positive or negative).
3. Fine-tune sentiment analysis using Hugging Face and LangChain.
4. RAG: Enhance sentiment analysis with professional analysts' opinions.
5. Daily Market Sentiment: Generate daily market sentiment and compare with SPY price changes.
Uses the following:
Libraries: `Scrapy`, `yfinance`, `openai`, `huggingface_hub`, `langchain`, `requests`
Usage

1. Scrapy Web Scraping:
   Run the Scrapy spider:
   ```bash
   scrapy runspider finance_spider.py
   ```

2. Sentiment Classification: Use GPT-3 to classify sentiment in collected text.

3. Train Sentiment Model: Fine-tune the sentiment analysis model using Hugging Face.

4. Compare with SPY: Fetch SPY data using `yfinance` and compare sentiment with price change.

License

MIT License



