---
title: The NextJS app I sold for $15K - a full stack breakdown
description: Below is the tech stack I used to build my NextJS app and sell it for $15k
date: 2024-08-14
authors:
  - name: Matthew Wong
    title: Founder
    url: https://twitter.com/IThinkWong
    image_url: https://github.com/matthewwong525.png
---
Hi everyone!

I've been building an app for a client I can't mention the app yet because she hasn't released it yet, but essentially it's [linktr.ee](http://linktr.ee) for people who host events. It's fairly common app so I figured it'd be cool to share my tech stack and a short blurb on why I chose the tool. 

<!-- truncate -->

Here's my full tech stack breakdown:

* **Framework (NextJS)** - The opinionated framework makes development a breeze. I'm able to actually focus on the app rather than setting up the code.
* **State Manager (Plain React / Supabase)** - Honestly with NextJS server routing, I'm able to pass required states from the server and get away with simple plain react states. It's a lot simpler and removes the headache of having another state manager.
* **Language (Typescript)** - Typescript is TOOO good. Having to not worry about the mysterious types saves sooo much time. One thing to note is that, I use [types directly generated from Supabase](https://supabase.com/docs/guides/api/rest/generating-types). Highly recommend doing this!
* **Components (ShadCN/UI)** - This one speeds up the front-end work massively. It allows me to only focus on the placement rather than designing the component. One note here, is that I'd recommend copying the placement of similar functioning websites (e.g. copy Apple Notes UI for your note-taking app). They've probably spent hundreds of man hours optimizing for UI so leverage that.
* **Styling (TailwindCSS)** - This is a no brainer. Tailwind makes adjusting the styling a breeze and allows for me to quickly make changes without having to 
* **Database (Supabase)** - Supabase is a PostgreSQL wrapper that makes it super easy to setup. It is also scales nicely. Highly HIGHLY recommend!
* **Auth (Supabase Auth)** - The integration between the database and auth is seamless and the client libraries make it a breeze to work with. I recommend checkout out their [auth guide](https://supabase.com/docs/guides/auth/server-side/nextjs?queryGroups=router&router=app) to see how to set it up with NextJS.
* **Server (Supabase Edge Functions)** - Most of the time I don't need server processing because I can directly go through Supabase with it's client library. But when I do (e.g. making calls to OpenAI), I use Supabase Edge Functions. It's bundled with the pricing and the client library makes it easy to call.
* **Storage (Supabase Storage)** - The client library, Supabase integration, and pricing make it a no brainer for me to use Supabase storage since I'm using it for pretty much everything already.
* **Hosting (Vercel)** - Hosting on Vercel with Supabase is a breeze. It also has a generous free plan like Supabase
* **Icons (React Icons)** - React Icons is comprehensive and is easy to work with. If you don't need that many icons I recommend only using [Lucide Icons](https://lucide.dev/icons/), which is already bundled with ShadCN/UI
* **Analytics (Posthog)** - It's important to have analytics, posthog makes it such a breeze and integrates well with other platforms (e.g. Stripe) to have a full view of your business.
* **Email (Postmark)** - Postmark has been working well as an email marketing platform but to be honest, I've been looking at a more comprehensive email platform that also makes it easy to setup complicated email campaigns. Might migrate to [loops.so](https://loops.so/).
* **Payments (Stripe)** - Stripe is an amazing platform and is pretty much the goto payments platform for most SaaS companies. It integrates with pretty much everything and is easy to use.
* **Payments Sync (Supabase Edge Functions)** - One caveat of using Stripe is that it's often difficult to keep track of payments within your app. What I've done is I setup a sync between Stripe and Supabase through Supabase Edge Functions. You can see my code [here](https://github.com/devtodollars/mvp-boilerplate/blob/main/supabase/functions/stripe_webhook/index.ts). 

P.S. i've also created a template of above in Github. Feel free to check it out [here](https://github.com/devtodollars/mvp-boilerplate)