# AI Foundations

## Agenda

1. A use case:- We explore a real-world use case where  AI addresses familiar challenges, revealing its capability and potential
2. AI on Google Cloud :- How Google Cloud helps to solve both traditional AI and Generative AI problems
3. AI Infrastructure :- Here we get familiar with Google Cloud's Compute, Storage, Data and AI Products
4. AI Model :- We look into models necessary for AI development
5. BigQueryML:- We look into hands-on application of this using BigQueryML, connecting AI and Data
6. Summary :- Hands-on Lab 

## A Use Case - Coffee on Wheels

* It sells coffee on trucks.
* Operates in Major Cities

### Challenges

* Location and Route Optimization
* Sales Forecasting and real-time Monitoring
* Automating Marketing Campaigns

### Addressing these challenges through AI

#### Location and Route Optimization

* AI suggests routes based on weather, congestion and city events (like a football game!)
* Reduces travel time and cost

* Behind the Scenes:
 - Multimodal Data is collected to get data about the surroundings
 - BigQueryML studies Customer Behaviour and Foot-Traffic Patterns
 - AI Models in Vertex AI predict best location to park trucks
 - Insights are visualized using dashboards to support decision making

#### Sales Forecasting and Real-Time Monitoring

##### About

###### Sales Forecasting

* Predicts future sales for each truck and location
* Uses historical sales and seasonal trends
* Helps plan inventory and staffing
* Supports better business and revenue planning

###### Real-Time Monitoring

* Tracks sales and performance as they happen
* Displays live metrics as they happen
* Helps identify underperforming items quickly
* Enables fast business decisions and adjustments

##### Behind-the-Scenes

###### Sales Forecasting
* It is analyzed using BigQuery
* ML Models are trained on Vertex AI
* Predictive AI forecasts future trends
* Results are visualized using dashboards for insights

###### Real-Time Monitoring
* Sales data is continuously streamed into system
* BigQuery processes incoming data into near real-time
* Dashboards update constantly to reflect current performance
* Alerts and Insights help team respond immidiately


#### Automating Marketing Campaign

* Automates creation and execution of marketing campaign
* Generates Personalized Content for customers
* Improves marketing efficieny and consistency
* Helps increase customer engagement and sales

## AI on Google Cloud

### Why should you choose Google for AI?

* Google has a history of leveraging AI in powerful products (E.g. Search, Maps, Workspace)
* It is a leader in AI and ML innovation (e.g. Vertex AI, Gemini, NotebookLM)
* Google belives in responsible AI and collaborative progress

### There are two kinds of AI Problems:

* Predictive AI:
 - Uses existing data to classify information
 - Predicts future outcomes based on historical patterns
 - Excels at learning what's already there to make informed decisions
 - E.g. Prediction of sales forecasting and route optimization
* Generative AI
 - Creates Summaries
 - Uncovers Complex Correlations
 - Generates new content such as text, images or videos 
 - E.g. Creation of customer responses and automation of marketing campaigns

### When to use Predictive and Generative AI?

* Predictive AI is used for Forecasting and Prediction Tasks
* Generative AI is used to generate Multimodal content and automation
* Not a hard line drawn in the application - sometimes, you can use both of them in your application

### Google Cloud Infrastructure

#### Layer 1 - AI Infrastructure

* Foundation layer with
 - Advanced Compute
 - Networking
 - Storage
* Supports all AI workloads

#### Layer 2 - AI Development
 - Vertex AI provides all the tools needed for AI development like Design, Training and Deployment
 - It is powered by foundational models like Gemini and integrated deployment pipelines
 - Integrates seamlessly with BigQuery
 - Ideal for developers, data scientists and engineers

#### Applications and Solutions
* Ready-to-use tools for:
 - Business users
 - Analysts
* Enables rapid prototyping without deep technical skills

### Course Structure

#### Module 1

* AI Infrastructure
* Data Tools
* Builds the foundation for AI development

#### Module 2

* Focuses on Generative AI
* Learn about Foundational models and tol,s for building AI Applications

#### Module 3

* Focuses on Predictive AI
* Explores multiple options for training ML models  

#### Module 4

* Build an ML model end-to-end
 - Data Preparation
 - Model Training
 - Deployment


## AI Infrastructure

AI Infrastructure has three layers:

1. Networking and Security Layer
>  - Lays the foundation to support all of Google's infrastructure and applications

2. Compute and Storage facilities
>  - Google Cloud decouples or seperates the compute and storage units so they can scale independently based on need

3. Data and AI products
> - Enable you to perform tasks to
>> - Ingest
>> - Store
>> - Process
>>  - Deliver business insights, data pipelines and ML models


## Some essentials about Google Cloud

### Compute

* Organizations with growing data needs lot of compute power to run data and AI jobs
* Google Cloud offers several platforms which offer features ranging from flexible infrastructure to fully managed serverless platforms
* These platorms aim to balance control and convinience

#### Examples:

##### Compute Engine

* Has high control 
* Least convininence
* It is like managing a physical server

##### Google Kubernetes Engine (GKE)

* Medium Control
* Medium Conveninence
* Control over containerized apps with orchestration benefits

##### Cloud Run

* Less control
* More convenience
* Serverless Convinience, Google manages the infrastructure

#### Hardware

* The processing power in Google Cloud comes from the hardware.
* In the current world, the traditional computer chips like Central Processing Units (CPUs) or even the more recent Graphics Processing Units (GPUs) may not be adequate for AI workloads
* That's why in 2016, Google developed the Tensor Processing Unit (TPU)
* TPUs are Google's customized application-specific chips (ASICs) to accelerate AI workloads
* CPUs and GPUs are general-purpose hardware
* TPUs are domain-specific hardware.

### Storage

* Most applications require a database and storage solution of some kind
* The best option depends on your:
> * Data type
> * Business needs

* For unstructured data like documents, images and audio files, cloud storage is your ideal choice
* For structured data with rows, columns and the like, there are options like BigQuery and AlloyDB (for PostgreSQL) and others

* BigQuery, Google's flagship data warehouse, is able to handle
> * Structured Data
> * Semi-Structured data (like JSON)
> * Unstructured Data ( by creating an external table that provides a structured reference to that data)


### Data and AI Products

* Google Cloud provides a comprehensive suite of data and AI tools
* To build a data-to-AI project, you orchastrate these products in a data-to-AI workflow 

#### Data-to-AI Workflow

* Ingest and Process
> * Real-time and Batch data both from diverse sources
> * Using tools like Pub/Sub, Dataflow, Dataproc and Cloud Data Fusion

* Store and Analyze
> * Store your data in solutions like CLoud Storage
> * Use analysis tools like BigQuery, AlloyDB, Cloud SQL and Spanner
> * Use BigTable and Firestore for NoSQL databases
> * Use Looker for Visualization 

* Activate with AI  
> * Use Vertex AI as your central Ai development platforms
> * Products:
>> * Vertex AI Studio, Agent Builder, AutoML and notebooks for AI projects for out-of-the-box solutions and custom builds

#### Main focus topics in this course - Vertex AI and BigQuery


## AI Models

First, lets clarify two topics - Artificial Intelligence and Machine Learning

* Artificial Intelligence is an umbrella term that encompasses that includes anything related to computers mimicking human intelligence
> * Applications - Robots and Self-driving Cars

* Machine Learning is a subset of Artificial Intelligence that allows computers to learn without being explicitly programmed
> * ML usually includes supervised and unsupervised learning
> * Supervised Learning deals with labelled data, is task driven and identifies a goal
>> * Classification - Predicts a categorical variable (E.g. Logistic Regression)
>> * Regression - Predicts a numeric variable (E.g. Simple Regression)
> * Unsupervised Learning deals with unlabelled data, is data-driven and identifies a pattern
>> * Clustering - Groups data points together (E.g. K-means clustering)
>> * Association - Identifies underlying relationships (E.g. Association Rule Learning)
>> * Dimensionality Reduction - Reduces the number of dimensions (E.g. Pricipal Component Analysis) 
* Deep Learning, or Deep Neural Networks is a subset of machine learning that adds layers in between input data and output results to make a machine learn at much depth

* Generative AI or GenAI creates content and performs tasks based on requests
> * It uses foundational models like Large Language Models ( a type of deep learning model) to predict, interpret and interact with language


## BigQuery ML

* In this lesson, we explore BigQueryML, the primary data analytics tool on Google Cloud
* It is a fully managed storage facility for datasets
* It is a fast SQL-based analytical engine
* The two services are connected by Google's high-speed internal network
* In BigQuery, you can perform both data analytics and build pre-defined ML models within BigQuery
* This lesson:
> * Capabilities of BigQuery to build ML Models
> * Steps and key SQL commands

* Building and Training an ML Model is a very time and resource-intensive task because it involves:
> * Importing and preparing data
> * Experimenting with different models
> * Training the model with new data
> * Deploy the model to make predictions 

* With BigQueryML, you can manage the tabular data and execute ML models in one place with just a few steps.

* BigQueryML tunes the parameters for you and helps to manage the ML workflow

### Key Phases of a BigQuery ML Project

1. Extract, Transform and Load Data into BigQuery 
> * If using other Google products like Youtube, look for easy connectors to get that data into BigQuery
> * Enrich existing data warehouse with other data sources using SQL joins
2. Select and preprocess features
> * Use SQL to create the training dataset for the model to learn from
> * BigQuery does some of the preprocessing FOR you, like one-hot encoding of categorical variables
3. Create the model inside BigQuery
> * Use the `CREATE MODEL` command 
> * Use the `input_label_cols` variable to define if the model is supervised or unsupervised
4. Evaluate the performance of the trained model
> * Execute and `ML.EVALUATE`query
> * In the query, mention the parameters to work on, like `roc_auc`, `accuracy`, `precision` and `recall`
5. Use the model to make predictions
> * Invoke the `ML.PREDICT` command


### Models Supported by BigQueryML

1. Classification
> * Logistic Regression
> * DNN Classifier (TensorFlow)
> * XGBoost
> * AutoML Tables
> * Wide and Deep NNs
2. Regression
> * Linear Regression
> * DNN Classifier (TensorFlow)
> * XGBoost
> * AutoML Tables
> * Wide and Deep NNs 
3. Other Models
> * k-means clustering
> * Time-Series Forecasting (ARIMA+)
> * Recommendation - Matrix Factorization
> * Anomaly detection 
4. MLOps
> * Importing TensorFlow models to batch prediction
> * Exporting models from BigQuery ML for online prediction
> * Tuning hyperparameters using Vertex AI Vizier

MLOps (Machine Learning Operations) turns an ML Experiment into production and helps to
1. Deploy
2. Monitor
3. Manage the ML Models

 
