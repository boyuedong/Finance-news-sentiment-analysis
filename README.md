Automated Finance News Sentiment Analysis with FinBERT (updated nonbinary version)

This project automates the collection and sentiment analysis of financial news headlines from Yahoo Finance using AI. The script runs daily at a scheduled time, scrapes the latest headlines, and classifies them into Positive, Neutral, or Negative sentiment using FinBERT, a financial sentiment analysis model. The results are saved into a CSV file, enabling users to track sentiment trends over time.

How It Works
	1.	Scrapes financial news from Yahoo Finance.
	2.	Processes headlines using FinBERT to determine sentiment.
	3.	Saves the data into a CSV file (daily_finance_news_sentiment.csv).
	4.	Runs automatically every day at 8:00 AM 

Installation & Setup

Step 1: Install Dependencies

Run the following command to install required Python libraries:

pip install schedule transformers pandas requests beautifulsoup4

Step 2: Run the Script

Execute the script in a Python environment (Jupyter Notebook, Google Colab, or Terminal):

python finance_news_sentiment.py

The script will run continuously, fetching and analyzing news daily.


Data Output

The script generates a CSV file (daily_finance_news_sentiment.csv) with the following columns:

Timestamp	Title	Sentiment
2024-06-15 08:00:00	Fed hikes interest rates again	Negative
2024-06-15 08:00:01	Tech stocks rally as AI optimism grows	Positive
2024-06-15 08:00:02	Oil prices remain stable amid global concerns	Neutral


License

This project is open-source and available under the MIT License.


Built by Boyue – AI Enthusiast 🚀
