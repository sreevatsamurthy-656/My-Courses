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



