---
title: Our Step-by-Step Guide to Estimating Software Development Costs with AI
label: Estimating Software Costs
description: This guide aims to standardize the process for generating software development costs for DevToDollars
date: 2024-07-14
authors:
  - name: Matthew Wong
    title: Founder
    url: https://twitter.com/IThinkWong
    image_url: https://github.com/matthewwong525.png
---
Right now determining software development estimates is more of an art than science. This guide aims to standardize the process for generating software development costs for [DevToDollars](https://devtodollars.com). Feel free to use our process to determine your software costs!
## 1. Gathering Business Requirements
The first step to figuring the software development costs is by getting on a call with the client and understanding their needs. Below are a list of questions you should have answered by the end of the call.

- How will this software help you and/or what problem does it solve?
- Who are the users and what are their needs / goals?
- What's the current workflow for each user?
- What are the core features and functionalities needed?
- Additional Questions: Competitors? Software Platform?

:::note
An important part of your job is to cut complexity in the clients' work. We want to ensure we don't build things that they don't need.
:::

## 2. Compile Your Findings
After answering the following gathering the business requirements above, the next step is to compile your rough meeting notes into something concise for ChatGPT to ingest. Fill in the bullet points below with your findings:

```
Business Goals & Problem:
- 

Users and Needs & Goals:
- 

Current Workflow:
- 

Core Features & Functionalities:
- 

Additional Important Notes:
- 
```

As an example, here is the level of detail that makes sense:
```
Business Goals & Problem:
- Goal: Is to create a tool to help automatically create accurate software development cost estimates
- Problem: Right now non-technical clients looking for custom software need to spend a lot of time speaking with different software vendors to find out an accurate cost estimation. Also, it's hard for them to trust the development agency as the development agency to scope their project as they are incentivized to give higher estimations.

Users and Needs & Goals:
- Non-technical client that requires software: they need custom software to make current processes more efficient. Their goal is to use the software as a software to drive business.

Current Workflow for each User:
- Right now a non-technical client needs to speak with multiple vendors to get a reliable quote. They setup the call, explain their process to the development agency and the development agency comes back with a quote. Once they have multiple quotes they go through each one, they go through each one and decide who to move forward with based on their requirements. 

Core Features & Functionalities:
- An AI chat to help determine the client determine the business requirements
- AI to determine the software development costs from the business requirements
- Collect email to send out the cost estimation.
- Great UX to make it easy for the client to get their cost estimations. 

Additional Important Notes:
- This should be a web app that is mobile friendly.
```

## 3. Create the User Stories
After compiling your findings, the next task is to create the user stories. User stories are essentially features written from the perspective of the end user. You will use AI to create the user stories based on the findings compiled above. Below is the prompt you will use:

```
You are an experienced startup CTO. Your task is to create a detailed bullet list of user stories needed to complete the MVP based on the my needs below. 
```

Here is an example of what you will send to ChatGPT (or Claude):
```
You are an experienced startup CTO. Your task is to create a detailed bullet list of user stories needed to complete the MVP based on the needs below. 

Business Goals & Problem:
- Goal: Is to create a tool to help automatically create accurate software development cost estimates
- Problem: Right now non-technical clients looking for custom software need to spend a lot of time speaking with different software vendors to find out an accurate cost estimation. Also, it's hard for them to trust the development agency as the development agency to scope their project as they are incentivized to give higher estimations.

Users and Needs & Goals:
- Non-technical client that requires software: they need custom software to make current processes more efficient. Their goal is to use the software as a software to drive business.

Current Workflow for each User:
- Right now a non-technical client needs to speak with multiple vendors to get a reliable quote. They setup the call, explain their process to the development agency and the development agency comes back with a quote. Once they have multiple quotes they go through each one, they go through each one and decide who to move forward with based on their requirements. 

Core Features & Functionalities:
- An AI chat to help determine the client determine the business requirements
- AI to determine the software development costs from the business requirements
- Collect email to send out the cost estimation.
- Great UX to make it easy for the client to get their cost estimations. 

Additional Important Notes:
- This should be a web app that is mobile friendly.
```

## 4. Create the Time Estimation
If you are satisfied with the user stories generated from the prompt above, the next step is to create the time estimations from each user story. **In the same chat**, paste the following prompt below.

```
Based on the user stories, estimate the amount of time it takes a full stack developer to complete each user story (including extra time for additional complexities) split the hours into "frontend hours" and "backend hours". Return the results in a table with the last row being the total time estimate.
```

Below is an example of the estimated time estimations (using GPT-4o):

| User Story                                      | Frontend Hours | Backend Hours | Total Hours |
|-------------------------------------------------|----------------|---------------|-------------|
| **User Registration and Authentication**        |                |               |             |
| Sign up                                         | 6              | 8             | 14          |
| Log in                                          | 4              | 6             | 10          |
| **User Profile Management**                     |                |               |             |
| Update profile information                      | 5              | 7             | 12          |
| **Requirement Collection**                      |                |               |             |
| AI chat interaction to describe business needs  | 10             | 12            | 22          |
| AI to ask clear questions                       | 8              | 10            | 18          |
| Review and edit collected requirements          | 6              | 8             | 14          |
| **Cost Estimation**                             |                |               |             |
| Analyze business requirements for cost estimate | 5              | 15            | 20          |
| Explain factors affecting cost                  | 3              | 7             | 10          |
| Detailed breakdown sent via email               | 2              | 6             | 8           |
| **UX/UI**                                       |                |               |             |
| Intuitive interface                             | 15             | 8             | 23          |
| Mobile-friendly web app                         | 10             | 5             | 15          |
| **AI Chat Interaction**                         |                |               |             |
| Friendly greeting and introduction              | 4              | 6             | 10          |
| Structured questions to gather requirements     | 5              | 10            | 15          |
| Provide clarifications and examples             | 4              | 8             | 12          |
| **Requirement Analysis**                        |                |               |             |
| Process and extract key requirements            | 3              | 12            | 15          |
| Flag incomplete or ambiguous requirements       | 2              | 8             | 10          |
| **Cost Estimation Engine**                      |                |               |             |
| Analyze requirements and calculate cost         | 4              | 15            | 19          |
| Generate detailed cost breakdown                | 3              | 10            | 13          |
| Present cost breakdown clearly                  | 5              | 6             | 11          |
| **Email System**                                |                |               |             |
| Collect client email address                    | 3              | 5             | 8           |
| Send cost estimation email                      | 2              | 6             | 8           |
| **Additional Functionalities**                  |                |               |             |
| View project history                            | 5              | 10            | 15          |
| Provide feedback mechanism                      | 6              | 8             | 14          |
| **Security**                                    |                |               |             |
| Ensure data security                            | 2              | 10            | 12          |
| **Total Time Estimate**                         | **133**        | **196**       | **329**     |

## 5. Inspect the Generated Cost Estimation
Of course, we're not going to blindly trust AI with the estimations. After generating the estimations, inspect the estimations and make sure to make adjustments to what makes sense. At this point, feel free to add missing stories or subtract user stories that don't make sense.

## 6. Determine the Total Cost
Now that you know the hours, it's not too difficult to figure out the cost to build the project. At DevToDollars, we charge $80 / hour. Multiply the rate but the total hours to determine the costs.

But if you're looking to hire someone elsewhere, use the below table as a rough estimation to determine your costs:

| Type of Developer           | Location                    | Hourly Rate Range (USD) |
| --------------------------- | --------------------------- | ----------------------- |
| Offshore Freelancer         | India, Ukraine, Philippines | $15 - $50               |
| Local/Western Freelancer    | USA, Canada, Western Europe | $50 - $150              |
| Software Development Agency | Global                      | $50 - $100              |
| Large Agency/Consultancy    | USA, UK, Western Europe     | $100 - $300             |
## 7. Send the Estimate to the Client
Now that you've determined the cost, compile all the information into a contract and send this information to the client. 

:::note
If you're someone looking to hire a developer, I'd be more than happy to help you look over your estimate. If you're interested, [feel free to book a call with me here](https://usemotion.com/meet/ithinkwong/xyz6xw9?d=30).
:::