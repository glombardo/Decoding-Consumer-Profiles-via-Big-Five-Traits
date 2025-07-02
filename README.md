Project: Decoding Consumer Profiles via Big Five Personality Traits

Summary: A data‑science project that maps Big Five personality traits onto consumer survey data to uncover distinct, actionable audience segments.We combine psychometric scoring, dimensionality reduction (PCA), and unsupervised clustering techniques to translate hundreds of attitudinal variables into a handful of marketing‑ready personas.

Key goals: 1) Score each respondent on the Big Five (OCEAN) traits from raw questionnaire responses. 2) Visualise latent structure with PCA and t‑SNE to spot well‑separated groups. 3) Segment the population using Ward‑linkage hierarchical clustering and K‑Means (optimal k determined with Silhouette & Elbow metrics via Yellowbrick). 4) Profile clusters along demographics, media behaviour, and purchasing intent to surface strategic insights for brand, media, and product teams.

Repository layout:

.
├── data/                # raw & processed data (git‑ignored)
│   ├── raw/             # original survey extracts
│   └── processed/       # tidy, scored & ready‑to‑model
├── notebooks/
│   ├── Decoding_Consumer_Profiles_via_Big_Five_Traits.ipynb
│   └── PCA_Follow_Up_Decoding_Consumer_Profiles_via_Big_Five_Traits.ipynb
├── reports/             # exported html / pdf reports & slide decks
├── environment.yml      # reproducible conda environment
└── README.md

Quick‑start (Colab): 1) Click the “Open in Colab” badge at the top of this file. 2) In the Colab runtime, upload the required CSV/Parquet files to /content/data/raw/ (or mount Google Drive). 3) Run the cells top‑to‑bottom – they install dependencies, clean data, and output interactive visuals.

Local setup:

git clone https://github.com/<your‑repo>/consumer‑profiles‑big‑five.git
cd consumer‑profiles‑big‑five

# create reproducible environment
conda env create -f environment.yml
conda activate bigfive

jupyter lab
# open the notebook of interest

Core Python stack

Package

Purpose

pandas, numpy

data wrangling & numerics

scikit‑learn

PCA, clustering, pipeline utilities

scipy

hierarchical linkage metrics

yellowbrick

cluster diagnostic & silhouette plots

matplotlib, seaborn

static & styled charts

Notebook guide

Notebook

Highlights

What you learn

Decoding_Consumer_Profiles_via_Big_Five_Traits

• Big Five scoring pipeline• Ward dendrograms & optimal‑k search• Cluster interpretation (radar & strip plots)

Baseline segmentation and rich persona descriptions

PCA_Follow_Up_Decoding_Consumer_Profiles_via_Big_Five_Traits

• PCA on 50‑item inventory• Scree & loading plots• Re‑cluster in PCs, stability checks

Validates dimensional structure and ensures segments are robust
