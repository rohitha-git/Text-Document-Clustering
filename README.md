Text Document Clustering using TF-IDF and SBERT Embeddings
Table of Contents

Abstract

Introduction

Problem Statement

Objectives

Dataset Description

Methodology

Data Preprocessing

Feature Extraction (TF-IDF & SBERT Embeddings)

K-Means Clustering

Evaluation Metrics (Silhouette Score & Inertia)

Dimensionality Reduction (UMAP)

Cluster Visualization

Cluster Labeling Algorithm

Semantic Search Integration (Optional)

Technologies Used

System Architecture

Results & Discussion

Conclusion

Future Scope

References

Abstract

This project focuses on clustering text documents based on their semantic similarity using Natural Language Processing (NLP) techniques. The BBC News dataset is used as the primary corpus containing articles from categories such as business, sport, tech, politics, and entertainment.
Two feature extraction methods are implemented: TF-IDF vectorization for traditional statistical representation and SBERT (Sentence-BERT) for semantic embeddings. K-Means clustering is applied to identify hidden groupings within the documents. UMAP is used to visualize high-dimensional embeddings in 2D.
The results show that SBERT significantly improves cluster separation and topic coherence compared to TF-IDF. The project demonstrates how modern embedding models can enhance text clustering and information retrieval.

Introduction

Text data is growing rapidly across news portals, social media, and digital platforms. Organizing large volumes of unstructured text manually is inefficient. Clustering helps group similar documents automatically, making information retrieval faster and more meaningful.
This project explores the use of TF-IDF and SBERT embeddings to cluster BBC news articles and visualize their relationships using machine learning techniques.

Problem Statement

Traditional document clustering methods rely only on word frequency and fail to capture semantic meaning.
There is a need for a system that can cluster documents based on the context and meaning rather than just keywords.

Objectives

Clean and preprocess text documents.

Convert documents into numerical vectors using TF-IDF and SBERT.

Perform K-Means clustering to group similar documents.

Evaluate cluster quality using Silhouette Score and Inertia.

Reduce dimensionality using UMAP for visualization.

Automatically label clusters using top keywords.

(Optional) Implement semantic search for retrieving similar documents.

Dataset Description

Dataset: BBC Text Dataset

Total Documents: 2,225

Fields:

Text: News article content

Category (Ground Truth): business, sport, tech, politics, entertainment
This dataset is widely used for text classification and clustering research.

Methodology
1. Data Preprocessing

Convert text to lowercase

Remove punctuation, numbers, stopwords

Tokenization

Lemmatization

Remove duplicates and missing values

2. Feature Extraction
TF-IDF

Converts text into a sparse matrix

Captures importance of each word

Useful for baseline clustering

SBERT Embeddings

Uses sentence-transformers

Produces dense 384-dimensional semantic vectors

Captures meaning and context of text

3. K-Means Clustering

Applied separately on TF-IDF and SBERT vectors

Optimal cluster count found using silhouette score comparisons

SBERT gives much better separation

4. Evaluation Metrics

Silhouette Score → Measures cluster separation

Inertia → Measures compactness of clusters

5. Dimensionality Reduction (UMAP)

Reduces high-dimensional embeddings into 2D

Helps visualize document similarity

6. Cluster Visualization

Plot clusters using UMAP

Color-coded cluster points

Shows how well documents form groups

7. Cluster Labeling Algorithm

Extract top TF-IDF keywords for each cluster

Automatically assign topic names

Helps interpret cluster themes

8. Semantic Search (Optional)

Encode user query → Compare with document embeddings

Returns most semantically similar documents

Much better than keyword search

Technologies Used

Python

NLTK

spaCy

Scikit-learn

Sentence-BERT (SBERT)

Pandas, NumPy

UMAP

Matplotlib / Seaborn

Google Colab

System Architecture
BBC Text Dataset
       ↓
Preprocessing
       ↓
Embeddings (TF-IDF / SBERT)
       ↓
K-Means Clustering
       ↓
Evaluation (Silhouette Score, Inertia)
       ↓
UMAP Visualization
       ↓
Cluster Labeling
       ↓
(Optional) Semantic Search

Results & Discussion

SBERT embeddings produced higher silhouette scores than TF-IDF.

UMAP plots show better cluster separation for SBERT.

Automatically generated keywords successfully describe cluster themes.

Final clustering closely matches original BBC categories, proving accuracy.

Conclusion

The project shows that semantic embeddings (SBERT) outperform traditional TF-IDF for text clustering.
Using SBERT + K-Means + UMAP creates a powerful workflow for understanding document relationships and grouping articles meaningfully.

Future Scope

Add sentiment analysis

Deploy as a web application

Implement hierarchical clustering

Integrate topic modeling (LDA / BERTopic)

Build dashboard using Streamlit

References

BBC Dataset

Sentence Transformers Documentation

Scikit-learn

UMAP Official Docs
