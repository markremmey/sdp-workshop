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
   1. To do this go to portal.azure.com from a web browser and click on resource group that is created for the purpose of this lab.
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
1. 
1. 
1. 

1. 
1. 