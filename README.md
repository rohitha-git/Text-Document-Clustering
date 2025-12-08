# Semantic Text Document Clustering  
### Using TF-IDF, SBERT Embeddings and K-Means

This project demonstrates how to cluster text documents based on semantic similarity rather than simple keyword frequency. It compares traditional NLP techniques (TF-IDF) with transformer-based deep learning models (SBERT) to show the difference in clustering quality and meaning-based similarity.

---

## Project Overview

Massive amounts of text are generated daily, making manual organization difficult. Traditional keyword-based methods like TF-IDF fail when two documents use different words but convey the same meaning.

Example:

- "India’s economy is slowing down"  
- "The financial growth rate of the country has reduced"

TF-IDF treats them as unrelated.  
SBERT recognizes they are semantically similar.

This project implements the following:

- TF-IDF Vectorization  
- Sentence-BERT (all-MiniLM-L6-v2) embeddings  
- K-Means clustering  
- UMAP dimensionality reduction for visualization  
- Automatic cluster labeling  
- Semantic search engine  
- Comparison of TF-IDF vs SBERT clustering

---

## Features

- Text preprocessing (stopwords, lemmatization, cleaning)  
- Clustering using TF-IDF  
- Clustering using SBERT semantic embeddings  
- Optimal K selection using Silhouette Score  
- UMAP-based 2D visualization  
- Automatic cluster keyword labeling  
- Semantic search using SBERT  
- Evaluation between traditional and semantic approaches

---

## Dataset

BBC News Dataset  
- Total documents: 2225  
- Categories: Business, Sports, Politics, Tech, Entertainment  

Contains:  
- text (article content)  
- category (used only for evaluation)

---


