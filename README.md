 
# Cosmos DB Scenario Based Demos and Labs

## Tweaks to the Original Repo
In order to deploy to Azure Government, some tweaks to the repository had to be made.

- Because the button for running the deployment scripts redirects to Commercial Azure, You will need to create a custom deployment and run a modified version of the ARM template. Modify the template to include valid government regions instead of the commercial ones that are set as defaults within the parameters as well as updating the allowedValues to include government ones.
- Make sure the api versions are updated to versions currently supported by Azure Government.
- Make sure Microsoft.Sql Resource Provider is registered under the appropiate subscription.
- Updating Endpoints and Urls to point to Azure Government versions.
- Add Key Vault Access Policies for Managed Identities with RBAC as Key Vault Secrets User for the function apps, web app, and synapse workspace and then add yourself as a Key Vault Administrator during configuration of the environment. 
  
This repo contains easy to deploy demos and detailed labs that show how to build end-to-end solutions for specific scenarios atop a common architecture that centers around Azure Cosmos DB.  

- **Demo**: The intent of the demo is to enable users to quickly get to showing an end-to-end solution working in their subscription, getting at the capabilities of Cosmos DB in the context of each of the scenario. It provides automation for deployment and minimizes any time spent manually configuring or provisioning resources in the target Azure subscription.

- **Labs:** The intent of the lab is to take participants step by step thru the setup and deployment of the key components of the solution deployed in the demo, providing guidance, teaching best practices and linking out to additional resources along the way.

##  Scenario 1 - Internet of Things (IoT)

In this scenario, you will use Azure Cosmos DB to ingest streaming vehicle telemetry data as the entry point to a near real-time analytics pipeline built on Cosmos DB, Azure Functions, Event Hubs, Azure Databricks, Azure Storage, Azure Stream Analytics, Power BI, Azure Web Apps, and Logic Apps.

Both a demo and a hands-on lab are available. See the [IoT README](./IoT/README.md), [Deployment](./IoT/README.md#deployment) section for details and how to get started for either the demo or the hands-on lab.

##  Scenario 2 - Retail Recommendation System for e-Commerce

In this scenario, you will  implement a recommendation system for e-commerce using several Microsoft Azure services including Cosmos DB, Azure Functions, Event Hubs, Azure Databricks, Azure Storage, Azure Stream Analytics, Power BI, Azure Web Apps, and Logic Apps.

### Retail demo

Follow the [step by step demo guide](./Retail/Demo%20step-by-step%20-%20Cosmos%20DB%20scenario-based%20demo%20-%20Retail.md) for instructions on how to deploy the demo, and for a script that will help you understand the key points showcased. 


### Retail hands-on lab

The lab guides consists of two documents:

- Complete the [before the hands-on lab setup guide](./Retail/Before%20the%20HOL%20-%20Cosmos%20DB%20scenario-based%20labs%20-%20Retail.md) to understand the requirements and to get setup to run the lab in your own environment.
- Follow the [hands-on lab step-by-step guide](./Retail/HOL%20step-by-step%20-%20Cosmos%20DB%20scenario-based%20labs%20-%20Retail.md) to get hands on constructing key components of the solution at your own pace.
