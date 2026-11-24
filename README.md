# DSC212 Research Assignment: Modularity on the Karate Club Graph

Recursive spectral modularity partitioning implemented from scratch (NumPy + NetworkX) on Zachary's Karate Club network.

## Contents
- `karate_modularity.ipynb`: the full notebook (code, outputs, visualisations, discussion)
- `requirements.txt`: Python dependencies

## How to run
```
pip install -r requirements.txt
jupyter notebook karate_modularity.ipynb   # then Kernel > Restart & Run All
```

## What it does
1. Builds the adjacency matrix A, degree vector k and modularity matrix B = A - kk^T/2m
2. Splits by the sign of the leading eigenvector of B (verified against `networkx.community.modularity`)
3. Recursively splits each community until its leading eigenvalue is not positive
4. Plots the graph after each split with a fixed layout
5. Tracks degree, betweenness, closeness and clustering across iterations (computed within each node's community)

## Reference
Newman, M. E. J. (2006). Modularity and community structure in networks. PNAS 103(23), 8577-8582.
