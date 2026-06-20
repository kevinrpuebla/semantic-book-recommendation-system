# Semantic Book Recommendation System

An NLP-powered recommendation engine that uses semantic vector search, transformer-based text classification, and metadata analysis to discover books based on natural language descriptions rather than exact keyword matching.

## Overview

Traditional recommendation systems often rely on predefined categories, ratings, or keyword matching. This project explores a more intelligent approach by leveraging modern Natural Language Processing (NLP) techniques and vector embeddings to recommend books based on the meaning of a user's query.

Using a dataset containing over 7,000 books and their metadata, the system performs:

* Exploratory Data Analysis (EDA)
* Data cleaning and feature engineering
* Zero-shot text classification
* Semantic vector search
* Natural language book retrieval

Users can enter prompts such as:

> "A book about fire and ice"

and receive books whose descriptions are semantically similar to the query.

---

## Features

### Data Exploration & Cleaning

* Downloaded and processed book metadata using KaggleHub
* Identified and visualized missing values
* Created engineered features such as:

  * Book age
  * Missing description indicators
  * Description length
* Removed incomplete records
* Generated a cleaned dataset for downstream NLP tasks

### Metadata Analysis

* Correlation analysis using Spearman correlation coefficients
* Feature relationship visualization with heatmaps
* Category frequency analysis

### Text Classification

* Applied transformer-based zero-shot classification
* Categorized books into Fiction and Nonfiction groups
* Evaluated classification performance across hundreds of book descriptions

### Semantic Search Engine

* Generated vector embeddings from book descriptions
* Stored embeddings using ChromaDB
* Performed semantic similarity search with LangChain
* Retrieved recommendations based on contextual meaning rather than keyword overlap

---

## Technologies Used

### Programming

* Python

### Data Science

* Pandas
* NumPy
* Matplotlib
* Seaborn

### NLP & Machine Learning

* Hugging Face Transformers
* BART Large MNLI
* OpenAI Embeddings

### Vector Search

* LangChain
* ChromaDB

### Data Acquisition

* KaggleHub

---

## Dataset

Dataset:

**7K Books with Metadata**

Source:
https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata

The dataset includes:

* Title
* Author
* ISBN
* Categories
* Description
* Number of Pages
* Publication Year
* Ratings

---

## Project Structure

```text
Semantic-Book-Recommendation-System/
│
├── data-exploration.ipynb
├── text-classification.ipynb
├── vector-search.ipynb
├── books_cleaned.csv
├── tagged_description.txt
├── README.md
└── requirements.txt
```

---

## Workflow

### 1. Data Exploration

* Load metadata
* Identify missing values
* Generate heatmaps
* Analyze feature relationships

### 2. Data Cleaning

* Remove incomplete entries
* Generate engineered features
* Export cleaned dataset

### 3. Text Classification

* Process book descriptions
* Apply zero-shot classification
* Compare predicted and actual categories

### 4. Semantic Search

* Convert descriptions into embeddings
* Store embeddings in a vector database
* Perform similarity-based retrieval
* Return the most relevant books

---

## Example Query

```python
retrieve_semantic_recommendations(
    "A book about fire and ice"
)
```

Example Output:

| Title              | Author      | Category  |
| ------------------ | ----------- | --------- |
| Recommended Book 1 | Author Name | Fiction   |
| Recommended Book 2 | Author Name | Fantasy   |
| Recommended Book 3 | Author Name | Adventure |

---

## Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Data Visualization
* Natural Language Processing
* Transformer Models
* Vector Databases
* Semantic Search
* Information Retrieval
* Machine Learning Workflows
* Python Development

---

## Future Improvements

* Web-based recommendation interface
* Hybrid recommendation system combining metadata and embeddings
* Fine-tuned classification models
* User preference profiles
* Recommendation ranking optimization
* Integration with larger language models

---

## Author

Kevin Puebla

Computer Science & Applied Mathematics Student
University of New Mexico
