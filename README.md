# Movie Reviews Data Sourcing and Analysis

*This project utilizes data sourced from online APIs to gather movie-related data from The New York Times and The Movie Database. The project involves extracting, cleaning, and merging this data into a unified format for further analysis, with final outputs saved as CSV files.*

**[Data](#data)** | **[Data Processing](#data-processing)** | **[Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)** | **[Core Skills, Technologies, Tools](#core-skills-technologies-tools)** | **[Continued Exploration](#continued-exploration)**

---

## Abstract

This project sources movie-related data from two APIs: The New York Times and The Movie Database (TMDb). After querying the respective APIs and extracting data, it performs data cleaning and transformation, merges data from the sources, and outputs the results to a CSV file for further analysis. Key steps include API integration, JSON data formatting, Pandas DataFrame manipulation and data merging.

## Data

*The data in this project is sourced from two APIs:*

* **The New York Times Article Search API** : Provides data on articles related to movie reviews. [NYT API documentation](https://developer.nytimes.com/docs/articlesearch-product/1/routes/articlesearch.json/get)
* **The Movie Database (TMDb) API** : Provides detailed movie data including titles, release dates, and reviews. [TMDb API documentation](https://developer.themoviedb.org/docs/search-and-query-for-details)

### Data Processing

*Cleaning, transforming, and preparing the raw data for analysis, focusing on merging data from multiple APIs and ensuring compatibility across datasets.*

* **API Access** : Query data from the NYT and TMDb APIs using Python requests.
* **Data Extraction** : API responses converted to JSON format for easy handling.
* **DataFrame Creation** : JSON data loaded into Pandas DataFrames.
* **Data Cleaning** : Handle missing or irrelevant data, and standardize formats.
* **Data Merging** : Combine movie-related data from two APIs into single DataFrame for analysis.
* **Complex Merging** : Merge two DataFrames with differing structures to unify the data for analysis.
* **Data Export** : Final cleaned, merged DataFrame exported to CSV format.

### Exploratory Data Analysis (EDA)

* **Data Validation** : Basic data accuracy and completeness verification after merging.

---

## Core Skills, Technologies, Tools

Python, Pandas, and the requests library to integrate data from two online APIs (NYT and TMDb). Performed data cleaning, formatting, and merging of JSON responses into Pandas DataFrames for analysis and export.

---

## Continued Exploration

Next phase of the project could include utilizing **Large Language Models (LLMs)** and **Transformers** to preform sentiment

Next phase of the project could utilize **Large Language Models (LLMs)** and **Transformers** from Hugging Face for sentiment analysis of movie review text and correlation with movie scores. Suggested NLP pipeline:

* **Text Preprocessing** : Use Hugging Face's **`transformers`** library for tokenization and vectorization.
* **Tokenization** : Break down text into tokens using pre-trained models like **BERTTokenizer** or  **RoBERTaTokenizer** .
* **Vectorization** : Generate dense embeddings with models like **BERT** or **DistilBERT** to capture semantic meaning.
* **Sentiment Analysis** : Apply pre-trained models via Hugging Face's **`sentiment-analysis`** pipeline, or fine-tune models like  **BERT** ,  **RoBERTa** , or **DistilBERT** for improved sentiment prediction.
* **Model Fine-tuning** : Fine-tune Transformer model to enhance accuracy and relevance.
* **Text Classification** : Classify reviews into sentiment categories (positive, neutral, negative) and analyze correlation with final movie scores.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
