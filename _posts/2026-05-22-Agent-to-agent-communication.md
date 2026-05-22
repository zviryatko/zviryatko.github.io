---
layout: post
title: "Agent to agent communication"
date: 2026-05-22
---

As next step after UI/UX and AX (AI experience) will be Agent-to-Agent communications. I’m not talking just about api or mcp, but about main app architecture design that expects AI calling that endpoints instead of users.

So, what does it mean on practice? Well, what can AI do and how it do what it can compared to humans?
First, it can read with attention. When you show validation error to human, they won’t notice many things, like for simple news website or driver license form, doesn’t mater how much good you write description on how to fill the form, or how not to fill, real (human) users will always fill them as they able to, or how they used to fill it before. Do you spot the difference? :)

Second, you can give much more context, much more form elements. Imagine you need to implement some complex workflow. To keep quality good you need to fill 150 different attributes. Every UX book highlight that as anti pattern! Totally no one enjoy filling 150 form fields. Except the AI, which can do that effectively. You don’t even need to parse the data with your server side agent. Imagine costs saving!

And third, most obviously cost-saving, you don’t need design. Forget about React, frontend, responsive. That’s awesome. Just do old simple crud with json api. That’s all.

I’m kindly appreciate such future. Tell to your agent in what format to collect data, give skill like prompt to someone’s agent, and they will do the magic. Automatic, on background. Users will control data to share, ai will control contract - easy-peasy.

Now wondering what idea to use to build such agentic-first app.

What do you think?