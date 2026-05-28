# Abalone Clustering with K-Means and PCA

This project uses unsupervised machine learning to group abalones by their physical measurements and explore whether those groups relate to abalone age.

## Motivation / Context

Determining the age of an abalone usually requires cutting the shell, staining it, and counting rings under a microscope, which is time-consuming. This project asks whether easier-to-measure physical features, such as length, diameter, height, and weight, can reveal useful patterns about abalone size and age.

This type of analysis connects to real-world problems where people want to find natural groups in data without already knowing the correct labels. Similar methods are used in customer segmentation, recommendation systems, and biological data exploration.

## What I Did

I used the Abalone dataset from the UCI Machine Learning Repository. The dataset contains 4,177 abalones with physical measurements such as sex, length, diameter, height, whole weight, shucked weight, viscera weight, shell weight, and rings. The Rings column is related to age because adding 1.5 to the number of rings gives the estimated age in years.

In the notebook, I:

1. Loaded and explored the Abalone dataset.
2. Looked at relationships between physical measurements and Rings.
3. Standardized the numeric features so that larger-scale measurements would not dominate the clustering.
4. Applied K-Means clustering to group abalones based on their measurements.
5. Used PCA to reduce the data to two dimensions so the clusters could be visualized.
6. Compared the clusters with the known Rings values to see whether the groupings matched abalone age.

## How to Run the Code

### Requirements

Install the main Python libraries used in this project:

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

### Run the Notebook

1. Clone this repository:

```bash
git clone https://github.com/alfreidben/data-science-projects.git
cd data-science-projects
```

2. Open Jupyter Notebook:

```bash
jupyter notebook
```

3. Open and run:

```text
Project_Unsupervised_Learning_Abalone_Dataset.ipynb
```

Run the cells from top to bottom to reproduce the analysis, clustering, PCA plot, and conclusions.

## Key Results

The K-Means clusters showed some meaningful structure, especially by separating smaller abalones from larger abalones. However, the clusters did not perfectly match the true age groups based on Rings.

The PCA visualization showed a large amount of overlap between the groups. This means that while physical measurements alone can give some information about age, they do not accurately separate abalones into age-based clusters.

## Skills Demonstrated

- Python programming
- Data cleaning and exploration
- Pandas and NumPy
- Data visualization with Matplotlib
- Feature scaling with StandardScaler
- K-Means clustering
- Principal Component Analysis, or PCA
- Unsupervised machine learning
- Interpreting model results for a real-world dataset

## Data Source

Dataset: Abalone Dataset — UCI Machine Learning Repository
https://archive.ics.uci.edu/dataset/1/abalone

## License

This repository is licensed under the MIT License.
