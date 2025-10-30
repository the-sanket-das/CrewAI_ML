# 🤖 CrewAI – Autonomous Data Scientist Agent

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FFD43B?style=for-the-badge&logo=autodesk&logoColor=black)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-102230?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![AI Agents](https://img.shields.io/badge/Agentic%20AI-6C63FF?style=for-the-badge&logo=openai&logoColor=white)

---

## 🧩 Project Overview

This project demonstrates how to build an **autonomous AI crew** capable of performing the **end-to-end data science workflow** using [CrewAI](https://docs.crewai.com/introduction).

The AI system consists of **multiple specialized agents**—each responsible for data preprocessing, model training, and result evaluation.  
Together, they predict **revenues from supplement sales** using **machine learning regression models**.

> 🧠 Think of it as a digital data science team — each agent has its own goal, tools, and role, collaborating like departments in an organization.

---

## 🏗️ System Architecture

```mermaid
graph TD;
    A[Data Loader Agent] --> B[Preprocessing Agent];
    B --> C[Model Trainer Agent];
    C --> D[Evaluator Agent];
    D --> E[Report Generator Agent];
