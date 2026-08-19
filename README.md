
<div align="center">

<!-- Top Animated Teal Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=008080&height=120&section=header&text=Davi%20AI%20-%20Data%20Assistant&fontSize=32&fontColor=ffffff&animation=twinkling" width="100%" />

[![Python](https://img.shields.io/badge/Python-3.9%2B-008080?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28%2B-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Website](https://img.shields.io/badge/Portfolio-kerstonanto.in-008080?style=for-the-badge&logo=google-chrome&logoColor=white)](https://kerstonanto.in)

> **A minimal build by Kerston Anto Singh**  
> *Offline data visualization foundation assistant. Transform natural language queries into instant EDA summaries, statistical metrics, and interactive visualizations.*

</div>

---

## Overview

**Davi AI** is an offline, lightweight data visualization assistant engineered for fast exploratory data analysis (EDA). Built on top of TF-IDF vectorization and cosine similarity matching, Davi AI maps natural language inputs directly to dynamic pandas operations and Seaborn visual outputs without sending data to external APIs.

* **Dynamic Knowledge Base Generation**: Automatically builds a custom TF-IDF search index based on your uploaded CSV column structure.
* **Instant Conversational Analytics**: Query dataset shapes, missing value ratios, unique counts, and schema types in plain English.
* **Automated Data Visualizations**: Generates histograms, scatter plots, line charts, box plots, violin plots, KDEs, heatmaps, and pairplots on demand.
* **In-Memory Data Cleaning**: Drop null rows or null columns interactively directly through conversational commands.

---

## Architecture & Workflow


```

[ CSV File Ingestion ] ──> ( Pandas Dataframe Loading )
│
▼
[ Dynamic KB Generation ] ─> ( Column-Mapped TF-IDF Vector Space )
│
▼
[ Query Matching Engine ] ─> ( Cosine Similarity Scoring vs. Intent Patterns )
│
▼
[ Processing Layer ] ────> ( Pandas Aggregation / Seaborn Chart Render )
│
▼
[ UI Presentation ] ─────> ( Custom Dark-Themed Streamlit Interface )

```

---

## Tech Stack & Dependencies

* **Core Language**: Python 3.9+
* **User Interface**: Streamlit
* **Data Processing**: Pandas, NumPy
* **NLP & Vectorization**: Scikit-Learn (`TfidfVectorizer`, `cosine_similarity`), Re
* **Data Visualization**: Seaborn, Matplotlib

---

## Quickstart & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/kerston2104/Davi_AI.git
cd Davi_AI

```

### 2. Set Up Virtual Environment

```bash
# Linux/macOS
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate

```

### 3. Install Dependencies

```bash
pip install -r requirements.txt

```

### 4. Run Application

```bash
streamlit run app.py

```

Open your browser at `http://localhost:8501`.

---

## Operating Modes

1. **Dataset Inspection**: Ask for `describe`, `shape`, `data types`, or `missing values` to inspect high-level statistics.
2. **Single Feature Analysis**: Ask for `histogram of Column`, `value counts of Column`, or `boxplot of Column`.
3. **Bivariate & Multivariate Relationships**: Request `scatter Column1 vs Column2`, `line chart Column1 vs Column2`, or `heatmap`.
4. **Data Cleaning**: Execute commands like `drop missing rows` or `drop missing columns` to update the active session state.

---

## Technical Details

* **Local TF-IDF Vector Engine**: Bypasses heavy LLM runtime overhead by utilizing unigram and bigram TF-IDF vectors matched via cosine similarity (threshold set at $0.15$).
* **Data Privacy**: Operations run strictly within local memory boundaries, ensuring no proprietary dataset records leave the offline runtime environment.

---

## Author & Contact

**Kerston Anto Singh**

* Minimal AI/ML Tools & Web Development
* Data visualization AI foundation model. For custom implementations or new model development, contact me directly.

🌐 **Website**: [kerstonanto.in](https://kerstonanto.in)

GitHub: [@kerston2104](https://www.google.com/search?q=https://github.com/kerston2104)

---
