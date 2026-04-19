# Agenda

1. Generative AI on Google Cloud
2. Foundation Models
3. Idea to App
4. Prompt Engineering
5. Deployment and Model Tuning
6. AI Agents
7. Agent Building with Google CLoud
8. Summary

# Generative AI on Google Cloud


* It is a type of artificial intellengence that:
> * Generates multimodal content like:
> * Takes action for you

## Generating Content

Gen AI can generate multimodal content. This content can be:
* Text
* Code
* Images
* Speech
* Video
* 3D

Some applications of this include:
* Producing Images and Videos
* Summarizing Meeting Notes
* Creating Research Reports
* Developing Q and A chatbots

## Taking Action

In addition to content creation, GenAI can take action on your behalf using AI agents. For example, it can:
* Automate workflows
* Plan and book travel
* Schedule Appointments
* Assist with clinical diagnoses

## How does Google deliver its AI services and help you build its own GenAI applications?

1. Foundation Models
> * Gemini
> * Veo
> * Imagen
> * Embeddings

2. GenAI development
> * Vertex AI Studio
> * Agent Builder
> * Model Garden

3. GenAI Applications
> * Gemini Enterprise
> * NotebookLM

* Generative AI is transforming how you work and create

# Foundation Models

## 1. What are Foundation Models?
Foundation models are large pre-trained AI models trained on massive datasets.

They:
- Learn patterns from text, images, video, and audio
- Generate new content based on learned patterns

Key Characteristics:
- Very large number of parameters (millions to trillions)
- Require high computational power
- Capable of complex reasoning and pattern recognition


## 2. How Generative AI Works
- AI learns from existing data through training
- Training produces a foundation model
- The model can:
  - Generate text
  - Create images and videos
  - Answer questions
  - Analyze data


## 3. Google’s Foundation Models

### General Purpose Models (Gemini Family)
- Gemini Pro
  - Best for complex reasoning tasks

- Gemini Flash
  - Optimized for speed and low latency
  - Suitable for real-time applications like chatbots

- Gemini Flash-Lite
  - Cost-efficient
  - Suitable for batch processing tasks


### Specialized Models
- Imagen
  - Image generation

- Veo
  - Video processing

- Embeddings models
  - Semantic search and data representation


## 4. Multimodal AI

Definition:
A multimodal model can process multiple types of data such as text, images, video, and audio.

Example:
- Input: Image of cookies
- Output: Recipe video walkthrough

Importance:
- Better understanding of context
- More human-like reasoning
- Enables real-world applications


## 5. Why Gemini for Multimodal Tasks
Gemini can:
- Process text, images, video, and audio
- Generate outputs across multiple modalities

Example Use Case:
- Home insurance risk assessment using:
  - Property images
  - Weather history
  - Inspection reports
  - Disaster videos

Best model: Gemini


## 6. Business Use Cases

Information Extraction:
- Extract text or data from images and videos

Information Analysis:
- Example: Categorize expenses from receipts

Information Retrieval:
- Answer questions based on extracted data

Content Creation:
- Generate advertisements, stories, and marketing content


## 7. Pre-trained vs Fine-tuned Models

Pre-trained Models:
- Trained on large general datasets
- Broad capabilities

Fine-tuned Models:
- Further trained on domain-specific data
- Used in healthcare, finance, and other industries

Analogy:
- Pre-trained = basic education
- Fine-tuned = specialized professional training


## 8. Horizontal vs Vertical AI

Horizontal AI:
- General-purpose models (e.g., LLMs)
- Used across multiple industries
- Tasks include content generation, summarization, and Q&A

Vertical AI:
- Industry-specific models
- Examples include disease diagnosis and financial modeling


## 9. Using Models on Google Cloud

No-Code:
- Google Cloud Console UI
- Used for prompt testing and exploration

Low-Code:
- APIs (e.g., Gemini API with cURL)
- Used for simple integrations

Code-Based:
- SDKs (Python, Java)
- Tools: Colab, Vertex AI Workbench
- Used for full-scale development


## 10. Key Takeaways
- Foundation models are the backbone of generative AI
- Multimodal capability is a major advancement
- Gemini is a general-purpose multimodal model
- Fine-tuning adapts models to specific industries
- Multiple access methods provide flexibility from no-code to full-code

# Idea to App

## 1. Motivation
Foundation models are powerful, but developers need tools to:
- Interact with them
- Build applications
- Deploy solutions in real-world scenarios

Google provides tools to support different roles.


## 2. Use Case: Cymbal Insurance

Three personas:

### Bea (Business Analyst)
- No technical background
- Wants to:
  - Prototype Gen AI apps quickly
  - Automate risk analysis and reporting

### Ann (AI Developer)
- Needs:
  - Prompt engineering tools
  - Ability to draft, evaluate, refine, and manage prompts

### Ian (ML Engineer)
- Needs:
  - Scalable and secure systems
  - Pipelines for:
    - Deployment
    - Fine-tuning models


## 3. Google Gen AI Tools

### Vertex AI Studio
- Build, deploy, and scale Gen AI applications
- Supports low-code / no-code development

### Agent Builder & Gemini Enterprise
- Design and manage AI agents

### NotebookLM
- AI-powered research and note-taking
- Works with documents for insights


## 4. Vertex AI Studio

Definition:
Vertex AI Studio is an interface between developers and foundation models.

Capabilities:
- Rapid prototyping of applications
- Prompt testing and refinement
- Model tuning with custom data
- Integration of real-world data
- Deployment with auto-generated code

Analogy:
- Models = raw materials
- Developer = craftsperson
- Studio = toolkit


## 5. Prompt to Production Lifecycle

Steps:
1. Design prompts
2. Evaluate outputs
3. Refine prompts
4. Build applications
5. Test applications
6. Deploy to production
7. Monitor and optimize


## 6. Prompts

Definition:
A prompt is a natural language input given to an AI model.

It can be:
- A question
- A task
- An instruction

Output can include:
- Text
- Code
- Images
- Video
- Audio


## 7. Prompt Design vs Prompt Engineering

Prompt Design:
- Creating a prompt to get a response

Prompt Engineering:
- Iterative process of:
  - Designing
  - Refining
  - Optimizing prompts


## 8. Anatomy of a Good Prompt

### 1. Task (Required)
- Core instruction
- Example:
  - "Conduct a risk analysis"

### 2. Context (Optional)
- Background or role definition
- Example:
  - "You are a business analyst at an insurance company"

### 3. Examples (Optional)
- Sample outputs or format
- Helps in complex tasks
- Also called few-shot prompting


## 9. Types of Prompting

Zero-shot:
- Only task is provided

Few-shot:
- Task + examples provided


## 10. Key Principles of Good Prompts

### Content
- Include:
  - Clear instructions
  - Relevant context
  - Examples if needed

### Structure
- Organize properly:
  - Use steps
  - Use labels
  - Use delimiters


## 11. Example of a Good Prompt

Structure:
1. Context
2. Task
3. Steps
4. Examples

Better Prompt (Correct Answer):
- Includes:
  - Task
  - Context
  - Structured steps
  - Output format

Why it works:
- Clear guidance to the model
- Reduces ambiguity
- Improves output quality


## 12. Tips for Effective Prompting

- Be clear and specific
- Use structured instructions
- Break complex tasks into steps
- Iterate and refine prompts
- Avoid unnecessary jargon
- Define clear goals

Advanced Techniques:
- Few-shot prompting
- Chain-of-thought prompting
- Retrieval Augmented Generation (RAG)


## 13. Vertex AI Studio Features

### Help Me Write
- AI-assisted prompt creation
- Improves clarity and structure

### Prompt Gallery
- Pre-built prompt examples
- Filter by:
  - Modality (text, image, video, etc.)
  - Task (classification, Q&A, etc.)

### Multimodal Support
- Input:
  - Documents
  - PDFs
  - Images
  - Videos
  - YouTube content

- Output:
  - Multimodal responses


## 14. Example Prompt (Bea’s Case)

Task:
- Conduct housing risk assessment

Context:
- Business analyst at insurance company

Instructions:
- Identify risks and severity
- Categorize risks
- Analyze impact
- Provide insights and recommendations


## 15. Rapid Prototyping

Steps in Vertex AI Studio:
- Write prompt
- Refine using AI tools
- Click "Build with Code"
- Deploy as application

Result:
- Auto-generated web app


## 16. Key Takeaways

- Vertex AI Studio enables fast Gen AI development
- Prompt engineering is critical for good outputs
- A good prompt includes:
  - Task
  - Context
  - Examples
- Iteration is essential
- Multimodal capabilities enhance applications
- Rapid prototyping reduces time from idea to application

# Deployment and Model Tuning


## 1. Overview
This lesson covers the second half of the prompt-to-production lifecycle:
- Build
- Test
- Deploy
- Monitor
- Optimize


## 2. From Prompt to Application

Initial approach:
- Use "Build with Code" → "Deploy as App"
- Quickly creates a working application

Advanced needs:
- Customization
- Integration into existing systems

Solution:
- Vertex AI Studio auto-generates code


## 3. Ways to Access Models

### No-Code
- UI in Vertex AI Studio
- Used for testing and prototyping

### Low-Code
- APIs (cURL)
- SDKs (Python)

Benefit:
- Flexibility to integrate into real applications


## 4. Code Generation & Deployment

Features:
- Auto-generated code from prompts
- Includes prompt + parameters

Deployment Tools:
- Cloud Run
- Cloud Shell

Advantage:
- No need to manage infrastructure
- Simplifies production deployment


## 5. Monitoring and Optimization

After deployment:
- Continuous monitoring is required
- Ensure:
  - Accuracy
  - Relevance
  - Performance


## 6. Grounding and RAG

Problem:
- Models rely on pre-trained data
- Data may be outdated or incorrect

### Grounding
- Connects model to external data sources
- Ensures up-to-date and verified responses

### RAG (Retrieval Augmented Generation)
- Method to implement grounding

Concept:
- Grounding = What
- RAG = How

Data Sources:
- Google Search (real-time)
- Custom enterprise data


## 7. Improving Model Quality

Two main approaches:

### 1. Grounding
- Adds external real-time knowledge
- Does not change model internally

### 2. Model Tuning
- Improves model behavior and output quality


## 8. Types of Model Customization

### 8.1 Prompt Design
- Uses instructions and examples
- Does not change model parameters

Advantages:
- Fast
- No coding required
- Low resource usage


### 8.2 Parameter-Efficient Tuning (Adapter Tuning)
- Updates small subset of parameters

Advantages:
- Efficient
- Good for domain adaptation


### 8.3 Full Fine-Tuning
- Updates all model parameters

Advantages:
- Best performance for complex tasks

Disadvantages:
- High computational cost


## 9. Supervised Fine-Tuning

Definition:
- Training model using labeled data

Data Format:
- JSONL file
- Each record contains:
  - Input (prompt)
  - Output (expected response)

Example:
- Input: "This building is great"
- Output: "Positive"

Use Cases:
- Classification
- Summarization
- Information extraction
- Chat systems


## 10. Tuning Workflow in Vertex AI

Steps:
1. Go to Vertex AI Studio → Tuning
2. Create tuned model
3. Provide dataset (JSONL format)
4. Start tuning job
5. Monitor progress

Output:
- New tuned model

Deployment:
- Stored in Model Registry
- Deploy to endpoint
- Test in Vertex AI Studio


## 11. Grounding vs Fine-Tuning (Important)

Analogy:
- Foundation Model → Basic education
- Fine-Tuning → Specialized training
- Grounding → Staying updated with latest knowledge

Key Difference:
- Fine-tuning = improves internal knowledge
- Grounding = adds external real-time knowledge


## 12. Key Takeaways

- Vertex AI Studio supports full lifecycle from prompt to production
- Code generation simplifies deployment
- Monitoring is essential for real-world performance
- Grounding and RAG ensure up-to-date responses
- Prompt design is the simplest customization method
- Fine-tuning improves model performance for specific tasks
- Trade-off exists between performance and computational cost


# AI Agents and Agentic AI

## 1. Overview
Traditional Gen AI applications are:
- Conversational
- Prompt → Response systems

Limitation:
- Cannot take actions
- Cannot interact with external systems

Solution:
- AI Agents


## 2. Evolution of Generative AI

Stages:
1. Chatbots
   - Answer questions
   - Generate content

2. AI Agents
   - Take actions
   - Interact with systems

3. Agentic AI
   - Multiple agents working together
   - Handle complex, multi-step tasks


## 3. What is an AI Agent?

Definition:
An AI agent is an application that:
- Uses AI models for reasoning
- Uses tools for external interaction
- Coordinates actions to achieve a goal

Key Characteristics:
- Goal-oriented
- Autonomous (to some extent)
- Capable of reasoning and decision-making


## 4. Why AI Agents are Needed

Problem with foundation models:
- Rely only on pre-trained knowledge
- Cannot:
  - Access real-time data
  - Interact with applications
  - Execute workflows

AI Agents solve this by:
- Connecting to external systems
- Taking actions
- Learning from feedback


## 5. Agentic AI

Definition:
- System of multiple coordinated AI agents

Capabilities:
- Handles complex workflows
- Performs multi-step reasoning
- Coordinates across domains

Example:
- Insurance system with:
  - Underwriting agent
  - Claims agent
  - Risk analysis agent


## 6. Components of an AI Agent

### 6.1 Model (Brain)
- AI model (e.g., Gemini)
- Responsible for:
  - Reasoning
  - Planning
  - Decision-making

### 6.2 Tools (Hands, Feet, Senses)
- Interfaces to external systems
- Typically APIs:
  - GET
  - POST
  - PATCH
  - DELETE

Functions:
- Take actions (e.g., send email)
- Fetch data (e.g., weather, database)

### 6.3 Orchestration Layer (Nervous System)
- Controls execution flow
- Manages:
  - Sequence of actions
  - Decision loops
  - Feedback handling

Function:
- Connects model decisions with tool execution


## 7. How AI Agents Work

Step-by-step:
1. Receive goal or task
2. Model plans actions
3. Tools execute actions
4. Results are observed
5. Feedback is processed
6. Loop continues until goal is achieved


## 8. Example Use Case (Insurance)

Task:
- Handle insurance claims

Steps:
1. Fetch claim history → Tools
2. Validate against policies → Model
3. Send confirmation email → Tools
4. Manage sequence → Orchestration layer


## 9. Component Responsibilities

- Model:
  - Understands logic and communication
  - Makes decisions

- Tools:
  - Connect to external systems
  - Perform actions

- Orchestration:
  - Manages workflow
  - Controls execution sequence


## 10. Key Takeaways

- AI agents extend Gen AI from passive to active systems
- They enable:
  - Automation
  - Decision-making
  - Workflow execution
- Built using:
  - Models (reasoning)
  - Tools (action)
  - Orchestration (control)
- Agentic AI represents the next evolution:
  - Multi-agent coordination
  - Complex problem solving


# Building AI Agents on Google Cloud

## 1. Overview
This lesson explains how to build AI agents using Google Cloud tools.

Layers in Google GenAI Architecture:
1. Foundation Models
2. Development Tools
3. Application Layer


## 2. Google GenAI Architecture for Agents

### 2.1 Foundation Layer (Brain)
- Vertex AI Model Garden
- Provides:
  - Google models (e.g., Gemini)
  - Third-party models

Role:
- Supplies models for reasoning and decision-making


### 2.2 Development Layer
- Vertex AI Agent Builder

Components:
- Agent Development Kit (ADK)
- Agent Engine
- Agent Garden

Purpose:
- Build agents end-to-end
- Supports:
  - Low-code
  - Pro-code development


### 2.3 Application Layer
- Gemini Enterprise
- Customer Engagement Suite

Purpose:
- No-code or minimal-code solutions
- Designed for business users


## 3. Key Decision Factors

When choosing tools:

### Ease of Use
- No-code → Gemini Enterprise
- Low-code → Agent Builder
- Pro-code → ADK / custom build

### Flexibility
- Low → Ready-made solutions
- High → Custom-built agents


## 4. Gemini Enterprise

Definition:
- No-code platform for building and using AI agents

Features:
- Combines:
  - AI models
  - Google Search
  - Enterprise data

Capabilities:
- Multimodal search across:
  - Documents
  - Images
  - Videos

Benefits:
- Breaks data silos
- Provides contextual, cited answers


### Agentspace

- Hub for AI agents
- Includes:
  - Pre-built agents
  - No-code agent designer

Agent Capabilities:
- Automate workflows
- Perform actions:
  - Update tickets
  - Send emails
  - Analyze reports


## 5. NotebookLM

Definition:
- AI-powered research assistant

Features:
- Accepts multiple data formats:
  - PDFs
  - Text
  - Markdown
  - Audio
  - Web links
  - YouTube links

Capabilities:
- Summarization with citations
- Q&A based on provided sources
- Content generation
- Insight extraction


### Studio Features

- Audio Overview:
  - Generates podcast-style summaries

- Notes:
  - Study guides
  - FAQs
  - Timelines
  - Briefings

Key Idea:
- Works only on provided data (controlled context)


## 6. Limitations of No-Code Tools

Tools like Gemini Enterprise:
- Limited customization
- Cannot:
  - Fully integrate with legacy systems
  - Enforce complex business logic
  - Customize behavior deeply

Solution:
- Use Vertex AI Agent Builder


## 7. Vertex AI Agent Builder Components

### 7.1 Agent Garden
- Pre-built agent templates
- Includes:
  - Sample code
  - Blueprints

Use Case:
- Start quickly without building from scratch


### 7.2 Agent Development Kit (ADK)
- Open-source framework
- Used with Python

Capabilities:
- Full control over agent logic
- Integration with:
  - APIs
  - Databases
  - Google Cloud services

Analogy:
- SDK for building AI agents


### 7.3 Agent Engine
- Managed runtime environment

Features:
- Deployment
- Scaling
- Monitoring

Benefit:
- No infrastructure management required


## 8. Development Paths

### 8.1 No-Code Path
Tools:
- Gemini Enterprise
- Conversational agents

Best For:
- Business users
- Quick deployment

Limitations:
- Low flexibility


### 8.2 Low-Code Path
Tools:
- Agent Builder
- Agent Garden

Best For:
- Analysts
- Data scientists

Benefits:
- Faster development with customization


### 8.3 Pro-Code Path
Tools:
- ADK
- Custom solutions

Best For:
- Software engineers
- ML engineers

Benefits:
- Maximum flexibility
- Deep integrations
- Complex logic


## 9. Choosing the Right Approach

| Approach   | Ease of Use | Flexibility | Best For |
|-----------|------------|------------|----------|
| No-Code   | High       | Low        | Business users |
| Low-Code  | Medium     | Medium     | Analysts, DS |
| Pro-Code  | Low        | High       | Engineers |


## 10. Key Takeaways

- Google Cloud provides a full stack for AI agent development
- Choose tools based on:
  - Ease of use
  - Flexibility
- Gemini Enterprise is best for quick, no-code solutions
- Vertex AI Agent Builder enables customization
- ADK provides full control for complex systems
- NotebookLM is a powerful research and learning assistant