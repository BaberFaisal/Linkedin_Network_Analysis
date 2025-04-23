# LinkedIn Ego Network Analysis

This Jupyter Notebook (`NetWork_Analysis__Code.ipynb`) performs a complete analysis of an ego network created from mutual LinkedIn connections. The goal is to understand the structure, key individuals, and community patterns within the user's professional network.

---

##  Files Used

- **Connections.csv** – Downloaded from LinkedIn, includes first name, last name, position, company, and connection date of 1st-degree connections.
- **output.xlsx** – Created using Selenium-based simulation, contains mutual connections (edges) between the user's LinkedIn friends.

---

## Steps Performed

### 1. Data Preprocessing
- Standardized names and merged attributes.
- Created an undirected graph with nodes as people and edges as mutual connections.
- Added node attributes (Position, Company).

### 2. Network Summary
- Node and edge count
- Directed/undirected & weighted/unweighted check
- Degree distribution plot
- Average path length and clustering coefficient

### 3. Structural Analysis
- Centrality measures: Degree, Betweenness, Closeness, Eigenvector
- Degree assortativity and attribute mixing (Position, Company)
- Jaccard similarity (shared neighbors)
- K-core decomposition (core influencers)

### 4. Community Detection
- Louvain method (primary)
- Greedy Modularity, Label Propagation, and Girvan-Newman (alternative methods)
- Modularity scores and number of communities
- Network visualizations using node color by community

---

##Key Insights

- High clustering and short path lengths indicate **small-world properties**.
- A few nodes (e.g., Amal Mahmoud, PhD) are central across all metrics — acting as **core influencers**.
- The network is **disassortative by degree**, typical of real-world hub structures.
- Communities are meaningful and reflect real-life social or professional groups.

---

## Requirements

Install required packages:
```bash
pip install networkx matplotlib pandas seaborn python-louvain
