## Voice Gender Clustering: Unsupervised Learning for Gender Identification

![image](https://user-images.githubusercontent.com/96771321/188281821-76c88f8d-0cb4-4a8b-92b2-dcc5fb28ba13.png)

> View Notebook: https://github.com/Davidsonity/GenderByVoice/blob/main/notebook.ipynb

---

### Introduction
The objective of this project is to utilize unsupervised machine learning techniques to identify the gender of a voice based on its acoustic properties. The project focuses on clustering the voice samples into subsets with similar behaviors, allowing us to distinguish between male and female voices.

### Dataset
The dataset used in this project consists of 3,168 recorded voice samples collected from male and female speakers. Each voice sample is characterized by various acoustic properties, such as duration, mean frequency, standard deviation of frequency, spectral entropy, and more. The dataset provides valuable features that can be used to distinguish between male and female voices.

**Data Source:** [Voice Gender Dataset](https://www.kaggle.com/datasets/primaryobjects/voicegender)

### Repository Structure
The repository contains the following files:

- **Gender_Report.ipynb:** Jupyter Notebook file containing the project code, data wrangling, exploratory data analysis, and clustering operations.
- **Gender_Report.pdf:** PDF version of the project report, which provides a detailed explanation of the project steps, results, and insights.
- **LICENSE:** A file specifying the license terms and conditions for the project.
- **README.md:** This file, providing an overview, instructions, and details about the project.
- **notebook.ipynb:** An additional notebook file (not directly related to the gender clustering project).
- **voice.csv:** The dataset file containing the voice samples' acoustic properties.

### Preliminary Wrangling
Before diving into the clustering process, some preliminary data wrangling steps are performed. These steps include importing necessary libraries, loading the dataset, and performing exploratory data analysis. The exploratory analysis involves visualizing numerical columns, checking the distribution of features, and identifying any skewed distributions that require transformation.

### Clustering Operations
The main part of the project involves applying different clustering algorithms to the dataset. The following clustering algorithms are implemented:

1. **K-means Clustering:** The K-means algorithm is used to group the voice samples into clusters based on their acoustic properties. The number of clusters is set to 2, representing male and female clusters. The algorithm assigns labels to each voice sample based on its cluster membership.

2. **Agglomerative Clustering:** The Agglomerative Clustering algorithm is employed to group the voice samples into clusters using a hierarchical approach. The algorithm merges similar clusters iteratively until the desired number of clusters is achieved. The number of clusters is set to 2, representing male and female clusters.

3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise):** Although attempted, DBSCAN is found to be unsuitable for this problem since the number of clusters cannot be explicitly specified. Therefore, DBSCAN is not used for gender identification in this project.

### Results and Insights
The project provides several insights into the gender distribution within the voice clusters. The results obtained from K-means and Agglomerative Clustering are analyzed and visualized to gain a better understanding of the gender composition within each cluster. The following insights are derived:

- K-means Clustering:
  - Cluster 1: 61% female and 39% male
  - Cluster 2: 33% female and 67% male

- Agglomerative Clustering:
  - Cluster 1: 35% female and 65% male
  - Cluster 2: 61% female and 39% male

The project demonstrates that both K-means and Agglomerative Clustering techniques can effectively group the voice samples into clusters with distinguishable gender compositions. The choice between the two algorithms depends on the specific requirements and preferences of the application.

### Usage and Reproduction
To reproduce the results of this project, follow these steps:

1. Download the dataset (voice.csv) from the provided data source: [Voice Gender Dataset](https://www.kaggle.com/datasets/primaryobjects/voicegender).
2. Ensure the required libraries are installed, including pandas, numpy, matplotlib, seaborn, and scikit-learn.
3. Open the Jupyter Notebook file (Gender_Report.ipynb) in Jupyter Notebook or any compatible environment.
4. Execute the cells in the notebook sequentially to perform data wrangling, exploratory data analysis, and clustering operations.
5. Observe the visualization outputs and analysis provided in the notebook to gain insights into the gender clustering results.

Please note that proper Python environment setup and familiarity with Jupyter Notebook are required to run the project successfully.

### Contributors
This project was developed by Emuejevoke Eshemitan as part of Research Purpose. Contributions, suggestions, and improvements are welcome.

---
