---
draft: true
---
# Our Step-by-Step Guide to Generating Software Development Costs with AI
Right now determining software development estimates is more of an art than science. This guide aims to standardize the process for generating software development costs for [DevToDollars](https://devtodollars.com). Feel free to use our process to determine your software costs!
## 1. Gathering Business Requirements
The first step to figuring the software development costs is by getting on a call with the client and understanding their needs. Below are a list of questions you should have answered by the end of the call.

- How will this software help you and/or what problem does it solve?
- Who are the users and what are their needs / goals?
- What's the current workflow for each user?
- What are the core features and functionalities needed?

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

## 3. Create the User Stories
After compiling your findings, the next task is to create the user stories. User stories are essentially features written from the perspective of the end user. You will use AI to create the user stories based on the findings compiled above. Below is the prompt you will use:

```
You are an experienced startup CTO. Your task is to create a comprehensive bullet list of user stories needed to complete the MVP based on the my needs below. 
```

Here is an example of what you will send to ChatGPT (or Claude):
```
You are an experienced startup CTO. Your task is to create a comprehensive bullet list of user stories needed to complete the MVP based on the my needs below. 

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

## 4. Create the Time Estimation
If you are satisfied with the user stories generated from the prompt above, the next step is to create the time estimations from each user story. **In the same chat**, paste the following prompt below.

```
Based on the user stories, estimate the amount of time it takes a full stack developer to complete each user story (including extra time for additional complexities) split the hours into "frontend hours" and "backend hours". Return the results in a table with the last row being the total time estimate.
```

Below is an example of the estimated time estimations:
```
TODO: Add time estimations here
```
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

---

If you're someone looking to hire a developer, I'd be more than happy to help you look over your estimate. If you're interested, [feel free to book a call with me here](https://usemotion.com/meet/ithinkwong/xyz6xw9?d=30).

I do want to stress that I understand our costs may not be a right for everyone. 