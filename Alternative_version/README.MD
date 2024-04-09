## Data Analizer 
This Python script analyzes textual data using techniques such as TF-IDF vectorization, cosine similarity, and BM25 retrieval.

## Initialization
```python
def __init__(self,chunk_size=200, stop_words='english', alfa=0.5)
```
-chunk_size: Size of the chunker (default: 200).
-stop_words: Language-specific stop words (default: 'english').
-alfa: percentage of taken articles from the accuracy of the most suitable article and taking them for further selection(default: 0.5).

## Example Usage
analyzer = DataAnalyzer()
query = "humans evolution" 
data = pd.read_csv("/medium.csv")  
analyzer.analyze_data(query, data)

## Dependencies
-numpy
-scikit-learn
-langchain (installable via pip install langchain)
-pandas

installation !pip install -U chromadb langchain  rank_bm25 sentence_transformers
