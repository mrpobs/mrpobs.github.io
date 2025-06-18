Enron Email Analysis – Final Machine Learning Project
Overview
This project explores the Enron email dataset through three analytical lenses:

Burnout Prediction – Identifying potential signs of employee stress and overwork using email metadata and content.

Communication Clustering – Detecting implicit departmental structures and leadership roles using graph analysis and community detection.

Urgency Classification – Inferring the urgency level of emails using heuristics and semantic embeddings.

It is a proof of concept developed as part of a final Machine Learning project by:

Constanza Segrelles

Daniel Bravo

Pablo Benavides

Project Structure
The repository contains the following scripts and notebooks:

ml.py: Preprocessing and cleaning of the original Enron dataset. Extracts metadata, cleans message bodies, and prepares features.

ml_burnout.py: Detects temporal and relational patterns that may indicate employee burnout. Includes graph analysis and outlier detection.

ml_clusters.py: Builds a communication graph and applies community detection to cluster departments. Calculates leadership metrics and communication styles.

ml_urgency.py: Classifies emails into urgency levels (urgent, important, routine, disposable) using heuristics and DistilBERT embeddings.

Each file is a standalone analysis but they all share a common preprocessed dataset (correos_limpios.csv).

Dataset
The project uses the Enron Email Dataset, which consists of emails from around 150 employees, mostly senior staff, collected during the investigation of Enron's collapse.

⚠️ Disclaimer: Due to computational limits, only a subset of ~30,000 emails was used.

Setup
Use Google Colab for execution.

Mount Google Drive for data access.

Install required packages (if not already available):

python
Copiar
Editar
!pip install tqdm transformers networkx python-louvain seaborn
Instructions
1. Preprocess Emails (ml.py)
Extracts metadata (from, to, subject, date, body).

Cleans text for NLP.

Enriches data with time features and recipient count.

Outputs: correos_limpios.csv

2. Burnout Detection (ml_burnout.py)
Analyzes off-hours activity and communication gaps.

Constructs temporal plots and graphs.

Identifies employees at risk of burnout via behavior patterns.

3. Clustering Departments (ml_clusters.py)
Creates a communication network from email data.

Detects communities using modularity-based clustering.

Measures centrality (PageRank, Degree, Betweenness) per cluster.

4. Urgency Classification (ml_urgency.py)
Labels emails using heuristics and text indicators.

Extracts DistilBERT embeddings of email bodies.

Trains classifiers to distinguish urgency levels.

Key Insights
Temporal anomalies and off-hours activity can suggest burnout.

Clustering communication patterns can reveal implicit organizational structure.

Simple heuristics combined with semantic embeddings provide a strong baseline for urgency detection.

Limitations
Email content is only partially processed due to volume.

Burnout labels are heuristic, not ground-truth.

Classification models are basic due to limited computational resources.

Acknowledgments
CMU for the Enron dataset.

Hugging Face for transformer models.

Python libraries: pandas, networkx, seaborn, matplotlib, transformers.

