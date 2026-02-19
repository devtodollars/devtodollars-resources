---
title: A Guide to Building Complex Integrations
description: Hey, I'm Amirali, I am builder, who builds products for customers and myself. I'm sharing some of my experience with building ai agents with you guys in this article.
image: ./assets/building-with-llms.jpg
date: 2026-02-19
authors:
  - name: Amirali Azimi Tabrizi
    title: Founder
    url: https://x.com/Zimbilazim
    image_url: https://github.com/Amiralizim.png
---
![building-ai-agents-with-llms-banner](assets/building-with-llms.jpg)

If you think about it, LLM providers are distributed systems on steroids. Building reliable systems with them, comes with particular challenges. A modern day developer should have proper skills of using LLMs in systems at scale.

Some of the problems one may face when building AI agents using model providers could be:

- Unreliable output of the LLM providers specially with regards to the requested format in the prompt.
- Running into rate limits boundaries of the provider.
- Model quality of output dropping or an outage on the provider side.
- Huge cost of tokens when using llms at scale.

My goal in this blog post is to give the builder a mind frame on how to build cool stuff with these systems in a reliable and scalable fashion.

### Reliability

When it comes to reliability, there are a few needs that a developer has to address right off the bat. First and foremost, is LLM providers’ rate limit boundaries. For this purpose, I used technologies such as LLM gateways where one needs to keep track of the token usage by a model and switch providers if the limits are within reach. I’ve used [Portkey] (https://portkey.ai/) in the past for this purpose. It’s open source and easy to use, you just need to pass in a config file and you are good to go.

The second important reliability issue, is the format of the output returned by the provider. Imagine your prompt asked for an LLM to return its output in json format, but on the 6th try, a string output is received. Fortunately for us, the providers have a field called response_type where one can pass the type of expected response in the header of the request. The format of this header varies based on specific providers. Please refer the documentation of the provider used for the specific format.

For providers unexpected outage purposes, there two solutions I’ve used in the past. The first solution is using default fallback cases with try catch phrases (i.e default object definitions), so your objects don’t become null suddenly and ur system doesn’t crash.

The second is having another provider as a backup in case one fails in your logic.

### Saving Cost

The fastest way to have cost saving, is enabling caching mechanism before the user input reaches the provider. If you have a cache hit, boom, you don’t need to pay the provider. This is particularly good when you are testing with the same data multiple times during development. That way you don’t have to pay for tokens while testing. [Portkey](https://portkey.ai/) also provides simple caching system on top of your LLM calls.

You can go nuts here and use a vector database as well. It’s a pretty cool system for building memory for agents and create a converging “history” systems. In the past I’ve used [Pinecone](https://www.pinecone.io/) for vector database purposes, however there are many other opensource alternatives that I would like to play around with as well. [Trychroma](https://www.trychroma.com/) is a notable one.
If you haven’t worked with vector databases before, they are basically databases that store flat data in vector formats, so you can capture higher dimensional relationships between them. If you are interested read this document for deeper understanding of vector dbs: [what is a vector database](https://www.pinecone.io/learn/vector-database/). 

Another cost saving mechanism is fixing the output’s token count with a header variable you pass to the provider. Again each llm provider have their own variable for this and you would have to refer to their documentation. Only risk for token output fixing is getting a truncated output. Be aware of this and handle it with grace if you decide to implement token truncating.

### Reaching for Better Quality

We all know how ai can be slopish and at times very spikey. That’s why I write all these blogs by my hand with zero ai involved 😁. Personally I have used multiple layers for this purpose and put a supervisor llm at the end where it determines the quality of the previous layers’ output. You can also use more deterministic systems such as large data sets formed into a vector format and check the llm’s output at different stages against it to verify some sort of quality of response.

### Final Thought

I hope this article came helpful for developers to build a mind frame around building with these systems. Its really fun to play around with these systems as a developer. If you like to work with me, shoot me an [email](mailto:amirali@devtodollars.com), or join our [Discord Community](https://discord.gg/AU6aQczrR9) of builders and build amazing things together. It’s an amazing time to be a builder and hope you all are as excited as I am.