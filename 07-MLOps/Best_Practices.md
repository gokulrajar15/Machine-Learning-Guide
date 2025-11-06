# Best Practices for Machine Learning

This document outlines essential best practices for developing, deploying, and maintaining machine learning systems in production environments.

## Table of Contents
1. [Rolling Window Training Data with Random Sampling](#rolling-window-training-data-with-random-sampling)

---

## Rolling Window Training Data with Random Sampling

### Overview
Rolling window training with random sampling is a technique used to maintain model performance over time by continuously updating the training dataset with fresh data while maintaining diversity through random sampling.

### 📌 Final Practical Formula

```
training_data = last_3_months_data + 10% to 30% random samples of older important cases
```

### Key Concepts

#### Rolling Window Approach
- **Definition**: A method where the training dataset is updated by sliding a fixed-size window over time-ordered data
- **Purpose**: Ensures the model learns from the most recent patterns while discarding outdated information
- **Window Size**: Determines how much historical data to retain (e.g., last 6 months, 1 year)

#### Random Sampling Integration
- **Stratified Sampling**: Maintains class distribution proportions within each window
- **Temporal Sampling**: Randomly selects data points from different time periods within the window
- **Balanced Sampling**: Ensures fair representation of different data segments

### Use Cases

- **Financial Trading Models**: Adapting to market regime changes
- **Recommendation Systems**: Incorporating changing user preferences
- **Fraud Detection**: Updating to new fraud patterns and attack vectors
- **Demand Forecasting**: Adjusting to seasonal patterns and market trends
- **Dynamic Pricing**: Responding to competitive landscape changes
