## ArticleSearch Class

## Overview
The `ArticleSearch` class provides functionality to search for articles based on a given query using TF-IDF similarity scoring and retrieval of relevant documents. It preprocesses the data, calculates similarity scores, and retrieves the best-matching articles.

## Initialization
```python
def __init__(self, model_name, query, first_chunker_size=5000, second_chunker_size=1000, device='cuda', stop_words='english',alfa = 0.5):
```
-model_name: Name of the model used for embeddings.
-query: Query string for article search.
-first_chunker_size: Size of the first chunker (default: 2000).
-second_chunker_size: Size of the second chunker (default: 400).
-device: Device to run the model on (default: 'cuda').
-stop_words: Language-specific stop words (default: 'english').
-alfa: percentage of taken articles from the accuracy of the most suitable article and taking them for further selection(default: 0.5).
-
## Example Usage
model_name = "BAAI/bge-small-en-v1.5"
query = "humans evolution " #query to search
file_path = "/medium.csv"
article_search = ArticleSearch(model_name, query)
article_content = article_search.search_articles(file_path)
print(article_content)

## Dependencies
-pandas
-numpy
-scikit-learn
-transformers
-vectorhub
-langchain
installation !pip install -U chromadb langchain  rank_bm25 sentence_transformers
