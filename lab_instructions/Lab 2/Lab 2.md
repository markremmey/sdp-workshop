# Use Azure OpenAI with your own data

### Overview
In this lab, you will be using your own data with Azure OpenAI Large Language Models(LLM) which will be made searchable using Azure Cognitive Search. You will be using the Porche Owner's Manual pdf provided under [Lab 2](/SampleInvoices/Lab%202/) folder.


### Goal
* How to leverage the chatGPT LLM to extract concise summary from your own document repository using OpenAI.

### Pre-requisites
* Access to Azure OpenAI chat playground
* Sample data to test with OpenAI

### Instructions

### Step 1: Navigate to Azure OpenAI Playground

![Alt text](images/image.png)

* 1.1 Click on **"Go to Azure OpenAI Studio"**

![Alt text](images/image-1.png)

* 1.2 Click on **"Bring your own data"**

![Alt text](images/image-2.png)

### Step 2: Upload your own data
In this step, we will be using Porche's owner manual for Taycan, Panamera and Cayenne models.

* 2.1 Select the following options for adding the data source pop-up:
    * 2.1.1 Select data source: Upload files
    * 2.1.2 Select Azure Blob storage resource: Choose the already created storage account from the dropdown. If asked, enable CORS.
    * 2.1.3 Select Azure Cognitive Search resource: Select the search service used in the previous lab from the dropdown.
    * 2.1.4 Enter the index name: Give an index name e.g aoaiworkshop
    * 2.1.5 Check the acknowledgement and click Next.

![Alt text](images/image-3.png)

* 2.2 Click on Browse for a file and select the Porche Owner Manual pdf and click Upload files and Next. You can select multiple files as well.

![Alt text](images/image-4.png)

* 2.3 Click on Save and close

![Alt text](images/image-5.png)

### Step 3: Interact with Azure OpenAI chatGPT LLM using your own data

* 3.1 Under the Assistant Setup pane, wait until your data upload is finished

![Alt text](images/image-6.png)

* 3.2 Under the Chat Session pane, you can start testing out your prompts as shown in the figure below

![Alt text](images/image-7.png)

* 3.3 You can also configure the responses of your bot by selecting the system message under Assistance Setup. Here we have edited the default system message.

![Alt text](images/image-9.png)

* 3.4 Click on Continue

![Alt text](images/image-10.png)

![Alt text](images/image-11.png)

* 3.5 In Configuration pane, you can try and experiment with different parameter configuration to see how it changes the behavior of the model

![Alt text](images/image-8.png)