# Creating a Chatbot

**Project Overview: Building a Chatbot for Website** 

## Introduction:

This is a high level overview of the steps needed to create a chatbot. Organizations are increasinly looking to add a chatbot to their site for a more enjoyable customer experience. This chatbat can also help drive analytics as to what the customers are looking for from the organization.

The quick setup would be to gather the data from a website or documents that the organization wants to make available for the users to interact with and import that info into a DB.

The solution would consist of a front-end application to ingest the data into DB and a second a second front-end that the customers can use to interact with the data.

**The following are the high level steps needed to complete the tasks.**

## Pre-requasites:
1. Determing H/A, RTO, RPO and build the solution accordingly. A local install may have a higher H/A, RTO and RPO than a cloud solution. Database access maybe slower locally than in the cloud. The customer experience could be hindered by a slow response time on a local installation. 
2. Local or cloud - determine what DB to use. 
3. Local or cloud - Create DB table with approrpiate access from front-end application

## Data Collection:
1. Gather all of the information from the website or documents to be consumed (PDFs, CSV, HTML, etc). The data type and location will determine what the best tools to use for this step.
2. Review the data to determine a folder structure.

## Front-end for Data Ingestion:
1. Create a front-end website to ingest the data possibly using streamlit or any other application for data ingestion.
    * Ingested data will save files to specific folders either in the cloud or locally based on content.
    * Ingestion process will input data into preconfrigured DB.
2. Start importing data.

## Chatbot Integration (Second Front-End Instance):
1. Requirements Gathering:
    * Determine specific requirements for the chatbot - local or commercial.
    * If commercial, is there a preference on the model (ChatGPT, Claude, Bard, etc.)
    * If local extensive testing and research must be done to determine if the model will behave as expected. Also, can the training data for the local model be determined to help determine if the model is biased in it's responses.
    * Does the chatbot require a personality type?
2. Prompt Engineering:
    * Based on requirements, prompts will be created to guide the user in their search for answers.
    * Based upon the prompts, the relevent data on the DB will be queried with the Large Language Model (LLM) to return the expected results.
3. Guardrails and Data Usage:
    * Guardrails will be established to prevent the chatbot from generating irrelevant or incorrect responses.
    * Only answered derived from the ingested data will be used to answer the user queries.

## Testing and Deployment:
1. Review data and ask it questions that should only be available from the ingested data. Verify answers with ingested data.
2. Reply with error message when data does not exist in the ingested data to answer the specific data (no hullicinations).
    * Provide examples of questions that it can answer based on ingested data.

## Maintenance and Scaling:
1. Import new data as it becomes available.
2. Update prompts if new data extends beyond the initial bounderies of the ingested data.
3. Design the front-end/back-end infrastructure to leverage cloud providers ability to scale to meet increased demand and reduce when demand subsides. If installed locally, use onprem tools to adjust the environment accordingly.

## Documentation:
It is important to retain up to date documentation on the existing solution. Documentation should include the following:
1. Diagrams showing the process flow of the application. 
2. Versions of applications being used.
3. Troubleshooting guide.
4. Disaster recovery runbook.

## Conclusion:

A well documented solution will lead to an easier time maintaining the solution regardless of who takes ownership of it. This extends the life of the application and allows for modifications as long as the documentation is kept up to date.


