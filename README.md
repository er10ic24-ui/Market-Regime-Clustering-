# Market-Regime-Clustering-
Identifying market regimes in daily stock returns using PCA and K-means clustering, with interpretable visualizations of regime dynamics over time.
## Overview 

This mini project applies unsupervised learning techniques to identify market regimes in daily stock return data.
Using Principal Component Analysis (PCA) for dimensionality reduction and K-means clustering on the reduced features, we group dates with similar return patterns and analyze how market behavior evolves over time.

The project emphasizes interpretability, combining clustering results with multiple visualizations to understand regime dynamics.

## Data Description
	•	Observations: Daily dates
	•	Features: Stock return data transformed into 10 principal components
	•	Returns are treated as already standardized; extreme outliers are clipped for visualization purposes.

## Methodology

### 1. Principal Component Analysis (PCA)
	•	PCA is applied to reduce dimensionality and capture dominant market factors.
	•	The first 10 principal components are retained.
	•	Explained variance is examined to confirm that leading components capture most of the variability.

Visualization:

	- Explained variance ratio for each principal component

### 2. Choosing the Number of Clusters
	•	The Elbow method is used to select the number of clusters.
	•	Based on the elbow point in within-cluster sum of squares, 7 clusters are chosen.

Visualization:

	- Elbow plot of inertia vs. number of clusters

### 3. K-Means Clustering
	•	K-means clustering is applied to the PCA-reduced data.
	•	Dates are grouped into 7 market regimes based on similarity in return structure.

Visualization:

	- 2D scatter plot using the first two principal components, colored by cluster assignment

## Results & Visual Analysis

### 1. Timeline of Market Regimes
	•	Each date is labeled by its cluster assignment.
	•	This visualization shows how market regimes evolve and transition over time.

Insight:

	- No single regime dominates the entire period.
	- Some clusters persist as baseline regimes, while others appear intermittently, indicating transient market conditions.

### 2. Cluster Mean Return Profiles
	•	For each cluster, the average return across the 10 principal components is computed.
	•	This reveals the characteristic structure of each market regime.

Insight:

	- Regime differences are primarily driven by the first few principal components.
	- Higher-order components contribute minimally to cluster separation.

### 3. Heatmap of Cluster Centers
	•	A heatmap visualization of cluster centroids across all principal components.
	•	Provides a compact comparison of regime structure.

Insight:

	- Confirms that regime separation is dominated by leading components.
	- Highlights similarities and contrasts among identified regimes.
	
## Key Findings
	•	Market regimes can be effectively identified by clustering dates in PCA-reduced return space.
	•	The first few principal components dominate regime behavior.
	•	The market exhibits regime persistence with regular transitions over time.
	•	PCA + K-means offers a simple yet interpretable framework for market regime analysis.
 
