# Description

![Alt text](assets/1.png)

We have a user prompt and before we feed it to the LLM, we go against a vector DB (retrieval) and we’re going to do a semantic search against our corpus (private documents or more up-to-date info). We’re goingbto retrieve documents via a vectorDB search and combine it into our prompt and feed that to our LLM and then the LLM is going to use both our original prompt and this retrieved info and generate a user response.

# Steps

First let's create a Resource group:

![Alt text](assets/2.png)

The create a storage account in the same resource group:

![Alt text](assets/3.png)

Rest of parameters as default

Let’s create a container and go to Kaggle Netflix Movies and TV Shows and download the csv file and this what we’re going to place in our storage container in Azure:

![Alt text](assets/4.png)

![Alt text](assets/5.png)

Now create the storage account where we’re going to store our data. We’re going to create it in a container:

![Alt text](assets/6.png)

Now let’s create an AI Foundry resource in the same resource group:

![Alt text](assets/7.png)

Rest of paramters as default

Go to AI Foundry portal. Deploy base model and select model text-embedding-3-large

![Alt text](assets/8.png)

Go to AI service and Create a search service:

![Alt text](assets/9.png)

Import and vectorize data, Azure Blob storage, RAG:

![Alt text](assets/10.png)

![Alt text](assets/11.png)

Rest of parameters as default

Go to chat playground, model catalog, gpt-4o:

![Alt text](assets/12.png)

Select data source, azure blob storage

![Alt text](assets/13.png)

In Data connection, get API key

# Results

Now go to chat playground and ask a question. then check it in the csv file

![Alt text](assets/14.png)

![Alt text](assets/15.png)

and the recommendations are inside the csv file! It works!!

We try with another example:

![Alt text](assets/16.png)

Let’s check in the csv:

![Alt text](assets/17.png)

And it's there too! Amazing!!
