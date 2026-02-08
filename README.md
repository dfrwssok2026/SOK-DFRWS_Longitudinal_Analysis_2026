# Supplementary Data & Code for DFRWS SoK 2026

This repository provides the supplementary datasets, analysis notebooks, prompt templates, runner scripts, and visualization code used in our DFRWS SoK 2026 paper on large-scale analysis of digital forensics research using large language models (LLMs).

The materials support reproducibility of the taxonomy construction, LLM-assisted labeling, and result visualizations reported in the paper.

## Repository Structure

### data_visualization/
Supplementary CSV files used for figures.

### taxonomy.ipynb
Taxonomy construction, analysis, and plots.

### community_network_research_focus.ipynb
information extraction, community structure (school, authors_name, affiliation, published year, venues, anti-df vs df).

### tool_submission.ipynb
tool prompts, data visualization script.

### results_combined_prompts_new.csv
Combined LLM labeling results (community network and research focus).

### results_new_taxonomy_analysis.csv
LLM classification for 544 dfrws papers (taxonomy)

### tools_new_expanded.csv.xlsx
Expanded tool metadata.

### taxonomy_updated.pdf
Updated taxonomy diagram.

## Requirements

- Python 3.9+
- Jupyter Notebook (recommended)

## Install Dependencies

```bash
pip install openai python-dotenv pandas numpy matplotlib seaborn tqdm

OpenAI API Setup

Some notebooks rely on the OpenAI API.

Step 1: Create a .env file

OPENAI_API_KEY=your_api_key_here

Step 2: Load in Python

from dotenv import load_dotenv
from openai import OpenAI
import os

load_dotenv()
client = OpenAI(api_key=os.getenv("OPENAI_API_KEY"))


Note: Running LLM-based experiments may incur API usage costs.
