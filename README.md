Finance Sentiment Analysis (updated nonbinary version)

This project demonstrates a finance sentiment analysis pipeline that scrapes Yahoo Finance news headlines, then uses a transformer-based AI model for sentiment analysis. The pipeline assigns discrete sentiment values: 1 for positive, 0 for neutral, and -1 for negative. The goal is to provide a data-driven tool for analyzing financial news sentiment across different industries.

Overview

This project performs the following steps:
	1.	Data Scraping:
Scrapes Yahoo Finance for news headlines of selected tickers across various industries using BeautifulSoup.
	2.	AI Sentiment Analysis:
Uses a Hugging Face transformer model (cardiffnlp/twitter-roberta-base-sentiment) to compute sentiment probabilities for each headline. Instead of relying solely on the top label, it calculates the difference between positive and negative probabilities and assigns a discrete sentiment based on a configurable threshold.
	3.	Aggregation and Display:
Aggregates the results into a pandas DataFrame, which includes ticker, industry, timestamp, headline, dominant sentiment label, and the computed sentiment value.

Features
	•	Scraping Yahoo Finance:
Custom scraping of Yahoo Finance pages to extract headlines for a list of predefined tickers.
	•	Transformer-Based Sentiment Analysis:
Uses a transformer model to capture nuanced sentiment beyond basic lexicon methods. The model returns all sentiment scores to allow for threshold-based decision making.
	•	Discrete Sentiment Mapping:
Maps the sentiment to three values:
	•	1: Positive
	•	0: Neutral
	•	-1: Negative
	•	Multi-Industry Support:
Supports multiple industry categories by associating each ticker with its respective industry (e.g., Technology, Healthcare, Energy).

Requirements
	•	Python 3.x
	•	Google Colab (or local Jupyter environment)
	•	Libraries:
	•	requests
	•	beautifulsoup4
	•	pandas
	•	datetime
	•	nltk
	•	transformers
	•	torch

Installation & Setup
	1.	Clone the Repository:

git clone https://github.com/yourusername/finance-sentiment-analysis.git
cd finance-sentiment-analysis


	2.	Install Required Libraries:
If running locally, create a virtual environment and install dependencies using pip:

pip install requests beautifulsoup4 nltk transformers torch pandas

If using Google Colab, simply run the cell with the pip install commands.

	3.	Download NLTK Lexicon (Optional):
The code optionally downloads the VADER lexicon. This is not required for the transformer-based AI sentiment analysis but can be used for comparisons.

import nltk
nltk.download('vader_lexicon')



Usage
	1.	Run the Notebook:
Open the provided notebook in Google Colab (or Jupyter Notebook) and run all cells sequentially. The notebook contains code that:
	•	Scrapes Yahoo Finance for a predefined list of tickers.
	•	Analyzes each headline using the transformer model.
	•	Displays the results in a pandas DataFrame.
	2.	Modify the Ticker List:
You can update the tickers_info dictionary to include additional tickers and assign them to appropriate industry categories.
	3.	Adjust Sentiment Threshold:
The threshold for mapping the difference between positive and negative sentiment scores can be adjusted in the compute_sentiment function to optimize performance for your data.

Code Structure
	•	Scraping Function:
scrape_yahoo_finance_news(ticker)
Scrapes Yahoo Finance pages for a given ticker and extracts news headlines.
	•	Sentiment Analysis Function:
analyze_headlines_with_ai(ticker, industry)
Processes each headline using the transformer pipeline and computes a discrete sentiment value.
	•	Main Loop:
Iterates over all tickers in the tickers_info dictionary, collects sentiment analysis results, and aggregates them into a DataFrame.

Contributing

Feel free to fork this repository and submit pull requests for improvements or bug fixes. If you have ideas to enhance the scraping mechanism, sentiment analysis precision, or overall pipeline, your contributions are welcome!

Disclaimer
	•	Data Usage:
Ensure you comply with Yahoo Finance’s terms of service when scraping data.
	•	Sentiment Accuracy:
The transformer model used provides a state-of-the-art approach to sentiment analysis, but no model is perfect. Results should be interpreted as indicative rather than definitive.

License

This project is licensed under the MIT License.

This README provides a comprehensive overview of the project, instructions on setup, and guidelines for usage. Adjust sections as needed for your specific project requirements.
