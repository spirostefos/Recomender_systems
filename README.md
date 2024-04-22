## Introduction
In this project, we aim to develop and optimize two distinct recommender system models: one based on neighborhood methods and the other on matrix factorization. Our primary objective is to enhance recommendation quality by meticulously tuning hyperparameters. We rigorously evaluate the performance of these models against a baseline model to measure their effectiveness.

## Phase 1: Exploratory Data Analysis (EDA) and Dataset Preparation
We begin by loading essential modules and libraries, followed by an in-depth Exploratory Data Analysis (EDA) of the dataset 'MovieLens-Ratings.csv'. The EDA process involves extracting insights using charts and plots. To manage the dataset's size, we employ stratification sampling to extract a representative sample. This sample undergoes a similar EDA process, enabling a comparative analysis with the original data.

## Dataset
The dataset used in this project is the MovieLens dataset, which can be obtained from the [GroupLens website](https://grouplens.org/datasets/movielens/). Make sure to download the dataset and place it in the `Recomender_system/` directory before running the code.

## Dataset Overview
- **Number of Users:** 283,228
- **Number of Movies:** 53,889
- **Missing Values:** None

## Data Visualization
We visualize the distribution of movie ratings using bar plots and pie charts, providing insights into the prevalence of different rating categories.

## Stratification Sampling
StratifiedShuffleSplit is applied to perform stratified random sampling, ensuring fair representation of all subgroups within the dataset. The resulting sampled data allows for robust analysis and insights.

## Model Development and Evaluation
### Baseline Model: Normal Predictor
We construct a Normal Predictor model and conduct a 5-fold cross-validation to obtain performance scores.

### KNNWithZScore Model
We explore the K-nearest neighbors (KNN) approach with Z-score normalization, optimizing hyperparameters through grid search and cross-validation.

### SVD++ Model
We implement the SVD++ matrix factorization-based algorithm, tuning hyperparameters to improve recommendation accuracy.

## Conclusion
After evaluating the performance of the three models, we conclude that SVD++ outperforms the baseline and KNNWithZScore models, achieving the lowest RMSE. The success of hyperparameter tuning underscores its importance in optimizing recommendation systems.

## Requirements
- Python 3.x
- NumPy
- Pandas
- SciPy
- Scikit-learn

## Setup Instructions
1. Clone the repository to your local machine: `git clone https://github.com/your-username/recommender-system.git`
2. Navigate to the project directory: `cd recommender-system`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Run the main script to execute the project: `python main.py`
