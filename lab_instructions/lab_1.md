# Deploy Pre-trained Model with Business Process Automation Accelerator (BPA)

### Overview
In this lab, you will create a pipeline with the Business Process Automation Accelerator and utilize it to generate a JSON output in Azure Cosmos DB. We will create an indexer using search with this output and utilize the Sample Search Application within the BPA accelerator to search on specific aspects of the document.


### Goal
* Use a sample invoice document and utilize the BPA accelerator to use the Form Recognizer Pretrained Invoice Model
* Add an element that converts the invoice output to simpler format
* Run the pipeline with sample document and create a Search indexer of the simplified output 
* Utilize the Sample Search Application in the Accelerator to search on specific areas of the Invoice 
* Utilize a pipeline to create Table index and use that in the Sample Search Application


### Pre-requisites
* The accelerator is deployed and ready in the resource group
* You have access to sample invoices folder with the invoices to upload


### Instructions

##### Part 1

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

1. The get to **Search Service**. To view the results, go to portal.azure.com ([Azure Portal](portal.azure.com)) again in your browser and get to the resource group like we did earlier in Step 1. There, in the resource group, click on the resource that is of type **Search Service**. 
    
    ![searchservicetype.png](/images/searchservicetype.png)

1. Click on **Import Data**. 
    ![selectimportdata.png](/images/selectimportdata.png)

1. Select **Azure Cosmos DB** from the dropdown in datasource.
    ![selectazurecosmosdb.png](/images/selectazurecosmosdb.png)

1. Provide a name for datasource and click on **Choose an existing connection**  for **Connection String**. Here the Azure CosmosDB resource created as a part of BPA accelerator already setup will be one of the sources you can choose from.
    ![selectcosmosdb.png](/images/selectcosmosdb.png)


1. Keep the default for **Managed identity Authentication**, which is **None**. For **Databases** and **Collection** use the dropdown to select the same name as the Cosmos DB you selected at step 15. 

1. Under Query, use the following Query.  The pipeline should match the pipeline name you used in step 3
    > SELECT * from c WHERE c.id != 'pipelines' AND c.id != 'cogsearch'  AND c.pipeline = 'lab1pipeline' AND c._ts >= @HighWaterMark ORDER by c._ts

    ![importdata.png](/images/importdata.png)

1. Click **Next: Add cognitive skills (Optional)**. This validates and creates the index schema. 

1. In the next Screen(**Add cognitive skills (Optional)**), Click **Skip to: Customize Target Index**, 
      ![customizetargetindex.png](/images/customizetargetindex.png)

1. In the next screen, under **aggregated results**, click on the **...** on **invoice**, click **delete** . Similarly, you can also delete **resultindexes**
    ![deleteinvoice.png](/images/deleteinvoice.png)

1. Make all fields **Retrievable** and **Searchable**
    ![Retrievable.png](/images/Retrievable.png)

1. Under **aggregatedResults**-> **simplifyInvoice** Select, customerName, invoiceId, invoicedate and dueDate to be filterable and sortable
    ![simplifyinvoicefiltersort.png](/images/simplifyinvoicefiltersort.png)


1. Similarly, under **aggregatedResults**-> **items**, select all fields to be filterable and sortable.
    ![itemsfileterableandsortable.png](/images/itemsfileterableandsortable.png)

1. Provide a name for the Index and click on **Next: Create an indexer**
    ![indexname.png](/images/indexname.png)

1. Provide a name for the indexer and click **Submit**
    
    ![createindexer.png](/images/createindexer.png)

1. You will get a notification that the import is successfully configured

1. Now, go back to the accelerator url that you retreived from Step 1 and click on **Sample Search Application**.  
    ![samplesearchapplication.png](/images/samplesearchapplication.png)

    This opens the same search application
     ![searchlandingpage.png](/images/searchlandingpage.png)

1. You can now filter and search on items and other fields configured.


#### Part 2
We can extend this lab further by using Form Recognizer Layout Service and check how we can retrieve information in the form of tables using Azure Cognitive Search.

1. Create a new pipeline using the layout service and extract information for table search. The steps will be similar to Steps 1-8 in **Part 1** that you just did. The pipeline page before you click **Done** at Step 7 should like like the screen shot below:
     ![pipelinetablesearch.png](/images/pipelinetablesearch.png)

1. Next step would be to ingest documents in the pipeline similar to steps 9-11 in part 1 but use the pipeline created as a part of this exercise.

1. Now, we need to configure **Search Service** for table search. This can be configured similar to steps 12-17. The Query will be slightly different from what we used in step 17 and also make sure the pipeline is the name of the pipeline created for this step. Note that this query filters for **table** type 

    > SELECT * from c WHERE c.id != 'pipelines' AND c.id != 'cogsearch'  AND c.pipeline = 'lab1table' AND c.type = 'table' AND c._ts >= @HighWaterMark ORDER by c._ts

1. Follow steps 18-19 as before and when you get to **Customize target index** section, give the index a name that helps identify that it is a table index and then make all fields **Searchable** and **Retrievable** and the table data and id **Filterable** and **Facetable**. 
    ![tableindexoptions.png](/images/tableindexoptions.png)

1. Follow steps 24-25 and once you get a notification after clicking **Submit**, you can follow step 27 to open the **Sample Search Application** 

1. Here, select the index created as a part of this exercise and also enable **Table Search**
    ![tablesearch.png](/images/tablesearch.png)

1.  Explore this UI, eg, table search configuration and filter and search on specific items to get more insights.
