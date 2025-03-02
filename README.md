# CDP Chatbot

## Overview
CDP Chatbot is a data extraction and NLP-powered chatbot designed to scrape, process, and retrieve information from Customer Data Platform (CDP) documentation websites such as Segment, mParticle, and Lytics. The chatbot uses advanced web scraping techniques, parallel processing, and natural language processing (NLP) to provide relevant responses to user queries.

#Repository Link-https://github.com/mohammedifran13/cdp_chatbot

## Features
- **Scraping URLs from Sitemaps**: Extracts URLs from sitemaps of CDP documentation websites.
- **Multithreaded Web Scraping**: Fetches and processes URLs efficiently using concurrent threads.
- **Text Extraction**: Scrapes text content from URLs and stores the processed data in CSV format.
- **Natural Language Processing (NLP)**: Uses tokenization, BM25 ranking, and sentence embedding for efficient information retrieval.
- **Query Expansion with Synonyms**: Enhances search capabilities by expanding queries with synonyms.
- **Search & Ranking**: Uses BM25 and semantic similarity for ranking the most relevant documents.
- **AI-Powered Refinement**: Integrates with Gemini API to refine extracted answers and improve response quality.
- **External API Querying**: Fetches additional insights from external APIs for specific CDP queries.

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/CDP-Chatbot.git
   cd CDP-Chatbot
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the chatbot:
   ```bash
   python chatbot.py
   ```

## Dependencies
- Python 3.7+
- `requests`
- `beautifulsoup4`
- `pandas`
- `concurrent.futures`
- `nltk`
- `rank_bm25`
- `spacy`
- `sentence-transformers`

## Usage
### Scraping Data
Run the script to scrape data from sitemaps:
```python
python scrape_data.py
```
This will generate CSV files containing extracted URLs and text data.

### Querying the Chatbot
Example usage:
```python
from chatbot import answer_query
query = "How do I set up a new source in Segment?"
response = answer_query(query)
print(response)
```

## File Structure
```
CDP-Chatbot/
│── scrape_data.py  # Script for web scraping
│── chatbot.py  # Main chatbot script
│── requirements.txt  # Dependencies
│── data/  # Folder containing scraped data CSVs
│── README.md  # Project documentation
```

## API Keys
The chatbot uses Gemini API for response refinement. Add your API keys in `config.py`:
```python
GEMINI_API_KEYS = [
    "your-api-key-1",
    "your-api-key-2"
]
```

## Future Enhancements
- Expand support for more CDPs (e.g., Zeotap, Tealium)
- Improve query refinement with advanced NLP models
- Implement a web-based UI for better user interaction

## License
This project is licensed under the MIT License.

