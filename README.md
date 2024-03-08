# Cognitive Search in Microsoft Azure

[![License](https://img.shields.io/npm/l/react)](https://github.com/JadesonBruno/cognitive-search-in-microsoft-azure/blob/main/LICENSE)

This repository has the purpose of storing the project developed within the scope of the "Document Intelligence and Knowledge Mining" module of the "Microsoft Azure AI Fundamentals" Bootcamp by [DIO](https://www.dio.me/), under the instruction of the teacher [Valéria Baptista](https://www.linkedin.com/in/valeriabaptista/).

The project is an essential requirement for passing the "Document Intelligence and Knowledge Mining" module, consolidating participants practical learning and preparing them for subsequent challenges.

The development of this project aims to demonstrate how knowledge mining can be used in Microsoft Azure, creating Azure AI Search indexes alongside AI capabilities. For a better understanding, I divided the entire process into steps, from creating resources to obtaining insights with cognitive research.

## Problem Context 

Let’s imagine you work for Fourth Coffee, a national coffee chain. You’re asked to help build a knowledge mining solution that makes it easy to search for insights about customer experiences. You decide to build an Azure AI Search index using data extracted from customer reviews.

## Step 1: Creating a resource Azure AI Search

Inicialmente, precisamos acessar o portal do Azure: https://portal.azure.com/.

To start retrieving this information we need to create some resources, the first of which is Azure AI Search.

<p align="center">
  <img src="./assets/01_selecting_a_resource_azure_ai_search.gif" alt="Creating a Resourse Azure AI Search">
</p>

You need to fill in some information to create the resource.

<p align="center">
  <img src="./assets/02_configuring_azure_ai_search.png" alt="Configuring Azure AI Search">
</p>

After reviewing the resource, we can create.

<p align="center">
  <img src="./assets/03_creating_azure_ai_search.png" alt="Creating Azure AI Search">
</p>

After the deployment is complete, let's move on to the next step.

<p align="center">
  <img src="./assets/04_ai_search_deployment_complete.png" alt="Azure AI Search deployment complete">
</p>

## Step 2: Creating a resource Azure AI Service

Let's select the Azure AI Service resource.

<p align="center">
  <img src="./assets/05_selecting_ai_service.gif" alt="Selecting Azure AI Service">
</p>

You need to fill in some information to configure the feature.

<p align="center">
  <img src="./assets/06_configuring_ai_service.png" alt="Configuring Azure AI Service">
</p>

After reviewing the resource, we can create.

<p align="center">
  <img src="./assets/07_creating_ai_service.png" alt="Creating Azure AI Service">
</p>

After the deployment is complete, let's move on to the next step.

<p align="center">
  <img src="./assets/08_ai_service_deployment_complete.png" alt="Azure AI Service deployment complete">
</p>

## Step 3: Creating Storage Account

We need to create a storage account because it will provide us with a unique namespace for the data, it will contain all the data objects and from there we can integrate it with cognitive search.

Let's start by selecting a storage account.

<p align="center">
  <img src="./assets/09_selecting_storage_account.gif" alt="Selecting a Storage Account">
</p>

We need to fill in some information to create our storage account.

<p align="center">
  <img src="./assets/10_cofiguring_storage_account.png" alt="Selecting a Storage Account">
</p>

After reviewing the resource, we can create.

<p align="center">
  <img src="./assets/11_creating_storage_account.png" alt="Selecting a Storage Account">
</p>

After the deployment is complete, we go to the next step, clicking on "Go to Resource".

<p align="center">
  <img src="./assets/12_storage_account_deployment_complete.png" alt="Storage Account Deployment Complete">
</p>

## Step 4: Configuring the created storage account

We will need to allow anonymous Blob access.

<p align="center">
  <img src="./assets/13_allow_anonymous_blob_access.gif" alt="Allow anonymous Blob acess">
</p>

## Step 5: Create a new container within our storage account

You will need to Create a new container within our storage account.

<p align="center">
  <img src="./assets/14_creating_new_container.gif" alt="Creating a new container">
</p>

## Step 6: Import the data into the container

Let's access the created container and upload the files present in the repository input to the [review-coffee](./inputs/review-coffee/) folder.

<p align="center">
  <img src="./assets/15_upload_files_in_container.png" alt="Upload files in container">
</p>

<p align="center">
  <img src="./assets/16_upload_complete.png" alt="Upload complete">
</p>

## Step 7: Import the data into Azure AI Search

You will need to import the data into Azure AI Search via Azure Blop Storage.

<p align="center">
  <img src="./assets/17_import_data_into_ai_search.gif" alt="Import data into Azure AI Search">
</p>

## Step 8: Connect to your data

You need to fill in some information to configure data import into Azure AI Search via Azure Blob Storage.

<p align="center">
  <img src="./assets/18_connect_to_your_data.png" alt="Connect to your data">
</p>

## Step 9: Add coginitive skills

Filling in the field "Attach AI Services".

<p align="center">
  <img src="./assets/19_attach_ai_services.png" alt="Attach AI Services">
</p>

Filling in the field "Add enrichments".

<p align="center">
  <img src="./assets/20_add_enrichments.png" alt="Add enrichments">
</p>

Filling in the field "Save enrichments to a knowledge store".

<p align="center">
  <img src="./assets/21_error_connection_string.png" alt="Error connection string">
</p>

If an error occurs in storage account connection string, we will need to create a new container.

<p align="center">
  <img src="./assets/22_creating_new_private_container.gif" alt="Creating New Private Container">
</p>

Once the new private container has been created, we can move on to the next step.

<p align="center">
  <img src="./assets/23_save_enrichments_to_a_knowledge_store.png" alt="Save enrichments to a knowledge store">
</p>

## Step 10: Customize target index

<p align="center">
  <img src="./assets/24_customize_target_index_1.png" alt="Customize target index 1">
</p>

<p align="center">
  <img src="./assets/25_customize_target_index_2.png" alt="Customize target index 2">
</p>

## Step 11: Create an indexer

<p align="center">
  <img src="./assets/26_create_an_indexer.png" alt="Create an indexer">
</p>

## Step 12: View the indexer

<p align="center">
  <img src="./assets/27_view_the_index.gif" alt="View the index">
</p>

## Step 13: Query the index

Use the Search explorer to write and test queries. Search explorer is a tool built into the Azure portal that gives you an easy way to validate the quality of your search index. You can use Search explorer to write queries and review results in JSON.

<p align="center">
  <img src="./assets/28_query_the_index.gif" alt="View the index">
</p>

Let's start by analyzing whether the query string is available.

Code for querying in json format: [query_string_on](./inputs/queries/query_string_on.json).

<p align="center">
  <img src="./assets/29_query_string_on.png" alt="Query string on">
</p>

Result in json format: [result_query_string_on](./outputs/result_query_string_on.json).

Now let's filter queries by location in Chicago.

Code for querying in json format: [query_locations_chicago](./inputs/queries/query_locations_chicago.json).

<p align="center">
  <img src="./assets/30_query_locations_chicago.png" alt="Locations Chicago">
</p>

Result in json format: [result_query_locations_chicago](./outputs/result_query_locations_chicago.json).

Let's run a query based on a **negative** sentiment analysis.

Code for querying in json format: [query_negative_sentiment](./inputs/queries/query_negative_sentiment.json).

<p align="center">
  <img src="./assets/31_query_negative_sentiment.png" alt="Negative Sentiment">
</p>

Result in json format: [result_query_negative_sentiment](./outputs/result_query_negative_sentiment.json).

## Useful Links:

[Microsoft Azure AI Fundamentals: Document Intelligence and Knowledge Mining](https://learn.microsoft.com/en-us/training/paths/document-intelligence-knowledge-mining/)

[Explore an Azure AI Search index](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)


## Tecnologias Utilizadas

- Microsoft Azure AI Search
- Microsoft Azure AI Service
- Microsoft Azure Storage Accounts (Containers, Blop Storage)

## Contributions

Contributions are welcome. Feel free to suggest improvements and possible fixes to the code through an issue or pull requests.

## Author

Jadeson Bruno Albuquerque da Silva

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jadeson-silva/)