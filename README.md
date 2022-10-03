# Azure DataFactory Code to validate POST using a dataflow

This supports issues raised in 

* https://feedback.azure.com/d365community/idea/188df145-1cd2-ec11-a81b-6045bd7ac9f9
* https://github.com/MicrosoftDocs/azure-docs/issues/87405

## Http Post Body is `null`

Results from ADF Dataflow shows the highlighted body is `null`

**Settings:**

<img width="701" alt="image" src="https://user-images.githubusercontent.com/91074239/193567804-6134f48f-e375-4aad-8a96-48aca5bf5098.png">

**Data Preview:**

<img width="1390" alt="image" src="https://user-images.githubusercontent.com/91074239/193567278-3b75d5f2-cf99-496f-a49e-403f43296ff6.png">

Results from Postman clearly shows body is not null but the above dataflow shows the columns/properties but their values are `null`

**Body** column not available in select

![image](https://user-images.githubusercontent.com/91074239/193569729-8a52c012-b5b5-4b18-8725-cccd64ced75a.png)

**PostMan** Response

<img width="718" alt="image" src="https://user-images.githubusercontent.com/91074239/193567242-95f7a0d9-a927-4292-9ee5-ecf1354510f7.png">
