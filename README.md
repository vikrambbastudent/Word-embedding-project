# Word Embeddings with EDA
## In this repository, we delve into Exploratory Data Analysis (EDA) of GloVe word embeddings. This process involves uncovering the underlying structure and nuances within word embeddings through various analytical techniques. By understanding this structure, we aim to enhance our ability to leverage these embeddings effectively in machine learning models.

**The Dataset**

To get started, download the dataset at huggingface.co/stanfordnlp/glove/resolve/main/glove.6B.zip[1]. This contains three text files, each containing a list of words along with their vector representations. We will use the 300-dimensional representations (glove.6B.300d.txt).

**Overview**

- Word embeddings are dense vector representations of words in a continuous vector space, where semantic relationships between words are captured based on their contextual usage. GloVe (Global Vectors for Word Representation) is one such technique that learns word embeddings by factorizing the word co-occurrence matrix.

**Objectives**

-Apply EDA techniques to GloVe word embeddings to uncover their inherent structure.

- Explore techniques such as covariance matrices, clustering, PCA (Principal Component Analysis), and vector math to gain insights into the embeddings.

- Identify and understand any biases or surprising patterns embedded within the word embeddings.
  
**Requirements**

To replicate the analysis and experiments conducted in this repository, you will need:

- Basic understanding of linear algebra, statistics, and vector mathematics.
  
- Python packages: numpy, sklearn, and matplotlib.
  
- Approximately 3 GB of spare disk space to store and process the word embeddings data.
  
**Contents**

**Introduction to Word Embeddings**

- Explanation of word embeddings and their significance.
  
- Overview of GloVe word embeddings.

- Exploratory Data Analysis (EDA)

- **Covariance Matrices**: Analyzing the relationships between word vectors.
  
- **Clustering:** Grouping similar word vectors together.

- **PCA (Principal Component Analysis):** Reducing dimensionality while preserving semantic information.

- **Vector Math:** Performing arithmetic operations to explore semantic relationships.

**Insights and Discoveries**

- Uncovering hidden biases or unexpected patterns within the word embeddings.
  
- Discussing implications for downstream applications in natural language processing.

  **Conclusion:**
We applied a variety of exploratory data analysis (EDA) techniques to a 300-dimensional dataset of GloVe word embeddings. We used cosine similarity to measure the similarity between the meanings of words, clustering to group words into related groups, and principal component analysis (PCA) to identify the most significant directions in vector space for the embedding model.

During our analysis, we visually observed minimal covariance between the input features using PCA. Attempting to visualize the entire 300-dimensional data in just two dimensions with PCA provided some insights but was challenging due to the complexity of the dataset.

We also explored assumptions and biases within our dataset. By comparing the cosine similarity of "nurse" with "man" and "woman," we identified gender bias. Using vector math, we successfully represented analogies such as "king" is to "queen" as "man" is to "woman." Subtracting various vectors associated with males and females allowed us to pinpoint a gender-associated vector direction, revealing the "most masculine" and "most feminine" vectors in our dataset.
