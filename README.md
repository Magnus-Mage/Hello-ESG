# FinBert ESG Analysis from Web Articles

This project is designed to scrape web articles related to Environmental, Social, and Governance (ESG) topics and analyze them using the FinBert model. The web scraping is done using Selenium, and the ESG sentiment of each article is computed using the FinBert model.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Workflow](#project-workflow)
- [ESG Sentiment Analysis](#esg-sentiment-analysis)
- [Contributing](#contributing)
- [License](#license)

## Installation

To get started, clone the repository and install the required packages.

### Prerequisites

- Python 3.x
- `pip` (Python package installer)
- Chrome Browser installed on your system

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/finbert-esg.git
    cd finbert-esg
    ```

2. Install the required Python libraries:

    ```bash
    pip install -r requirements.txt
    ```

3. Ensure you have Chrome installed and the ChromeDriver is compatible with your version of Chrome.

4. (Optional) Set up a virtual environment:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use venv\Scripts\activate
    ```

## Usage

1. **Web Scraping**

    The project uses Selenium to scrape articles from the web. To start scraping articles:

    - Ensure your Chrome binary is set correctly in the code:

    ```python
    options.binary_location = "/path/to/your/chrome/binary"
    ```

    - Run the Jupyter notebook or Python script that performs the scraping.

2. **ESG Analysis**

    Once the articles are scraped, the FinBert model is used to calculate the ESG sentiment for each article. The sentiment scores for Environmental, Social, and Governance categories will be extracted.

## Project Workflow

1. **Scraping Articles**: Selenium automates a Chrome browser session to gather articles from selected websites. You can customize the scraping logic to target specific URLs.

2. **Data Processing**: The scraped content is cleaned and processed using `pandas` for further analysis.

3. **ESG Sentiment Analysis**: The processed articles are fed into the FinBert model, which outputs sentiment scores for each of the three ESG categories.

## ESG Sentiment Analysis

The ESG sentiment analysis is based on the FinBert model, a BERT-based model fine-tuned for financial sentiment analysis. The model takes in text data and outputs sentiment scores across Environmental, Social, and Governance dimensions.

Example output:
```json
{
    "Environmental": 0.72,
    "Social": -0.15,
    "Governance": 0.34
}
