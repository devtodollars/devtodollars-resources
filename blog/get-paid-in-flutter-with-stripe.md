---
title: How to Get Paid in Flutter with Stripe
description: One of the biggest headaches with Flutter is setting up a way to collect payments. For Apple and Google you'll need to integrate with their In App Payments, and for Web you'll need to setup Stripe (or something similar)
image: ./assets/50k-flutter-banner.png
date: 2024-03-16
authors:
  - name: Matthew Wong
    title: Founder
    url: https://twitter.com/IThinkWong
    image_url: https://github.com/matthewwong525.png
---


[Architecture Diagram](https://devtodollars.com/assets/images/stripe-architecture-efd9f720c3343f59c5b086fd5b3c5759.png)

One of the biggest headaches with Flutter is setting up a way to collect payments. For Apple and Google you'll need to integrate with their In App Payments, and for Web you'll need to setup Stripe (or something similar). There are solutions like RevenueCat, but I feel they don't do a good job especially if you're just looking to [tip toe the android and apple play store](https://devtodollars.com/blog/how-to-get-paid-in-flutter-with-stripe#tip-toeing-the-android-and-apple-app-store).

That being said, I do plan to [update my boilerplate](https://github.com/devtodollars/mvp-boilerplate/issues/55) and create a guide on how to properly setup Google and Apple app store with webhooks. If that's something you're interested, let me know in the comments down below!

## Implementation

For this guide, I want to walk you through exactly how I've setup it up stripe