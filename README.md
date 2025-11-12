# 🚀 Predictive Analytics Using Machine Learning — Powered by CrewAI

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-6B4DE6?style=for-the-badge&logo=chainlink&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6F00?style=for-the-badge&logo=xgboost&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)

---

## 🤖 Automating the Complete Machine Learning Workflow with AI Agents

This project demonstrates how **Predictive Analytics** can be supercharged using **AI Agentic automation**.  
It applies **machine learning regression** techniques to predict **supplement sales** while automating the full ML pipeline using **CrewAI**.

---

## 📘 Project Overview

In traditional data science projects, analysts manually perform:
- Data loading & cleaning  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Model training & evaluation  

Here, we take it further — building a **team of autonomous AI agents** using **CrewAI** that collaborate to perform these steps automatically.

### 🧩 Automated Steps
- Exploratory Data Analysis (EDA)
- Data Visualization
- Data Cleaning & Missing Value Handling
- Feature Engineering
- Model Training using:
  - Multiple Linear Regression
  - XGBoost
  - Random Forest
- Model Evaluation using metrics such as MAE, MSE, RMSE, and MAPE

---

## 🧠 What is CrewAI?

**CrewAI** is an open-source Python framework that enables the creation and management of **multi-agent AI systems**.  
It lets developers orchestrate multiple AI agents (powered by LLMs) that collaborate on multi-step workflows.

Each agent has:
- **Role:** Defines their job title (e.g., Data Analyst, Python Coder)
- **Goal:** Main objective of the agent
- **Backstory:** Helps the LLM understand its persona and domain
- **LLM:** The underlying language model used for reasoning
- **Tools (optional):** Capabilities like executing code, reading files, or calling APIs
- **Delegation:** Some agents can delegate sub-tasks to others

📘 Official Docs: [CrewAI Documentation](https://docs.crewai.com/introduction)

---

## 🧩 Project Architecture

### 🧍 Agents
Each agent has a specific purpose:
- **Data Analyst Agent** → Performs EDA, summary statistics, and visualizations  
- **Data Engineer Agent** → Handles missing values, encodes categorical data, preprocesses  
- **Model Builder Agent** → Trains regression models (MLR, XGBoost, Random Forest)  
- **Evaluator Agent** → Compares model performance metrics  
- **Python Coder Agent** → Generates and executes code via the Notebook Executor

### 🧰 Tools
Agents use these tools to interact with their environment:
- **Notebook Executor Tool** (for code execution)
- **File read/write** operations
- **Library installation** (via `pip`)
- **Error & output capturing**

### ⚙️ Tasks
Each agent is assigned a specific **Task** defined by:
- **description** → What the agent must do  
- **expected_output** → What defines task success  
- **agent** → Which agent will perform it  
- **context** → Outputs from previous tasks (for sequential workflows)

### 👥 Crew
The **Crew** binds everything together — agents, tasks, and execution process.  
For this project, we use **sequential processing**, where each task runs one after the other, passing outputs as context.

---

## 🔁 Workflow Summary

1. **Plan:** The CrewAI system identifies and sequences ML steps.  
2. **Execute:** Agents autonomously perform cleaning, EDA, and modeling.  
3. **Collaborate:** Outputs are shared among agents.  
4. **Evaluate:** Model results and metrics are compiled for insights.

---

## ⚡ Notebook Executor Tool

The **Notebook Executor Tool** allows CrewAI agents to dynamically execute Python code.

**Features:**
- Accepts Python code as a string.
- Installs required Python libraries automatically.
- Executes using Python’s `exec()` function in the notebook’s global scope.
- Captures and returns printed output and errors.
- Shares global variables (like `shared_df`) between executions.

**Purpose:** Enables fully autonomous experimentation — agents can generate, execute, and debug code themselves.

---

## 📊 Machine Learning Models Used

| Model | Description | Library |
|--------|--------------|----------|
| **Multiple Linear Regression** | Predicts a continuous target using multiple features. | scikit-learn |
| **XGBoost** | Gradient boosting technique for improved prediction accuracy. | xgboost |
| **Random Forest** | Ensemble of decision trees to reduce variance and overfitting. | scikit-learn |

### 🧮 Evaluation Metrics
- **MAE (Mean Absolute Error)**  
- **MSE (Mean Squared Error)**  
- **RMSE (Root Mean Squared Error)**  
- **MAPE (Mean Absolute Percentage Error)**  

---

## 🧾 Dataset

**File Used:** `Supplement_Sales_Weekly.csv`

| Column | Description |
|---------|--------------|
| Date | Week of sale |
| Product Name | Supplement name |
| Category | Product category |
| Price | Product price |
| Discount | Discount applied |
| Location | Store/region |
| Units Sold | Target variable (Regression Output) |

---

## 🧱 Project Structure

