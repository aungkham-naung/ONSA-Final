# Network Modeling of Socioeconomic Segregation Across Chicago’s Community Areas

This repository contains the data, code, and outputs for our CS 579 final project on socioeconomic segregation across nine Chicago Community Areas, modeled as a similarity network.

Team members:
- Aung Kham Naung
- Hamza Bu Obaid
- Myat Minn Thiha
- Souptik Sinha

## Project Overview

The goal of this project is to examine socioeconomic inequalities across Chicago’s Community Areas, focusing on the hierarchy between high income, middle income, and low income neighborhoods. We use census based variables to build a socioeconomic “persona” for each Community Area and then construct similarity networks where nodes are Community Areas and edges represent how similar they are along these dimensions.

We focus on nine Community Areas:

- **North Side (high income, highly resourced)**
    - Lincoln Park
    - Lake View
    - Near North Side

- **Northwest Side (middle income, mixed profiles)**
    - Jefferson Park
    - Portage Park
    - Irving Park

- **South and West Side (high poverty, disinvestment)**
    - Englewood
    - West Englewood
    - South Lawndale / Little Village

We use these nine areas to explore how opportunities, resources, and living conditions cluster and diverge, and how segregation appears when we treat Community Areas as nodes in a similarity network.

## Repository Structure

```text
.
├── data
│   ├── raw
│   │   ├── ONSA_Data/                  # Original per-CA ACS/ONSA CSVs
│   │   └── tract_to_CA_crosswalk.csv   # 2020 Census Tracts → Community Areas
│   ├── intermediate
│   │   └── agg_data.csv                # Combined tract/block-group level data
│   └── processed
│       ├── Computation_Complete/       # Canonical similarity and network outputs
│       │   ├── cosine_similarity.csv
│       │   ├── euclidean_distance.csv
│       │   ├── correlation_matrix.csv
│       │   ├── centrality_metrics.csv
│       │   ├── louvain_communities.csv
│       │   ├── kmeans_labels.csv
│       │   ├── assortativity_results.csv
│       │   ├── clustering_coefficients.csv
│       │   └── final_graph.gpickle
│       ├── CA_Aggregated_Data.csv
│       ├── CA_Normalized_Features.csv
│       ├── Centrality_Measures_All_Networks.csv
│       ├── Clustering_Coefficients_All_Networks.csv
│       ├── Centrality_Summary_Statistics.csv
│       ├── Clustering_Summary.csv
│       ├── Louvain_Communities_All_Networks.csv
│       ├── Network_Summary_Report.csv
│       └── Hierarchical_Clusters.csv
├── notebooks
│   ├── CS579_data_agg + calculations.ipynb   # Main aggregation + canonical similarity pipeline
│   ├── Souptik_Network_Analysis.ipynb        # Alternative network construction and metrics
│   └── analysis2.ipynb                       # Additional network summaries and plots
├── outputs
│   ├── graphs
│   │   ├── cosine_0.3.graphml
│   │   ├── cosine_0.5.graphml
│   │   ├── cosine_0.7.graphml
│   │   ├── correlation_0.5.graphml
│   │   ├── euclidean_0.6.graphml
│   │   ├── top_3.graphml
│   │   └── top_4.graphml
│   └── figures
│       ├── Network_Graphs_All_Versions.png
│       ├── Centrality_Visualization_cosine_0.5.png
│       ├── Louvain_Communities_cosine_0.5.png
│       ├── Clustering_Coefficients_Visualization.png
│       └── Hierarchical_Clustering_Dendrogram.png
└── README.md
# ONSA-Final
