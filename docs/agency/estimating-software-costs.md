---
title: Our Step-by-Step Guide to Estimating Software Development Costs with AI
sidebar_label: Estimating Software Costs
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
- Additional Questions: Competitors? Software Platform? Timeline?

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
You are a seasoned startup CTO tasked with drafting user stories for an MVP. Below are the specific needs for the project. Create a comprehensive bullet list of user stories omitting generic elements like UI/UX, security, or testing.
```

Here is an example of what you will send to ChatGPT (or Claude):
```
You are a seasoned startup CTO tasked with drafting user stories for an MVP. Below are the specific needs for the project. Create a comprehensive bullet list of user stories omitting generic elements like UI/UX, security, or testing.

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
Based on the user stories, estimate the amount of time it takes a full stack developer to complete each user story including extra time for additional complexities. Return the results in a table with the last row being the total time estimate with the folowing columns:
- User Story
- Frontend Hours: Involve designing and implementing the user interface, ensuring responsiveness, and integrating with backend APIs.
- Backend Hours: Include setting up the server, database, API development, AI integration, and security implementations
- Total Hours: Sum of frontend and backend hours
```

Below is an example of the estimated time estimations (using GPT-4):

| User Story                         | Frontend Hours | Backend Hours | Total Hours |
|------------------------------------|----------------|---------------|-------------|
| **Initial Onboarding**             | 12             | 8             | 20          |
| **Business Requirements Input**    | 16             | 24            | 40          |
| **AI-driven Cost Estimation**      | 8              | 32            | 40          |
| **Reviewing Cost Estimates**       | 12             | 16            | 28          |
| **Receiving Cost Estimations via Email** | 8          | 12            | 20          |
| **Revising Requirements**          | 10             | 18            | 28          |
| **Mobile-Friendly Access**         | 16             | 8             | 24          |
| **User Feedback**                  | 6              | 10            | 16          |
| **Total**                          | 88             | 128           | 216         |

## 5. Inspect the Generated Cost Estimation
Of course, we're not going to blindly trust AI with the estimations. After generating the estimations, inspect the estimations and make sure to make adjustments to what makes sense. At this point, feel free to add missing stories or subtract user stories that don't make sense.

## 6. Determine the Total Cost
Now that you know the hours, it's not too difficult to figure out the cost to build the project. At DevToDollars, we charge $80 / hour. Multiply the rate but the total hours to determine the costs. For the project above, the total cost would be $17280.

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
If you're someone looking to hire a developer, I'd be more than happy to help you look over your estimate. [Feel free to book a call with me here](https://usemotion.com/meet/ithinkwong/xyz6xw9?d=30).
:::