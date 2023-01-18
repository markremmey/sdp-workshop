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
1 - Create Form Recognizer Resource  
![](images/step1a-create-form-rec-resource.png)  
![](images/step1b-create-form-rec-resource.png)  
![](images/step1c-create-form-rec-resource.png)  
![](images/step2a-Create-custom-labeling-project.png)  
![](images/step2b-Create-custom-labeling-project.png)  
![](images/step2c-Create-custom-labeling-project.png)  
![](images/step2d-Create-custom-labeling-project.png)  
![](images/step2e-Create-custom-labeling-project.png)  
![](images/step2f-Create-custom-labeling-project.png)  
![](images/step2g-Create-custom-labeling-project.png)  
![](images/step3a-import-sample-data.png)  
![](images/step3b-import-sample-data.png)  
![](images/step3c-import-sample-data.png)  
![](images/step3d-import-sample-data.png)  
![](images/step3e-import-sample-data.png)  
![](images/step3f-import-sample-data.png)  
![](images/step4a-train-the-model.png)  
![](images/step4b-train-the-model.png)  
![](images/step5a-test-the-model.png)  
![](images/step5b-test-the-model.png)  
![](images/step5c-test-the-model.png)  
![](images/step5d-test-the-model.png)  

