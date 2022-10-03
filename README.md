# Azure DataFactory Code to validate POST using a dataflow

This supports issues raised in 

* https://feedback.azure.com/d365community/idea/188df145-1cd2-ec11-a81b-6045bd7ac9f9
* https://github.com/MicrosoftDocs/azure-docs/issues/87405

## The issue

When making a HTTP `post` using ["External call transformation"](https://learn.microsoft.com/en-us/azure/data-factory/data-flow-external-call), 

* the response `body` is contains the properties but values are `null`
* the `body` column can't be selected using [select](https://learn.microsoft.com/en-us/azure/data-factory/data-flow-select) activity

### Additional details

Configuring, the external call activity as below 
<img width="701" alt="image" src="https://user-images.githubusercontent.com/91074239/193567804-6134f48f-e375-4aad-8a96-48aca5bf5098.png">

The resulting **data-preview** shows the properties from the response i.e. `origin` / `url` but their values are `null`

<img width="1390" alt="image" src="https://user-images.githubusercontent.com/91074239/193567278-3b75d5f2-cf99-496f-a49e-403f43296ff6.png">

Subsequently, trying to [select](https://learn.microsoft.com/en-us/azure/data-factory/data-flow-select) the `body` column isn't possible. 

![image](https://user-images.githubusercontent.com/91074239/193569729-8a52c012-b5b5-4b18-8725-cccd64ced75a.png)

## PostMan response

<img width="718" alt="image" src="https://user-images.githubusercontent.com/91074239/193567242-95f7a0d9-a927-4292-9ee5-ecf1354510f7.png">
