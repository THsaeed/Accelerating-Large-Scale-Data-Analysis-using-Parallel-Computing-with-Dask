# Accelerating-Large-Scale-Data-Analysis-using-Parallel-Computing-with-Dask
## Project Overview
This project investigates how parallel computing with Dask can accelerate large-scale data analysis tasks. It focuses on evaluating the performance, scalability, and feasibility of Dask as a distributed computing framework for modern data-intensive applications.

The project demonstrates how Dask extends common Python data science tools such as pandas, NumPy, and scikit-learn to operate efficiently in parallel and distributed environments.

---

## Problem Statement
Traditional single-machine data analysis approaches face significant limitations in terms of memory capacity, storage, and processing speed when dealing with large and complex datasets. As data volumes continue to grow across scientific, industrial, and commercial domains, there is a need for scalable frameworks that can process such data efficiently.

This project examines whether Dask can improve computation efficiency and support scalable data analytics compared to conventional single-machine methods.

---

## Dataset Description
The project uses the Adult dataset (Census Income dataset), a widely used benchmark dataset for classification tasks.

- Total instances: 48,842
- Training subset: 32,561
- Testing subset: 16,281
- Features: 14
- Label: Binary classification (<=50K or >50K annual income)

The dataset includes demographic and socioeconomic features such as age, workclass, education, occupation, marital status, and hours per week.

---

## Methodology
The methodology is based on comparing traditional machine learning with distributed machine learning using Dask.

### Traditional Approach
- Logistic Regression using scikit-learn

### Distributed Approach
- Logistic Regression using Dask-ML

### Dask-Based Workflow
- Dataset partitioning across workers
- Parallel task scheduling
- Distributed model training
- Aggregation of results through the scheduler

---

## System Design
The conceptual architecture of the project follows a distributed training workflow:
- The client submits the task
- The scheduler coordinates execution
- Workers process local data partitions in parallel
- Results are aggregated centrally

This design allows efficient task distribution and better scalability for large-scale analysis.

---

## Data Analysis
The project includes exploratory analysis of the Adult dataset, including:
- Age distribution histogram
- Heatmap showing correlations among numerical features

These visualizations help in understanding the structure of the data before model training.

---

## Evaluation Metrics
The implemented models were evaluated mainly using:
- Accuracy
- Training time

---

## Key Results
The experimental results showed that:

- The scikit-learn Logistic Regression model achieved an accuracy of approximately 80.77%
- The Dask-ML Logistic Regression model achieved an accuracy of approximately 81.70%

In another comparison:
- scikit-learn achieved 78.7%
- Dask-ML achieved 80.8%

Although Dask slightly improved accuracy, the distributed approach required more computation time due to task scheduling overhead in the experimental environment.

---

## Discussion
The findings show that Dask offers important advantages for scalable analytics:
- Parallel and distributed execution
- Better handling of large datasets
- Familiar integration with Python tools
- Flexible scheduling and resource management

However, the results also show that performance gains depend on the environment. In single-node settings such as Google Colab, the overhead of distributed scheduling may reduce the expected speed benefits.

---

## Tools and Technologies
- Python
- Dask
- Dask-ML
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Google Colab




---

## Project Status
This repository documents the methodology, system design, implementation, and experimental findings of the project. Future work may explore GPU clusters, hybrid cloud environments, and more complex machine learning workloads.

---

## Authors
- Thuraya Saeed Alshahrani
