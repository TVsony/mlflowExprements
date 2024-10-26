# Wine Quality Prediction with MLflow & DAGsHub
This project demonstrates a machine learning pipeline for predicting wine quality using an ElasticNet regression model. 
It leverages MLflow for experiment tracking and model versioning and integrates with DAGsHub for collaborative model and experiment tracking.

# 📑 Overview
This project aims to:
1) Train an ElasticNet regression model on the Wine Quality dataset.
2) Track experiment parameters and metrics using MLflow.
3) Log model versions and signatures for streamlined model management.
4) Use DAGsHub for centralized ML experiment tracking and collaboration.

# 🚀 Getting Started
Prerequisites
Ensure you have the following installed:

Python 3.7+
Virtual environment tool (e.g., venv or conda)

git clone https://dagshub.com/TVsony/mlflowExprements
cd mlflowExprements

# Install Dependencies
Set up your virtual environment and install the necessary libraries

# Create and activate the virtual environment
python -m venv 
source env/bin/activate # On Windows: env\Scripts\activate

# Install dependencies
pip install -r requirements.txt

## DAGsHub Integration
To enable DAGsHub integration, make sure to authenticate with DAGsHub and set up your repository details as shown in the code. 
This allows seamless tracking of all experiments and models.

# 🧑‍💻 Running the Experiment
python main.py [alpha] [l1_ratio]

alpha: Controls the regularization strength (default = 0.5).
l1_ratio: Specifies the ElasticNet mixing parameter (default = 0.5).

**Example**
python main.py 0.3 0.8

## Script Breakdown
1 Data Loading: Loads wine quality data from an online CSV file.
2 Data Splitting: Divides data into training and test sets (75/25 split).
3 Model Training: Trains an ElasticNet regression model.
4 Evaluation Metrics: Computes RMSE, MAE, and R2 scores for performance evaluation.
5 Logging to MLflow: Logs hyperparameters, metrics, and the trained model to MLflow.
6 DAGsHub Integration: Sets DAGsHub as the tracking URI for centralized tracking.

# 📊 Metrics & Model Tracking
Each experiment records:

1 Hyperparameters: alpha, l1_ratio
2 Evaluation Metrics: RMSE, MAE, R2 Score
Model versions are tracked, and each model's signature and parameters are logged, ensuring a streamlined pipeline for model versioning.

## 🔗 Tracking URI
This project uses a remote MLflow tracking server hosted on DAGsHub

Tracking URI: 
https://dagshub.com/TVsony/mlflowExprements.mlflow

# 📦 Model Registry
1 Models are registered with DAGsHub's MLflow instance, making it easy to view, manage, and deploy versions.
2 The model ElasticnetWineModel will appear under the MLflow dashboard on DAGsHub.

# 🧪 Evaluation Results
The following metrics are logged during model training:

- RMSE: Root Mean Squared Error – measures model error
- MAE: Mean Absolute Error – measures prediction accuracy
- R2: R-Squared – measures model fit

# ⚙️ Configuration
Configure MLflow’s tracking URI and DAGsHub credentials within the script

# For DAGsHub tracking
remote_server_uri="https://dagshub.com/TVsony/mlflowExprements.mlflow"
mlflow.set_tracking_uri(remote_server_uri)

# 📂 Project Structure

├── main.py                    # Main ML training script
├── README.md                  # Project documentation
├── requirements.txt           # Python dependencies

# 📘 References

- MLflow Documentation
- DAGsHub Documentation
- Krish Naik youtune channel 

