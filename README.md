# WGAN-GP for Synthetic Network Traffic Generation (IoT-23)
WGAN-GP model for generating synthetic IoT-23 network traffic to improve IDS performance and solve class imbalance in cybersecurity datasets.

This project implements a Wasserstein Generative Adversarial Network with Gradient Penalty (WGAN-GP) to generate high-quality synthetic network traffic using the IoT-23 dataset.

The goal is to address data scarcity and class imbalance in cybersecurity datasets, improving the performance of Intrusion Detection Systems (IDS).

Synthetic data is evaluated using statistical tests and its impact on classification performance using a Random Forest model.

- Implementation of WGAN-GP for stable synthetic data generation
- Handles class imbalance in IoT-23 dataset
- Feature engineering and preprocessing pipeline
- Statistical validation:
  - Kolmogorov-Smirnov (KS) Test
  - Wasserstein Distance
  - Correlation Analysis
- Performance evaluation using Random Forest classifier
- GUI dashboard for automated evaluation and visualization

- Python
- PyTorch
- Scikit-learn
- Pandas & NumPy
- Matplotlib / Seaborn
- XGBoost (feature importance)
- Streamlit UI dashboard

- Dataset: IoT-23 (Stratosphere Lab)
- Contains both benign and malicious IoT network traffic
- Includes attack types such as:
  - DDoS
  - C&C
  - Okiru Botnet
  - Port Scanning


 1. Data Preprocessing
   - One-hot encoding
   - Feature engineering (IAT, connection rate, unique ports)
   - Feature selection using correlation + XGBoost
   - MinMax scaling

2. Model Development
   - WGAN-GP architecture (Generator & Critic)
   - Gradient penalty for training stability

3. Synthetic Data Generation
   - Class-wise data generation
   - Inverse transformations applied

4. Evaluation
   - Statistical fidelity tests (KS Test, Wasserstein Distance)
   - Model performance using Random Forest
  


- Synthetic data closely matched real data distributions
- Improved detection of minority classes:
  - Okiru Recall: 0.23 → 0.83
- Macro Recall improved from 0.84 → 0.93
- Demonstrated effectiveness of GAN-based data augmentation for IDS


(Add screenshots here if possible)
- Correlation Matrix (Real vs Synthetic)
- Confusion Matrix
- Performance Comparison Charts


A dashboard was developed to:
- Upload datasets and models
- Automate evaluation process
- Visualize classification performance

This reduces manual effort and improves analysis efficiency.
