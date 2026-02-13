---
title: A Guide to Building Complex Integrations
description: Hey, I'm Amirali, I am builder, who builds products for customers and myself. I'm sharing some of my experience with building integrations into bigger systems with you guys in this article.
image: ./assets/integration.jpeg
date: 2026-02-13
authors:
  - name: Amirali Azimi Tabrizi
    title: Founder
    url: https://x.com/Zimbilazim
    image_url: https://github.com/Amiralizim.png
---
![complex-integration-banner](assets/integration.jpeg)

When I first started building integrations to a huge system, I thought it would be a piece of cake.
As with building systems in general, I realized they are not necessarily as easy as I thought they would be. There are issues that reveal themselves to you once you are deep into the process.
Issues such as:
* Which system has the latest version of data? What is your tell?
* How do you synchronize data between the two systems to preserve the latest most correct data.
* How do you manage the data so every time you synchronize both systems, you don’t have to rewrite all the data.
What are the boundaries of the system you are integrating to? What do they allow you to do and what do they not?

As with building systems go, once you work at a problem long enough, the answers reveal themselves to you. So I will be sharing some of my approaches to these problems. My goal is to set a mind frame on how to approach huge integrations from the beginning.

### Before Begining the Integration
When you start integrating into another major provider, I recommend spending some time in their documentation, understanding their apis and database design decisions. I understand AI is great at coding these days, and you can push stuff pretty far with it, but you are still the driver. It will save you time if you drive the machine right. Focus on understanding the boundaries of the external systems as well. What are some of the things that they don’t allow you to do. This is specifically important to understand early on. It holds you back from chasing dead ends and solving impossible problems.

Studying big players APIs is a great place to start when approaching to design a software in a specific vertical. For example, if you want to build an accounting software, I recommend digging deep into [Xero](https://www.xero.com/) platform’s api. This will show you abstractions that you might be missing in the beginning, in your DB design. It will also give you a very mature view of a system ahead of time.

### What an integration is consistent of
An integration is formed from three major things. A sync, a resync and export. Syncing takes the data from the external system to your system. Resync is how your system matches its data with the external system after the initial Sync. Finally, export is how your system sends data from your system to the external system. I recommend implementing in three separate stages (move vertically). Finishing Sync completely, enables you to make all your mistakes and not having to fix it in three different places. I say this because I tried doing sync, resync and export at the same time for each object (moving horizontally). This caused a lot of pain, because if a mistake was made about the third party’s object I had to go back and fix it in three different places.

### Part 1: Sync
I recommend starting with Sync, it allows you to deeply understand the third parties system and be prepared for next stages of the integration. Store the external objects id in the database, so you can find it later on, this is important.
Recording time when a synchronization happens between two systems is important. At the end of the day, time can be your tell for what is the latest version of the data.
Try to not complicate things, if something has already been exported to the third party, don’t allow the user to edit that field again on your platform, this avoids complications of finding who is the source of truth, and constantly syncing stuff.

### Part 2: Export
Then move to Export. Make sure you have a tell in your database of what object has already been exported to the third party platform. Another important factor about export is making sure you are not writing old data to the third party platform. This is where last sync time comes in handy. Also keep your updated_at field up to date when users change an object on your system, this will save you a lot of headaches later on.

### Part 3: Resync
Resync is a very important piece. Even tho when you get to resync you are tired from implementing the Sync and Export logic, don’t take it lightly. A method I chose for resync was called modified since. The third party applications usually accept a time variable in their header. It will return objects that have been modified after that specific time. In that way you can make sure the data you have on your application are synced with the latest data on the third party platform. Finally, make sure you cover all the CRUD cases, specially deleted objects on the third party. Sometimes the modified since doesn’t cover deleted objects on the third party causing you to face some weird problems when you are in production.

I recommend wrapping your Resync function in a cron job. The resync cron job that runs for example every day, makes sure your system and the third party system don’t diverge from each other too far.
Its also not a bad idea to run your resync function before each export, just to make sure your data is not out dated between the last resync and export times.

### Final Thought
Integrations are a challenging problem, and are unique to each system. There will be weird stuff that will come up as you build the integration. My aim in this blog post was just to give you an overview and a thinking mind frame when approaching this problem. Maybe you can feed this blog post to your coding agent when you are starting to code a big integration. We are agent friendly, we don’t block coding agents from accessing our website.