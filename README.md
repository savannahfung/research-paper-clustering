# Research Paper Clustering

## Objective

Cluster a given set of research papers based on their abstract similarity using natural language processing, text preprocessing, and unsupervised machine learning.

## Requirements

- Python 3.11.5
- Libraries:
  - pandas
  - PyPDF2
  - scikit-learn
  - nltk
  - matplotlib

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/research-paper-clustering.git
   cd research-paper-clustering
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Notebook

1. Open the Jupyter Notebook:

   ```bash
   jupyter notebook research_paper_clustering.ipynb
   ```

2. Put the PDF files in the PDF directory or update `pdf_dir` variable with the directory containing all your PDF files.

3. Run all cells in the notebook.

## Output

- `clustering_results.csv`: File indicating which papers belong to each cluster.
- Summary report printed in the console with the number of clusters and the number of papers in each cluster, and the key terms or topics associated with each cluster.

## Approach

1. **Data Preprocessing**: Extract and preprocess the abstract content from PDFs.

- Extract text from PDF files using PyPDF2.
- Preprocess the extracted text by removing stop words, lemmatizing words, and handling special characters or formatting issues.
- Visualize the distribution of abstract lengths.

2. **Text Vectorization**: Convert text data into numerical representation using TF-IDF and apply LDA.

- Vectorize text using TF-IDF.
- Apply Latent Dirichlet Allocation (LDA) to extract topics.
- Standardize the topic distribution for clustering.

4. **Clustering**: Use K-means clustering to group similar papers.

- Determine the optimal number of clusters using the elbow method and silhouette analysis.
- Evaluate clustering performance using Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index.

5. **Visualization**: Visualize clustering results.

- Use PCA for dimensionality reduction.
- Scatter plot the clusters with research paper titles or IDs for context.

6. **Output Generation**: Save clustering results and generate a summary report.

- Save the results to clustering_results.csv.
- Print a summary report with the number of clusters and the number of papers in each cluster, and the key terms or topics associated with each cluster.
