# Deploy Pre-trained Model with Business Process Automation Accelerator (BPA)

### Overview
In this lab, you will create a pipeline with the Business Process Automation Accelerator and utilize it to generate a JSON output in Azure Cosmos DB. We will create an indexer using search with this output and utilize the Sample Search Application within the BPA accelerator to search on specific aspects of the document.


### Goal
* Use a sample invoice document and utilize the BPA accelerator to use the Form Recognizer Pretrained Invoice Model
* Add an element that converts the invoice output to simpler format
* Run the pipeline with sample document and create a Search indexer of the simplified output 
* Utilize the Sample Search Application in the Accelerator to search on specific areas of the Invoice 


### Pre-requisites
* The accelerator is deployed and ready in the resource group
* You have access to sample invoices folder with the invoices to upload


### Instructions

1. Launch the accelerator from the resource group in the Static Web App
   1. To do this go to portal.azure.com ([Azure Portal](portal.azure.com)) from a web browser and click on resource group that is created for the purpose of this lab.
   ![resourcegroup.png](/images/resourcegroup.png)
    Click on the resource group that is created for this lab, you should be able to see resources deployed as a part of Business Process Automation accelerator deployment.
    
    > **Note :** The names will be different in your specific labs and will not exactly match with the names of the resources or resource group

    ![resourceswithinresourcegroup.png](/images/resourceswithinresourcegroup.png)

    1. Look for the Static Web App under **type**. This is what we will use as a part of lab 1. Click on the Web App.
    
    ![staticwebappresource.png](/images/staticwebappresource.png)

    Click on the URL and this will launch the accelerator
    ![swaurl.png](/images/swaurl.png)

1. This is the home page of the Accelerator. Click on Configure a new pipeline
    ![BPAHomepage.png](/images/BPAHomepage.png)

1. Give a name for the pipeline and click on create 
     ![createnewpipeline.png](/images/createnewpipeline.png)

1. Select **PDF Document**
    ![documenttype.png](/images/documenttype.png)

1. Select **Form Recognizer Prebuilt Invoice Model**.
    ![selectprebuiltinvoice.png](/images/selectprebuiltinvoice.png)

1. Select **Convert the Invoice Output to a Simpler Format** in the **Pipeline Preview** page
    ![selectconverttosimplerformat](/images/selectconverttosimplerformat.png)

1.  Scroll down the page if need be and click **Done**. This step creates the pipeline
    ![lab1pipelinefinalpage](/images/lab1pipelinefinalpage.png)

1. You should be able to see the pipeline created in page that loads next 
    ![lab1pipelinecreated.png](/images/lab1pipelinecreated.png)

1. The next step is to ingest documents into this pipeline. Click on **home** and select **Ingest Documents**
    ![home1.png](/images/home1.png)

    ![ingestdocuments.png](/images/ingestdocuments.png)

1. Select the pipeline you just created **first** from the dropdown and then drop documents from Sample Invoices folder. Use Sample 7 folder and drop a few documents from there.
    ![selectpipeline.png](/images/selectpipeline.png)
    You may see a prompt that there are some active documents being processed by the pipeline
    ![activesamplesprocessing.png](/images/activesamplesprocessing.png)

1. The results can be viewed in **Azure Cosmos DB Data Explorer**. To view the results, go to portal.azure.com ([Azure Portal](portal.azure.com)) again in your browser and get to the resource group like we did earlier in Step 1. There, in the resource group, click on the resource that is of type Azure Cosmos DB account
    ![cosmosdbtype.png](/images/cosmosdbtype.png)

    Go to Data Explorer
    ![cosmosdbdataexplorer.png](/images/cosmosdbdataexplorer.png)

    From there, go to items
    ![cosmosdbitem.png](/images/cosmosdbitem.png)

    Click on one of the items. This represents the output from the pipeline on the documents uploaded. Since we added the item in the pipeline  - **Convert the Invoice Output to a Simpler Format**, th output is simplified so we can create an indexer with **Search Service**.
    ![oneitemjson.png](/images/oneitemjson.png)
    
    Scroll through the results and check the output and compare with the invoice uploaded.

1. The get to **Search Service**. To view the results, go to portal.azure.com ([Azure Portal](portal.azure.com)) again in your browser and get to the resource group like we did earlier in Step 1. There, in the resource group, click on the resource that is of type Search Service. 
    
    ![searchservicetype.png](/images/searchservicetype.png)

1. 

1. 

1. 

1. 