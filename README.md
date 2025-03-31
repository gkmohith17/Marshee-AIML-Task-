# Marshee: Pet Activity Classification

## Project Overview
Marshee is a machine learning system that classifies pet activities based on accelerometer data from a wearable device. It can detect whether a pet is walking, running, resting, or playing, providing insights into your pet's daily activity patterns.

## 📊 Key Features
* **Activity Classification**: Accurately identifies four distinct pet activities (walking, running, resting, playing)
* **Real-time Processing**: Processes accelerometer data with overlapping windows for continuous monitoring
* **Optimized for Deployment**: Includes a lightweight model version for on-device implementation
* **Comprehensive Pipeline**: Covers the full ML workflow from data preprocessing to deployment

## 🧠 Technical Approach

### Data Processing Pipeline

1. **Data Generation & Preprocessing**
   * Synthetic accelerometer data simulation
   * Outlier detection and removal using Z-scores
   * Low-pass filtering to remove high-frequency noise

2. **Feature Engineering**
   * Sliding window approach with 50% overlap
   * Extraction of time-domain features (mean, std, min, max, etc.)
   * Cross-axis correlations and magnitude-based features

3. **Model Training**
   * Random Forest classifier with hyperparameter tuning
   * Feature selection to improve efficiency
   * Cross-validation to ensure robustness

4. **Deployment Optimization**
   * Reduced feature set (top 10 most important)
   * Lighter model with fewer estimators and controlled depth
   * Real-time inference simulation
