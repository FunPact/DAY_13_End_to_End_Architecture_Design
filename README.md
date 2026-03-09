This Repository contains the Visual & Conceptual Outputs developed for **Day-13 of the Databricks 14 Days AI Challenge – 2 (Advanced)**. The Objective of this Stage was to tep back from Implementation & Document how the different Components built during the Previous Days connect into a Single Production-Style Data & AI Pipeline.

Unlike earlier Stages of the Challenge, **Day-13 does not involve the Development of any New Code-Based Implementation**. Instead, it focuses on Architecture Design, System Documentation, and Lifecycle Planning.

The Materials in this Repository include:

- Architecture Diagram
- Two-Pages Carousel Explaining the System Design
- Documentation of Pipeline Flow & Retraining Strategy

These Outputs were derived from **Observations & Learnings from the Code Activities Completed between Day-0 & Day-12**.

## 1. Architecture Design

The Architecture Diagram represents a **Lakehouse-based Machine Learning Pipeline** built on the Databricks Platform. It illustrates how Raw E-Commerce Event Data moves through different Layers of the System.

The Flow begins with **Raw CSV Ingestion** into the **Bronze Layer**, where the Data is stored as Delta tables. From there, Feature Engineering Processes transform Event-Level Data into Aggregated user Features within the Silver Layer. These Curated Datasets are used to Prepare Training Datasets for Machine Learning Models.

Model Training & Evaluation are performed using Algorithms such as **Logistic Regression and Random Forest**, with Experiment Tracking handled through **MLflow**. The Trained Model is then used in a **Batch Inference Pipeline** to generate Predictions stored in the **Gold Layer**. A Collaborative Filtering Recommendation Component using **ALS** Complements the Prediction Pipeline by Generating Product Recommendations.

## 2. Pipeline Flow Documentation

The Pipeline flow explains how the different Components of the System Operate sequentially. The Workflow includes:
1. Data Ingestion & Delta Table Creation
2. Feature Engineering & Data Validation
3. Training Dataset Preparation
4. Model Training & Experiment Tracking
5. Batch Inference & Prediction Generation

Supporting Operational Layers such as **Job Orchestration, Streaming Ingestion Capability, Performance Monitoring, & Cost Optimization** are also considered to reflect how such a System would Operate in a Production Environment.

3. Retraining Strategy

The final part of Day-13 defines a model retraining strategy to ensure the machine learning system remains accurate as new data becomes available.

Retraining can be triggered through scheduled workflows or changes in data distribution. Updated datasets are generated from Delta tables, models are retrained and evaluated, and experiments are tracked using MLflow. The best-performing model is then redeployed to the inference pipeline.

Key Note

There is no new code implementation in Day-13. The architecture, pipeline documentation, and retraining strategy are based entirely on insights derived from the code activities performed from Day-0 through Day-12 of the challenge.

The goal of this stage is to translate individual experiments and implementations into a structured, production-oriented system design.
