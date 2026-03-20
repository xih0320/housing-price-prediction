# Probabilistic Graphical Models: Bayesian Network Analysis

## Overview
This project applies **Probabilistic Graphical Models (PGMs)** to two real-world datasets using Bayesian Networks and Markov Networks. The goal is to model variable dependencies, perform probabilistic inference, and extract meaningful insights from structured data.

---

## Part 1: Wine Quality — Bayesian Network

**Dataset:** Red Wine Quality (1,599 records, 12 physicochemical features)

**What I did:**
- Performed exploratory data analysis (EDA) and correlation analysis to understand feature relationships
- Constructed a Directed Acyclic Graph (DAG) based on domain knowledge and correlation structure
- Identified **Conditional Independence** relationships (e.g., A ⊥ K | H)
- Discretized continuous variables using `KBinsDiscretizer` and trained a Bayesian Network with `pgmpy`
- Performed **probabilistic inference** using Variable Elimination to query target variable distributions

**Tools:** Python, pandas, pgmpy, scikit-learn, NetworkX, seaborn

---

## Part 2: Depression Risk — Markov Network

**Dataset:** Student Depression Survey (27,901 records, features include Academic Pressure, Financial Stress, Work/Study Hours, CGPA)

**What I did:**
- Built an **Undirected Markov Network** modeling relationships between lifestyle factors and depression risk
- Defined conditional independence assumptions (e.g., Work/Study Hours ⊥ Age | Depression)
- Estimated joint probability factors from data using cross-tabulation
- Performed **Belief Propagation** and **Variable Elimination** inference to query depression probability given evidence
- Converted to **Junction Tree** for efficient exact inference

**Key Result:** Given average levels of Academic Pressure, Financial Stress, and Study Satisfaction, the model estimates a **65.97% probability of depression risk** — highlighting the compounding effect of multiple stressors.

**Tools:** Python, pandas, pgmpy, scikit-learn, NetworkX, matplotlib

---

## Skills Demonstrated
- Probabilistic graphical model construction (DAG, Markov Network, Junction Tree)
- Bayesian inference and Variable Elimination
- Data discretization and factor estimation
- Statistical analysis and data visualization
