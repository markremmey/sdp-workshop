# Workshop: Analyze documents with Form Recognizer and Business Process Automation Accelerator (BPA)

### Overview

Hello All, welcome to the workshop on Business Process Automation Accelerator and Form Recognizer. With this workshop, we have provided the necessary artifacts for you to get familiar with Form Recognizer Service and Business Process Automation Accelerator so you can take back some ideas on how to utilize the accelerator to build pipelines across multiple services to generate an AI solution that fits your business needs. 

This Github Repo contains all the files and code required to execute the **Analyze documents with Form Recognizer and BPA Workshop**.

#### About the services covered

**Form Recognizer**

Azure Form Recognizer is a cloud-based Azure Applied AI Service that uses machine-learning models to extract key-value pairs, text, and tables from your documents. Form Recognizer analyzes your forms and documents, extracts text and data, maps field relationships as key-value pairs, and returns a structured JSON output. 

**Business Process Automation(BPA) Accelerator**

Manually developing end-to-end solutions for business users may be costly and resource intensive. This accelerator provides a no code Studio for users to quickly build complex, multi-stage AI pipelines across multiple Azure AI and ML Services. Users can select, and stack, AI/ML Services from across Azure Cognitive Services (Speech, Language, Form Recognizer, ReadAPI), Azure Machine Learning into a single, fully integrated pipeline. Integration between services is automated by BPA, and once deployed, a web app is created. This customizable UI* provides and drag-n-drop interface for end users to build multi service pipelines. Finally, the user-created pipeline is triggered as soon as the first input file(s) are uploaded, storing the results in a document database.

### Goals
* Understand key concepts of Form Recognizer and understand how to leverage BPA accelerator in conjunction with Form Recognizer and other services 


### Agenda 
1. Business Process Automation(BPA) Accelerator Overview, Capabilities and Usage
1. Develop and execute a simple pipeline with Form Recognizer pre-trained invoice model with BPA
    1. **Challenge 1:** Deploy Pre-trained Model
1. Analyze the output with Forms Recognizer Studio and Azure Search
1. Train a custom model using Form Recognizer Studio
1. Utilize the custom model in the BPA accelerator and analyze the output
   1. **Challenge 2:** Train & Deploy Custom Model



#### Audience
1. Data Scientists
1. Business Analysts
1. Data science Managers
1. AI specialists
1. ML Engineers

#### Challenge Instructions
1. [Deploy Pre-trained Model with BPA](lab_instructions/lab_1.md)
1. [Train and Deploy Custom Model](lab_instructions/lab_2.md)
