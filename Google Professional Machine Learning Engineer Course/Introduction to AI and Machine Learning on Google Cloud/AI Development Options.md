# Predictive AI & ML Development Options (Google Cloud)

## 1. Overview
This module shifts focus from:
- Generative AI → content generation
to:
- Predictive AI → forecasting, classification, traditional ML tasks

Goal:
- Understand how to build ML models
- Explore available development options


## 2. Google Cloud AI Development Spectrum

Options range from:
- No-code → easiest
- Low-code → moderate flexibility
- Full-code → maximum control

Applies to both:
- Generative AI
- Predictive AI


## 3. Types of Users and Their Needs

### Business Users
- No technical background
- Want:
  - Quick prototyping
  - Minimal setup

### Data Scientists
- Have training data
- Want:
  - Build models efficiently
  - Avoid heavy manual tuning

### ML Engineers
- Prefer:
  - Full control
  - Custom pipelines
  - End-to-end system design


## 4. Development Options

### 4.1 No-Code / Out-of-the-Box
- Tools:
  - Gemini Enterprise
  - Conversational Agents

Use Case:
- Quick solutions without coding


### 4.2 Low-Code Options

#### AutoML
- Build custom models using UI
- Minimal coding required

#### Pre-trained APIs
- Use ready-made models
- No training required


### 4.3 Code-Based Options

#### BigQuery ML
- Build models using SQL
- Works within BigQuery

#### Custom Training
- Build models from scratch
- Full control over pipeline


## 5. Comparison of ML Options

### Data Type Support

| Option             | Supported Data Types                          |
|------------------|----------------------------------------------|
| Pre-trained APIs | Text, image, video, audio                    |
| AutoML           | Tabular, image                              |
| BigQuery ML      | Tabular, semi-structured (JSON)              |
| Custom Training  | All types (text, image, video, etc.)         |


### Training Data Requirement

| Option             | Training Data Needed |
|------------------|--------------------|
| Pre-trained APIs | No                 |
| AutoML           | Yes                |
| BigQuery ML      | Yes                |
| Custom Training  | Yes (large amount) |


### Skill Requirement

| Option             | Skill Level Required |
|------------------|---------------------|
| Pre-trained APIs | Low                 |
| AutoML           | Low                 |
| BigQuery ML      | Medium (SQL)        |
| Custom Training  | High                |


### Hyperparameter Tuning

| Option             | Tuning Control |
|------------------|---------------|
| Pre-trained APIs | No            |
| AutoML           | No            |
| BigQuery ML      | Yes           |
| Custom Training  | Yes           |


### Training Time

| Option             | Training Time |
|------------------|--------------|
| Pre-trained APIs | None         |
| AutoML           | Moderate     |
| BigQuery ML      | Moderate     |
| Custom Training  | High         |


## 6. When to Use Each Option

### Pre-trained APIs
- No ML expertise
- No training data
- Common tasks:
  - Vision
  - NLP
  - Speech

Best for:
- Fast deployment


### BigQuery ML
- Data already in BigQuery
- Team knows SQL

Best for:
- Quick model building on structured data


### AutoML
- Have training data
- Want minimal coding

Best for:
- Custom models without deep ML knowledge


### Custom Training
- Need full control
- Complex use cases

Best for:
- ML engineers and advanced workflows


## 7. Key Decision Factors

- Technical expertise
- Availability of training data
- Required customization
- Time constraints
- Budget considerations


## 8. Key Takeaways

- Google Cloud provides a full spectrum of ML tools
- Choice depends on:
  - Skill level
  - Data availability
  - Business requirements
- Pre-trained APIs are fastest but least flexible
- Custom training is most powerful but resource-intensive
- AutoML and BigQuery ML sit in the middle

# Vertex AI (Google Cloud Unified AI Platform)

## 1. Overview
Vertex AI is Google Cloud’s unified platform for:
- Building
- Deploying
- Managing machine learning models

Supports:
- Generative AI
- Predictive AI


## 2. Why Vertex AI is Needed

Challenges in ML development:
- Difficulty in moving models to production
- Scalability issues
- Monitoring and maintenance challenges
- CI/CD (continuous integration and delivery)
- Fragmented tools and workflows
- High coding requirements

Observation:
- Many ML projects fail to move beyond the pilot stage

Solution:
- Vertex AI provides a unified ML platform


## 3. What Does "Unified Platform" Mean?

### 3.1 End-to-End ML Pipeline

Vertex AI covers the entire ML lifecycle:

#### 1. Data Readiness
- Upload data from:
  - Cloud Storage
  - BigQuery
  - Local systems

#### 2. Feature Engineering
- Create features (processed inputs for ML models)
- Store and share via Feature Store

#### 3. Training & Tuning
- Train models
- Perform hyperparameter tuning

#### 4. Deployment & Monitoring
- Deploy models to production
- Monitor performance
- Enable continuous improvement


### 3.2 Unified AI Capabilities

Supports both:

- Generative AI:
  - Content generation (text, image, video, etc.)

- Predictive AI:
  - Classification
  - Forecasting


## 4. Model Building Options in Vertex AI

### 4.1 AutoML
- No-code / low-code solution
- User-friendly UI
- Focus on business problems, not coding

Best for:
- Data scientists with minimal coding needs


### 4.2 Custom Training
- Code-based solution
- Full control over model and pipeline

Tools:
- Vertex AI Workbench
- Colab

Best for:
- ML engineers
- Advanced use cases


### 4.3 BigQuery Integration
- Write SQL within Vertex AI Workbench
- Seamlessly connect:
  - BigQuery
  - Vertex AI


## 5. Benefits of Vertex AI (4S Framework)

### 5.1 Seamless
- Smooth workflow from data → model → production

### 5.2 Scalable
- MLOps capabilities:
  - Auto scaling
  - Monitoring
  - Resource management

### 5.3 Sustainable
- Reusable:
  - Features
  - Models
  - Pipelines

### 5.4 Speedy
- Reduces coding effort
- Up to 80% fewer lines of code


## 6. Key Takeaways

- Vertex AI unifies the entire ML workflow
- Solves production and usability challenges
- Supports both Gen AI and predictive AI
- Provides flexible model-building options:
  - AutoML (simple)
  - Custom training (advanced)
- Enables scalable and production-ready ML systems


# AutoML (Automated Machine Learning)

## 1. Overview
AutoML (Automated Machine Learning) automates the process of:
- Building
- Training
- Tuning
- Deploying ML models

Goal:
- Reduce manual effort in ML development
- Enable faster and more efficient model building


## 2. Motivation

Traditional ML challenges:
- Time-consuming:
  - Feature engineering
  - Model selection
  - Hyperparameter tuning
- Requires repeated experimentation
- High expertise needed

Solution:
- AutoML automates the ML pipeline


## 3. AutoML in Vertex AI

- Introduced around 2018
- Integrated into Vertex AI since 2021
- Provides a no-code / low-code interface

Key Advantage:
- Build ML models using UI (point-and-click)


## 4. AutoML Pipeline (4 Phases)

### Phase 1: Data Processing
- Automatically prepares data

Handles:
- Numerical data
- Date/time data
- Text
- Categories
- Arrays and nested fields

Goal:
- Convert data into model-ready format


### Phase 2: Model Search & Tuning

Two key technologies:

#### 4.2.1 Neural Architecture Search (NAS)
- Automatically searches for best model architecture
- Tries multiple models
- Tunes hyperparameters

Goal:
- Find optimal model for given data


#### 4.2.2 Transfer Learning
- Uses pre-trained models as a starting point

Concept:
- Learn from existing knowledge instead of starting from scratch

Benefits:
- Faster training
- Requires less data
- Improves accuracy

Example:
- Large Language Models (LLMs)
  - Pre-trained on large datasets
  - Fine-tuned for specific tasks


### Phase 3: Model Selection (Ensembling)
- Selects top-performing models (typically ~10)

Technique:
- Combine models (ensemble)

Example:
- Averaging predictions

Benefit:
- Higher accuracy than single model


### Phase 4: Prediction
- Final model is used for inference
- Ready for deployment


## 5. Core Technologies Behind AutoML

- Automated data preprocessing
- Neural Architecture Search (NAS)
- Transfer Learning
- Hyperparameter tuning
- Model ensembling


## 6. Advantages of AutoML

- No-code / low-code approach
- Reduces manual effort
- Faster model development
- Works well with smaller datasets (via transfer learning)
- Produces high-accuracy models (via ensembling)


## 7. Limitations (Implied)

- Less control over:
  - Model architecture
  - Hyperparameters
- May not suit highly customized or complex use cases


## 8. Key Takeaways

- AutoML automates the entire ML pipeline
- Uses advanced techniques like:
  - NAS
  - Transfer Learning
  - Ensembling
- Enables non-experts to build ML models
- Best suited for:
  - Quick development
  - Standard ML tasks
- Trades flexibility for ease of use

# Pre-trained APIs (Low-Code ML Solution)

## 1. Overview
Pre-trained APIs provide ready-to-use machine learning models that:
- Do not require training
- Can be accessed via simple API calls

Best for:
- Users without large datasets
- Users with limited ML expertise


## 2. Motivation

Challenge:
- Training ML models requires:
  - Large datasets (hundreds of thousands of records)
  - Time and expertise

Solution:
- Use pre-trained APIs to directly access trained models


## 3. What is an API?

API (Application Programming Interface):
- Defines how software components communicate

Analogy:
- Like an electrical outlet
  - You only need to know how to plug in
  - No need to understand internal wiring

Key Idea:
- Use functionality without knowing internal implementation


## 4. How Pre-trained APIs Work

Basic Steps:

1. Authentication
   - Provide API key
   - Example:
     - configure(api_key="YOUR_API_KEY")

2. Model Selection
   - Choose model (e.g., Gemini)

3. API Call
   - Send input (prompt/request)

4. Response
   - Receive output from model


## 5. Example Workflow

- Initialize API client
- Select model (e.g., Gemini Flash)
- Send prompt:
  - "What are the three largest countries by area?"
- Receive generated response

Key Insight:
- Similar to calling a function


## 6. Types of APIs in Google Cloud

### 6.1 Generative AI APIs
- Gemini APIs (multimodal)
- Used for:
  - Content generation
  - Q&A
  - Multimodal tasks


### 6.2 Vertex AI APIs
- Used for:
  - Training
  - Monitoring
  - Tuning models

- Minimal ML expertise required


### 6.3 Specialized APIs

- Speech APIs → speech-to-text, text-to-speech
- Vision APIs → image analysis
- Document APIs → document processing
- Conversation APIs → chat systems


## 7. Natural Language API

Capabilities:
- Entity recognition
- Sentiment analysis
- Syntax analysis
- Text classification

Use Case:
- Extract insights from raw text


## 8. Advantages of Pre-trained APIs

- No training required
- Fast to implement
- Low technical barrier
- Scalable
- Handles complex tasks


## 9. Limitations

- Limited customization
- Dependent on pre-trained capabilities
- May not fit highly domain-specific tasks


## 10. Key Takeaways

- Pre-trained APIs are the easiest way to use ML
- Require no training data
- Work like function calls via API
- Ideal for:
  - Beginners
  - Rapid prototyping
  - Common ML tasks
- Trade-off:
  - Ease of use vs flexibility

# Custom Training (Code-Based ML Approach)

## 1. Overview
Custom Training is a **do-it-yourself ML approach** where you build models from scratch.

Used when:
- AutoML is too restrictive
- Pre-trained APIs are insufficient
- Full control is required over:
  - Model architecture
  - Training process
  - Frameworks and infrastructure

---

## 2. Why Custom Training?

- Enables **complete flexibility**
- Allows **custom solutions for complex problems**
- Supports **advanced optimization and experimentation**

Trade-off:
- High flexibility vs high complexity

---

## 3. Training Environment Options

### 3.1 Pre-built Containers
- Ready-to-use environments
- Includes:
  - Python
  - TensorFlow
  - PyTorch

Analogy:
- Furnished kitchen (everything ready)

Best for:
- Standard ML workflows
- Faster setup

---

### 3.2 Custom Containers
- Fully customizable environment
- You define:
  - OS and dependencies
  - Machine type (CPU/GPU/TPU)
  - Storage and configurations

Analogy:
- Empty kitchen (build everything yourself)

Best for:
- Specialized or production-grade needs

---

## 4. Development Tools

### 4.1 Vertex AI Workbench
- Jupyter Notebook-like environment
- Supports:
  - Data exploration
  - Model training
  - Deployment

### 4.2 Colab Enterprise
- Integrated with Vertex AI
- Familiar notebook-based coding environment

---

## 5. ML Libraries

ML libraries provide reusable code for building models.

Popular libraries:
- TensorFlow
- PyTorch
- scikit-learn

Benefits:
- Faster development
- Reduced complexity
- Strong community support

---

## 6. TensorFlow Architecture

TensorFlow = End-to-end ML platform with layered abstraction

### Layers:

1. **Hardware Layer**
   - CPU, GPU, TPU

2. **Low-Level APIs**
   - Custom operations (C++ / Python)

3. **Model Libraries**
   - Neural network layers
   - Loss functions
   - Metrics

4. **High-Level APIs (Keras)**
   - Simplified model building
   - Most commonly used

Note:
- Vertex AI fully manages TensorFlow across all layers

---

## 7. Model Building with tf.keras

### Step 1: Create Model
- Define layers using `Sequential`
- Example:
  - Input → Hidden → Output layers

### Step 2: Compile Model
- Define:
  - Loss function (performance metric)
  - Optimizer (training method)

### Step 3: Train Model
- Use `.fit()`
- Provide:
  - Training data (X, y)
  - Number of epochs (iterations)

### Step 4: Deploy Model
- Use trained model for predictions

---

## 8. Workflow Summary

1. Choose environment (container)
2. Select development tool (Workbench / Colab)
3. Use ML libraries
4. Build model
5. Train model
6. Evaluate performance
7. Deploy model

---

## 9. JAX (Emerging Framework)

- High-performance numerical computing library
- Flexible and efficient

Use cases:
- Research
- High-performance ML systems

Advantage:
- Faster computation
- Better scalability

---

## 10. Advantages

- Full control over ML pipeline
- Highly customizable
- Best for complex and domain-specific tasks
- Supports cutting-edge research

---

## 11. Limitations

- Requires strong ML knowledge
- Time-consuming
- Needs large datasets
- Higher computational cost

---

## 12. Key Takeaways

- Custom training = maximum flexibility
- Best for advanced ML use cases
- Requires coding + ML expertise
- Uses tools like:
  - Vertex AI Workbench
  - Colab Enterprise
- Built using libraries like TensorFlow, PyTorch