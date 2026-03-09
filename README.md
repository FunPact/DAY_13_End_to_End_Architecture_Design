This Repository contains the Visual & Conceptual Outputs developed for Day-13 of the Databricks 14 Days AI Challenge – 2 (Advanced). The Objective of this Stage was to tep back from Implementation & Document how the different Components built during the Previous Days connect into a Single Production-Style Data & AI Pipeline.

Unlike earlier stages of the challenge, Day-13 does not involve the development of any new code-based implementation. Instead, it focuses on architecture design, system documentation, and lifecycle planning.

The materials in this repository include:

Architecture Diagram

Single-page Carousel explaining the system design

Documentation of pipeline flow and retraining strategy

These outputs were derived from observations and learnings from the code activities completed between Day-0 and Day-12.

1. Architecture Design

The architecture diagram represents a lakehouse-based machine learning pipeline built on the Databricks platform. It illustrates how raw e-commerce event data moves through different layers of the system.

The flow begins with raw CSV ingestion into the Bronze Layer, where the data is stored as Delta tables. From there, feature engineering processes transform event-level data into aggregated user features within the Silver Layer. These curated datasets are used to prepare training datasets for machine learning models.

Model training and evaluation are performed using algorithms such as Logistic Regression and Random Forest, with experiment tracking handled through MLflow. The trained model is then used in a batch inference pipeline to generate predictions stored in the Gold Layer. A collaborative filtering recommendation component using ALS complements the prediction pipeline by generating product recommendations.

2. Pipeline Flow Documentation

The pipeline flow explains how the different components of the system operate sequentially. The workflow includes:

Data ingestion and Delta table creation

Feature engineering and data validation

Training dataset preparation

Model training and experiment tracking

Batch inference and prediction generation

Supporting operational layers such as job orchestration, streaming ingestion capability, performance monitoring, and cost optimization are also considered to reflect how such a system would operate in a production environment.

3. Retraining Strategy

The final part of Day-13 defines a model retraining strategy to ensure the machine learning system remains accurate as new data becomes available.

Retraining can be triggered through scheduled workflows or changes in data distribution. Updated datasets are generated from Delta tables, models are retrained and evaluated, and experiments are tracked using MLflow. The best-performing model is then redeployed to the inference pipeline.

Key Note

There is no new code implementation in Day-13. The architecture, pipeline documentation, and retraining strategy are based entirely on insights derived from the code activities performed from Day-0 through Day-12 of the challenge.

The goal of this stage is to translate individual experiments and implementations into a structured, production-oriented system design.
