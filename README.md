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

# Experimental Findings

The experiments conducted in this project focused on evaluating the feasibility of integrating deterministic nutritional constraints with semantic recipe retrieval and generative explanation models.

The experimental workflow involved three main stages.

## Dataset Integration and Processing

Multiple open-source datasets were integrated to support the recommendation pipeline, including recipe data, nutritional information, and contextual food waste datasets. Data preprocessing included cleaning ingredient names, standardizing nutritional values, and constructing structured representations of recipe metadata.

## Semantic Recipe Retrieval

Recipes were converted into vector embeddings using SentenceTransformer models. These embeddings were indexed using FAISS to enable efficient similarity search across a large recipe corpus.

The retrieval mechanism allows the system to identify recipes that are semantically related to available ingredients and user dietary preferences.

## Deterministic Recipe Ranking

Candidate recipes retrieved from the embedding search were evaluated using deterministic scoring rules. The scoring process considered:

- ingredient overlap with available fridge items
- calorie constraints derived from personalized metabolic calculations
- protein requirements for diet goals such as high-protein meals

This deterministic ranking stage ensures that recommended meals satisfy nutritional feasibility before being presented to the user.

## Generative Explanation Experiments

Separate experiments were conducted to explore the use of generative language models for producing explanations describing why a recommended meal satisfies nutritional and sustainability criteria.

Different models were evaluated in a controlled prompt-based setting to observe their ability to reason about structured nutritional inputs.

## Computational Constraints

Some experiments involving embedding generation and large language model inference required GPU resources. Due to runtime limitations and restricted computational units in the execution environment, certain experiments were interrupted or executed partially.

The notebooks included in this repository reflect the actual experimental workflow and development process carried out during the thesis work.

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

# Citation

If you use this work or repository in your research, please cite the following thesis:

```
Vikhyath Sthavarmath. (2026). 
AI-Driven Sustainable Nutrition: Leveraging Generative Models for Personalized Meal Planning and Food Waste Reduction.
Master's Thesis, SRH University of Applied Sciences Heidelberg.
```

You may also cite this repository:

```
@misc{Sthavarmath2026sustainablemealai,
  author = {Sthavarmath, Vikhyath},
  title = {AI-Driven Sustainable Nutrition: Leveraging Generative Models for Personalized Meal Planning and Food Waste Reduction},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/vikhyath905/Master-Thesis}
}
```

---

# License

This repository is shared for academic and research purposes.


# Author

Vikhyath Sthavarmath

Master's Thesis  

SRH University of Applied Sciences Heidelberg

SRH Campus Leipzig
