# **Workshop: Azure OpenAI and Form Recognizer BPA accelerator to improve Document analysis**

### Overview

Hello All, welcome to the workshop on Business Process Automation Accelerator, OpenAI and Form Recognizer. With this workshop, we have provided the necessary artifacts for you to get familiar with Form Recognizer Service, OpenAI capabilities and Business Process Automation Accelerator so you can take back some ideas on how to utilize the accelerator to build pipelines across multiple services to generate an AI solution that fits your business needs. 

This Github Repo contains all the files and code required to execute the **Azure OpenAI and Form Recognizer BPA accelerator to improve Document analysis**.

#### About the services covered

**Azure OpenAI**

Azure OpenAI Service provides REST API access to OpenAI's powerful language models including the GPT-3, Codex and Embeddings model series. These models can be easily adapted to your specific task including but not limited to content generation, summarization, semantic search, and natural language to code translation. Users can access the service through REST APIs, Python SDK, or our web-based interface in the Azure OpenAI Studio.
https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview

**Azure Form Recognizer**

Azure Form Recognizer is a cloud-based Azure Applied AI Service that uses machine-learning models to extract key-value pairs, text, and tables from your documents. Form Recognizer analyzes your forms and documents, extracts text and data, maps field relationships as key-value pairs, and returns a structured JSON output. 

**Business Process Automation(BPA) Accelerator**

Manually developing end-to-end solutions for business users may be costly and resource intensive. This accelerator provides a no code Studio for users to quickly build complex, multi-stage AI pipelines across multiple Azure AI and ML Services. Users can select, and stack, AI/ML Services from across Azure Cognitive Services (Speech, Language, Form Recognizer, ReadAPI), Azure Machine Learning into a single, fully integrated pipeline. Integration between services is automated by BPA, and once deployed, a web app is created. This customizable UI* provides and drag-n-drop interface for end users to build multi service pipelines. Finally, the user-created pipeline is triggered as soon as the first input file(s) are uploaded, storing the results in a document database.

### Goals
* Understand key concepts of Azure OpenAI, Azure Form Recognizer and understand how to leverage BPA accelerator in conjunction with Azure Search and other services 


### Agenda 
1. Forms Recognizer - Overview and Experience
1. Azure OpenAI - Brief overview & Accessibility
1. Business Process Automation(BPA) Accelerator Capabilities & Usage
1. Develop and execute BPA pipeline with Form Recognizer
1. Analyze the output with Azure Search
1. Azure OpenAI usage to enhance the extracted information

**Challenge 1:** Deploy Pre-trained Invoice Model
1. Analyze the output with Forms Recognizer Studio and Azure Search

**Challenge 2:** Train & Deploy Custom Model
1. Train a custom model using Form Recognizer Studio
1. Utilize the custom model in the BPA accelerator and analyze the output

**Challenge 3:** Develop & Deploy Azure OpenAI Pipeline
1. Develop a pipeline using Azure OpenAI Generic module on BPA
2. Learn how to use the Azure OpenAI GPT-3 Playground
3. Visualize the filtered and summerized data from ingested documents

#### Audience
1. Data Scientists
1. Business Analysts
1. Data science Managers
1. AI specialists
1. ML Engineers

#### Challenge Instructions
1. [Deploy Pre-trained Model with BPA](lab_instructions/lab_1.md)
1. [Train and Deploy Custom Model](lab_instructions/lab_2.md)
1. [Create and Deploy a OpenAI Pipeline](lab_instructions/lab_3.md)
