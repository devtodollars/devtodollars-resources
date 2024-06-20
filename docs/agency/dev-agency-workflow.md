---
title: Dev Agency Workflow
description: 
date: 2024-06-20
authors:
  - name: Matthew Wong
    title: Founder
    url: https://twitter.com/IThinkWong
    image_url: https://github.com/matthewwong525.png
draft: false
---
Below are step-by-step instructions on what to do when working with the client

## 1. Requirements
Setup a call with the client and get an understanding of their idea. Below are the minimum things you should understand:
- Problem they are trying to solve
- Current workflow of the user
- Core features they want
- Software platforms they need. This includes responsiveness like (web desktop or web mobile, etc.)
- Competitors that they have and what makes them special.
- The solution that they have in mind.

Once we figure this out we talk with them and try to reduce the scope of work. Like do we really need X or Y feature or can we get away with this or that. 

## 2. Design
The way to do design is to use a component library either [shadcn](https://ui.shadcn.com/) (for NextJS) or [Material 3](https://m3.material.io/) (for Flutter) to create the design. Follow these steps:
1. Go to https://dribbble.com/ to find design inspirations or go to competitors and figure out what they use OR go to https://v0.dev and get design inspiration from there through a prompt
2. Adapt UI from the competitor / v0 and craft a UI in code or within Figma. If you're creating make sure to use the design kits ([material 3](https://www.figma.com/community/file/1035203688168086460/material-3-design-kit) , [shadcn](https://www.figma.com/community/file/1203061493325953101))
3. Create the UI and iterate with the client and make sure they are happy with the UI. I think we should iterate on the UI in code rather than in 

## 3. Functionality
- Once the UI is finalized, we need to start developing the application and connecting the frontend code with the backend code.
- If you haven't clone the [startup-boilerplate](https://github.com/devtodollars/startup-boilerplate) template and build off of that. This will make it a lot easier to build an app and comes with a lot of the needed components.
- More information is in the docs.

## 4. Iterate
- After functionality is built out we iterate with the client and we try to keep the in the loop as long as possible as we build out everything.