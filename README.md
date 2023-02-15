# Title
Fraud Insurance Claim Prediction

## Problem Statement
Quick Insurance Company (QIC) has been facing fraudulent claims for the past couple of years now. Because of this, 30% of their stuffs have been layed off. They accused these people for not paying enough attention when an individual files for a claim. Recently, they had a new CEO called Mr. Debrah. Just after he joined, someone made a fraudulent claim and the person succeded. After this incident, he relized that there has been more cases similar to this one. Enough is enough said Mr. Debrah, I have to put a stop to this act as soon as possible as the new CEO.

I have to contact King (Mr. Debrah's friend who is an IT expect). He called him and they meet later in the day to discuss the situation and measures to put inplace to help him prevent more fraudulent claims from happening in the near futer. I will get back to you said King. A few weeks later, King got back to him telling him of a solution he had in mind. He said, I could come up with a system that can help to detect fraud when someone tries to file for a claim. He explianed everything to Mr. Debrah who was very happy to hear of this new solution. He gave King permission to start as soon as possible by providing him with all the neccessary materials including datasets which contains fraudulent and non fraudulent claims made in the organization (requested by King). The `AIM` of this project is to build the system proposed by King to help Mr. Debrah detect fraudulent claims when a user files for one.

### Dev Environment On AWS Architecture Diagram
* A user makes a request to make prediction
* The request get routed to aws apigateway which get authorized to confirm if user has permission to access endpoint.
* API gateway sends the request to aws lambda function to make a prediction.
* AWS lambda function access s3 bucket to download model make prediction and send predicted output to client.

![aws diagram](./docs/images/all-aws.png)

### Staging Environment On GCP Architecture Diagram
* A user makes a request to make prediction
* The request get routed to gcp apigateway which get authorized to confirm if user has permission to access endpoint.
* API gateway sends the request to gcp cloudrun to make a prediction.
* GCP cloudrun access storage bucket to download model, make prediction and send predicted output to client.

![gcp diagram](./docs/images/gcp-all.png)

### Prod Environment On Azure Architecture Diagram
* A user makes a request to make prediction
* The request get routed to azure apimanager which get authorized to confirm if user has permission to access endpoint.
* API manager sends the request to azure containerapp to make prediction.
* Azure containerapp access storage account to download model, make prediction and send predicted output to client.

![azure diagram](./docs/images/azure-all.png)
