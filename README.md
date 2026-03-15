# AI-Driven Sustainable Nutrition: Leveraging Generative Models for Personalized Meal Planning and Food Waste Reduction

This repository contains the implementation and experimental notebooks developed for the Master's thesis titled:

**AI-Driven Sustainable Nutrition: Leveraging Generative Models for Personalized Meal Planning and Food Waste Reduction**

The project investigates how artificial intelligence techniques can support sustainable food consumption and personalized nutrition by integrating generative models with deterministic decision logic.

The system aims to recommend meals that satisfy nutritional requirements while prioritizing ingredients that are close to expiration, thereby contributing to food waste reduction.

---

# Research Motivation

Modern food systems face two critical challenges:

- the growing demand for **personalized nutrition**
- increasing levels of **household food waste**

While many nutrition applications focus on monitoring dietary intake, they rarely provide intelligent meal recommendations based on available ingredients. At the same time, recipe recommendation systems typically ignore nutritional constraints and sustainability considerations.

This research explores how AI-driven systems can generate meal recommendations that balance:

- nutritional adequacy
- ingredient availability
- sustainability through reduced food waste

---

# System Overview

The proposed system integrates several components within a structured recommendation pipeline:

1. **Dataset integration**  
   Multiple datasets containing nutritional information and recipe metadata are processed and merged.

2. **Ingredient prioritization**  
   Refrigerator ingredients are evaluated based on their expiration dates to prioritize items that should be consumed sooner.

3. **Personalized nutrition modeling**  
   User metabolic requirements are estimated using metabolic equations such as BMR and TDEE.

4. **Semantic recipe retrieval**  
   Recipe descriptions are converted into embeddings and searched using similarity-based retrieval.

5. **Deterministic ranking**  
   Candidate recipes are ranked using rule-based scoring functions that enforce nutritional constraints and ingredient usage.

6. **Generative reasoning experiments**  
   Generative models are evaluated for producing explanations that describe why selected recipes satisfy nutritional and sustainability requirements.

---

# Technologies Used

The implementation was developed using Python and integrates several AI and data processing tools:

- Python
- Pandas
- NumPy
- SentenceTransformers
- FAISS (Facebook AI Similarity Search)
- Natural Language Processing methods
- Generative AI models for reasoning experiments

---

# Datasets Used

The experiments rely on several open-source datasets:

### OpenFoodFacts Dataset
Provides nutritional information such as calories, protein, carbohydrates, and fat values for food products.

### Food.com Recipes Dataset
A large collection of recipes including ingredients and instructions used as the primary knowledge base for meal retrieval.

### Global Food Wastage Dataset
Used for contextual understanding of sustainability and food waste patterns.

### Synthetic Fridge Inventory Dataset
Simulated refrigerator inventory containing ingredients and expiration dates used for experimentation.

### Synthetic User Profile Dataset
Generated user profiles used to calculate personalized metabolic targets.

---

# Repository Structure

```
notebooks/
│
├── on_going.ipynb
├── thesis.ipynb
├── reasoning.ipynb
│
thesis/
│
└── final_thesis_report.pdf
│
proposal/
│
└── thesis_proposal.pdf
```

---

# Notebooks

### on_going.ipynb

This notebook contains early development experiments conducted during the initial stages of the research.  
It includes exploratory work related to dataset preprocessing, ingredient matching strategies, and early implementations of ranking mechanisms.

### thesis.ipynb

This notebook contains the main implementation of the meal recommendation system described in the thesis.  
The pipeline implemented here includes dataset integration, ingredient prioritization, metabolic modeling, semantic recipe retrieval, and deterministic ranking.

### reasoning.ipynb

This notebook contains experiments exploring the use of generative models to produce explanations describing why recommended meals satisfy nutritional requirements and sustainability objectives.

---

# Experimental Notes

The notebooks reflect the actual development process conducted during the thesis research.

Some experiments involved computationally intensive tasks such as embedding generation and large language model inference. Due to runtime limits and computational resource constraints in the execution environments, certain cells may contain interrupted runs or incomplete outputs.

These notebooks are preserved in their original state to accurately represent the research workflow.

---
# How to Reproduce the Experiments

The experiments were conducted using Jupyter notebooks and Python-based data processing tools.

To reproduce the workflow:

1. Clone the repository:

```
git clone https://github.com/your-username/your-repository-name.git
```

2. Install the required Python libraries:

```
pip install pandas numpy sentence-transformers faiss-cpu scikit-learn
```

3. Open the notebooks using Jupyter:

```
jupyter notebook
```

4. Run the notebooks in the following order:

- `on_going.ipynb`
- `thesis.ipynb`
- `reasoning.ipynb`

These notebooks contain the development pipeline, system implementation, and generative reasoning experiments described in the thesis.

---

# Important Notes

Some experiments involve embedding generation and generative model inference.  
These tasks may require GPU-enabled environments and sufficient runtime availability.

During the thesis development process, certain experiments were executed using limited computational resources. As a result:

- some notebook cells may contain interrupted runs
- certain outputs may not be fully reproduced without sufficient compute resources

The notebooks are included in their original state to reflect the authentic research workflow conducted during the project.


# Author

Vikhyath Sthavarmath

Master's Thesis  

SRH University of Applied Science, Heidelberg

SRH Campus Leipzig
