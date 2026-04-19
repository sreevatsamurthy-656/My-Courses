# ML Workflow on Google Cloud (Vertex AI)

## Overview
- ML model development can be done using:
  - Pre-trained APIs (ready-to-use)
  - AutoML (low/no-code)
  - Custom training (DIY/code-based)

- This module covers:
  - ML workflow stages
  - MLOps (deployment & automation)
  - Vertex AI Pipelines
  - Hands-on AutoML implementation
  - Optional: Neural network learning concepts

---

## ML Workflow (3 Main Stages)

### 1. Data Preparation
- Steps:
  - Data Uploading
  - Feature Engineering

- Key Points:
  - Large amount of data required
  - Data quality + quantity → affects model performance

- Types of Data:
  - **Structured Data**: Tables (numbers, text)
  - **Unstructured Data**: Images, videos
  - **Streaming Data**: Real-time
  - **Batch Data**: Stored datasets

---

### 2. Model Development
- Involves:
  - Training
  - Evaluation

- Process:
  - Iterative cycle:
    - Train → Evaluate → Improve → Repeat

---

### 3. Model Serving
- Steps:
  - Deploy model
  - Monitor performance

- Key Insight:
  - A model has no value unless it is used in production

---

## Restaurant Analogy 
- **Data Preparation** → Preparing ingredients
- **Model Development** → Experimenting with recipes
- **Model Serving** → Serving dishes to customers

---

## Iterative Nature of ML
- ML workflow is **not linear**
- Feedback loops exist:
  - Training → may require better features
  - Deployment → may reveal:
    - Data drift
    - Accuracy drop
- Requires revisiting earlier stages

---

## MLOps (Machine Learning Operations)
- Automates ML lifecycle:
  - Data → Training → Deployment → Monitoring
- Handles:
  - Continuous improvement
  - Production reliability

---

## Workflow Options in Vertex AI

### 1. AutoML (No-Code)
- UI-based model building
- Beginner-friendly
- No ML or coding expertise required

---

### 2. Code-Based Approach
- Tools:
  - Vertex AI Workbench
  - Google Colab
  - Vertex AI Pipelines

- Vertex AI Pipelines:
  - Uses SDKs (Software Development Kits)
  - Helps automate end-to-end ML workflows

- Best for:
  - ML Engineers
  - Data Scientists
  - Automation-focused development

---

## Key Takeaways
- ML workflow has 3 stages:
  1. Data Preparation
  2. Model Development
  3. Model Serving
- Workflow is iterative, not linear
- MLOps enables automation and scalability
- Two approaches:
  - AutoML (easy, no-code)
  - Pipelines (flexible, code-based)

# Data Preparation in ML Workflow (Vertex AI)

## Overview
- First stage of ML workflow
- Steps involved:
  1. Data Uploading
  2. Feature Engineering

---

## Data Uploading
- Data sources:
  - Cloud Storage
  - BigQuery
  - Local machine

- AutoML primarily supports **tabular data**

---

## Problem Types (Objectives)
For tabular data, AutoML supports:
- **Regression** → Predict continuous values
- **Classification** → Predict categories/classes
- **Forecasting** → Predict future trends (time series)

- Example:
  - Forecasting is widely used in industries like retail

---

## Feature Engineering

### What is a Feature?
- A **feature** is:
  - A factor contributing to prediction
  - Similar to:
    - Independent variable (statistics)
    - Column in a dataset

---

### Why Feature Engineering?
- Raw data needs preprocessing before training
- Improves model performance

---

### Analogy
- Data = Ingredients (carrots, onions, tomatoes)
- Feature Engineering = Preparing ingredients:
  - Peeling
  - Chopping
  - Cleaning

---

### Challenges
- Time-consuming
- Complex to design useful features

---

## Vertex AI Feature Store

### What is it?
- A **centralized repository** for:
  - Managing features
  - Serving features
  - Sharing features

---

### Key Capabilities
- Aggregates features from **BigQuery**
- Supports:
  - **Online serving** → Real-time
  - **Offline serving** → Batch processing
- Low-latency feature delivery
- Supports **Generative AI**:
  - Manages embeddings
  - Enables real-time similarity search

---

## Feature Store Workflow (Online Serving)

1. Prepare data source in BigQuery  
2. (Optional) Register data:
   - Create feature groups
   - Define features  
3. Create **Feature View**:
   - Select features for online serving  
4. Serve latest feature values in real-time  

---

## Benefits of Vertex AI Feature Store

### 1. Shareable
- Centralized feature management
- Consistency across teams

### 2. Reusable
- Avoid duplicate work
- Saves time

### 3. Scalable
- Handles large-scale serving
- Provides low-latency access

### 4. Easy to Use
- User-friendly interface
- Simplifies feature management

---

## Key Takeaways
- Data preparation is the foundation of ML
- Feature engineering directly impacts model performance
- Vertex AI Feature Store:
  - Simplifies feature handling
  - Enables scalable and reusable ML workflows

# Model Development in ML Workflow (Vertex AI)

## Overview
- Second stage of ML workflow
- Steps involved:
  1. Model Training
  2. Model Evaluation
- Process is **iterative** (train → evaluate → improve → repeat)

---

## Analogy
- Model Training → Cooking the recipe
- Model Evaluation → Tasting the food

---

## Model Training

### Key Configurations

#### 1. Training Method
- Specify dataset from data preparation stage
- Define:
  - Data type:
    - Tabular
    - Image
    - Text
    - Video
  - Training objective (problem to solve)

- Choose method:
  - **AutoML** (no-code)
  - **Custom Training** (code-based)

---

#### 2. Training Details
- For supervised learning:
  - Select **target column** (label)

- Training options:
  - Select features to include
  - Transform data types if required

---

#### 3. Budget and Execution
- Define:
  - Training budget
  - Pricing constraints

- Start training:
  - AutoML automatically:
    - Trains multiple models
    - Selects best-performing model

---

### Technologies Behind AutoML
- Neural Architecture Search
- Transfer Learning

---

## Model Evaluation

### Purpose
- Measure model performance
- Ensure model meets expectations

---

## Confusion Matrix

### Definition
- A table comparing:
  - Predicted values
  - Actual values

### Components (Binary Classification)

- **True Positive (TP)**  
  Model predicts positive and it is correct  

- **True Negative (TN)**  
  Model predicts negative and it is correct  

- **False Positive (FP)** (Type I Error)  
  Model predicts positive but it is incorrect  

- **False Negative (FN)** (Type II Error)  
  Model predicts negative but it is incorrect  

---

## Evaluation Metrics

### Recall
- Measures how many actual positive cases were correctly predicted

:contentReference[oaicite:0]{index=0}

---

### Precision
- Measures how many predicted positive cases are actually positive

:contentReference[oaicite:1]{index=1}

---

### Precision vs Recall Trade-off
- Improving one may reduce the other
- Depends on use case:

- **High Recall Priority**
  - Capture as many positives as possible
  - Example: Spam detection (catch all spam)

- **High Precision Priority**
  - Ensure predicted positives are correct
  - Example: Avoid marking valid emails as spam

---

### Precision-Recall Curve
- Visual tool in Vertex AI
- Helps adjust balance between precision and recall

---

## Feature Importance

### Definition
- Measures contribution of each feature to predictions

### Representation
- Displayed as a bar chart:
  - Larger value → higher importance

### Use Case
- Helps:
  - Select relevant features
  - Improve model performance

---

## Explainable AI

### What is it?
- Tools and frameworks to:
  - Interpret model predictions
  - Understand decision-making

### Example
- Feature importance is a part of Explainable AI

---

## Key Takeaways
- Model development includes training and evaluation
- Training requires selecting:
  - Data
  - Objective
  - Features
  - Budget
- Evaluation uses:
  - Confusion matrix
  - Precision and recall
- Trade-off between precision and recall depends on problem context
- Explainable AI improves transparency and trust in ML models

# Model Serving in ML Workflow (Vertex AI)

## Overview
- Third and final stage of ML workflow
- Steps involved:
  1. Model Deployment
  2. Model Monitoring
- Ensures the model is used in real-world applications

---

## Analogy
- Model Deployment → Serving food to customers  
- Model Monitoring → Ensuring restaurant operations run smoothly  

---

## Model Deployment

### Purpose
- Make the trained model available for predictions

---

### Deployment Options

#### 1. Online Prediction (Real-Time)
- Deploy model to an **endpoint**
- Used for:
  - Low latency requirements
  - Immediate predictions

- Example:
  - Real-time recommendations based on user activity

- Key Point:
  - Model must be deployed to an endpoint

---

#### 2. Batch Prediction
- Directly request predictions from the model
- Used for:
  - Large-scale predictions
  - No need for immediate response

- Example:
  - Periodic marketing campaigns based on user behavior

- Key Point:
  - No endpoint deployment required

---

### Deployment Methods
- Using Vertex AI UI
- Using APIs (code-based approach)

---

## Edge Deployment (Off-Cloud)

### What is it?
- Deploy model outside cloud (on devices or local systems)

### Why use it?
- Reduce latency
- Improve privacy
- Enable offline functionality

### Example
- IoT-based object detection in manufacturing
  - Real-time processing needed
  - Cloud latency may be too high

---

## Model Monitoring

### Purpose
- Track model performance after deployment
- Ensure:
  - Accuracy remains stable
  - System functions properly

---

## Vertex AI Pipelines

### What is it?
- Toolkit to:
  - Automate ML workflows
  - Monitor performance
  - Manage pipelines

---

### Key Features
- Serverless orchestration of ML workflow
- Automatically:
  - Tracks pipeline execution
  - Detects issues
  - Triggers alerts based on thresholds

---

### Development Tools
- Vertex AI Workbench
- Colab Enterprise

- Use SDKs to:
  - Define pipelines
  - Combine pre-built components

---

## Model Management
- Exists across all stages of ML workflow
- Handles:
  - Infrastructure
  - Resource management
- Allows data scientists to focus on logic instead of operations

---

## Key Takeaways
- Model serving makes ML models usable in production
- Two prediction types:
  - Online (real-time, requires endpoint)
  - Batch (delayed, no endpoint needed)
- Edge deployment helps in low-latency and offline scenarios
- Monitoring ensures long-term model reliability
- Vertex AI Pipelines enable automation and scalability

# MLOps and Workflow Automation (Vertex AI)

## Overview
- MLOps = Machine Learning Operations
- Combines:
  - Machine Learning
  - DevOps principles
- Goal:
  - Automate and manage ML systems in production

---

## Why MLOps?
- ML systems face challenges:
  - Data is constantly changing
  - Code evolves over time
- Need:
  - Continuous Integration (CI)
  - Continuous Training (CT)
  - Continuous Delivery (CD)

---

## Two Workflow Approaches

### 1. No-Code Approach
- Example:
  - AutoML via Google Cloud Console
- Suitable for:
  - Manual workflows
  - Beginners

---

### 2. Code-Based Approach
- Build **ML pipelines**
- Automates entire workflow
- Used for:
  - Scalable production systems

---

## Vertex AI Pipelines

### What is it?
- Core toolkit for MLOps on Vertex AI
- Automates:
  - Training
  - Evaluation
  - Deployment
  - Monitoring

---

### Supported Frameworks
- **Kubeflow Pipelines (KFP)**
- **TensorFlow Extended (TFX)**

#### When to use:
- TFX:
  - If using TensorFlow
  - Large-scale structured data
- KFP:
  - General-purpose alternative

---

## ML Pipeline

### Definition
- Series of automated steps forming an ML workflow

---

### Environments

#### 1. Development Environment
- Data preparation:
  - Extraction
  - Analysis
  - Processing
- Model development:
  - Training
  - Evaluation
  - Validation

- Output:
  - Trained model stored in model registry

---

#### 2. Staging & Production Environment
- Model serving:
  - Prediction
  - Monitoring

---

## Pipeline Components

### What is a Component?
- Self-contained code performing one task
- Equivalent to a function

---

### Types
- Pre-built components (provided by Google Cloud)
- Custom components (user-defined)

---

### Design Principle
- Each component should have:
  - Single responsibility
  - Reusability

---

## Building an ML Pipeline

### Step 1: Plan Components
- Define sequence of tasks
- Combine:
  - Pre-built components
  - Custom components

---

### Step 2: Build Custom Components
- Example:
  - **Evaluation Component**
    - Compares model performance to threshold
    - Decides:
      - Deploy model
      - Retrain model

---

### Step 3: Assemble Pipeline

#### Example Components
- `TabularDatasetCreateOp`
  - Creates dataset from Cloud Storage or BigQuery

- `AutoMLTabularTrainingJobRunOp`
  - Runs AutoML training job

- `EndpointCreateOp`
  - Creates endpoint

- `ModelDeployOp`
  - Deploys model to endpoint

- Custom Component:
  - Evaluation logic (threshold-based decision)

---

### Step 4: Compile and Run

- Compile pipeline:
  - `compiler.Compiler.compile`

- Run pipeline:
  - Define pipeline job
  - Execute workflow

---

## MLOps Maturity Levels

### Phase 0: Manual
- No automation
- Use UI tools like AutoML
- Important for understanding workflow

---

### Phase 1: Component Automation
- Build reusable pipeline components
- Partial automation

---

### Phase 2: Full Automation
- Integrate components into full pipeline
- Achieve:
  - CI (Continuous Integration)
  - CT (Continuous Training)
  - CD (Continuous Delivery)

---

## Example Use Case
- Classification model (e.g., bean classification)

### Workflow
1. Train model
2. Evaluate performance
3. Compare with threshold
4. If good → Deploy
5. Else → Retrain

---

## Benefits of MLOps

- Automation of ML lifecycle
- Reduced manual intervention
- Scalable and reliable systems
- Continuous monitoring and improvement

---

## Additional Features

- Pre-built pipeline templates available
  - For classification and regression
- Visualization of pipelines:
  - Shows components
  - Displays artifacts and workflow

---

## Key Takeaways
- MLOps brings DevOps practices to ML
- Vertex AI Pipelines enable full automation
- Pipelines consist of reusable components
- Automation evolves in phases:
  - Manual → Partial → Fully automated
- Enables continuous training, deployment, and monitoring

# How Neural Networks Learn

## Overview
- Neural networks learn by adjusting internal parameters to reduce prediction error
- Core idea:
  - Input data → Forward pass → Prediction → Error calculation → Backpropagation → Parameter update → Repeat

---

## Types of Neural Networks
- ANN (Artificial Neural Network) → Basic model
- DNN (Deep Neural Network) → Many hidden layers
- CNN (Convolutional Neural Network) → Image processing
- RNN (Recurrent Neural Network) → Sequential data
- LLMs (Large Language Models) → Modern language models

All of them are extensions of ANN.

---

## Structure of an ANN
- Layers:
  - Input layer
  - Hidden layer(s)
  - Output layer

- Components:
  - Neurons (nodes)
  - Connections (synapses equivalent)
  - Weights (learned parameters)

---

## Forward Propagation (How Prediction Happens)

### Step 1: Weighted Sum
- Each input is multiplied by its weight
- All results are summed

---

### Step 2: Activation Function (Hidden Layer)
- Applied to introduce non-linearity
- Without it, model becomes purely linear

---

### Step 3: Output Layer Computation
- Weighted sum computed again for output layer

---

### Step 4: Output Activation
- Produces final prediction (ŷ)

- Notation:
  - ŷ = predicted output
  - y = actual output

---

## Why Activation Functions are Needed

### Problem Without Activation
- Entire network becomes linear
- Multiple layers collapse into one linear equation
- Result:
  - No advantage of deep learning

---

### Solution: Non-linearity
- Activation functions introduce complexity
- Allow learning of real-world patterns

---

## Common Activation Functions

### ReLU (Rectified Linear Unit)
- If input < 0 → output = 0
- If input ≥ 0 → output = input

---

### Sigmoid
- Outputs value between 0 and 1
- Used in:
  - Binary classification
  - Logistic regression

---

### Tanh
- Outputs between -1 and +1
- Zero-centered activation

---

### Softmax
- Used for multi-class classification
- Converts outputs into probabilities

- Properties:
  - Values between 0 and 1
  - Sum of all outputs = 1

---

## Loss and Cost Functions

### Loss Function
- Error for a single data point

### Cost Function
- Average error over entire dataset

---

## Common Cost Functions

### Mean Squared Error (MSE)
- Used in regression

:contentReference[oaicite:0]{index=0}

---

### Cross-Entropy Loss
- Used in classification
- Measures difference between probability distributions

---

## Backpropagation
- Process of updating weights based on error
- Works by propagating error backward through the network

---

## Gradient Descent

### Purpose
- Minimize cost function

### Key Idea
- Move step-by-step toward minimum error

---

### Direction of Learning
- Uses derivative (gradient) to decide direction:
  - Negative gradient → move right/down
  - Positive gradient → move left/down

---

### Learning Rate
- Controls step size

- If too small:
  - Slow training

- If too large:
  - Overshooting / divergence

---

## Iteration and Epochs

- One full pass through dataset = **epoch**
- Training involves multiple epochs
- Model improves gradually over iterations

---

## Training Process Summary

1. Forward pass (prediction)
2. Compute loss
3. Backpropagation
4. Gradient descent update
5. Repeat for multiple epochs

---

## Parameters vs Hyperparameters

### Parameters (learned by model)
- Weights
- Biases

---

### Hyperparameters (set by human)
- Number of layers
- Number of neurons
- Learning rate
- Activation functions
- Number of epochs

---

## Key Takeaways
- Neural networks learn by minimizing error
- Activation functions enable non-linearity
- Loss functions measure prediction quality
- Backpropagation + gradient descent update weights
- Training is an iterative process over many epochs
- Hyperparameters control how learning happens

