---
layout: post
title: "Deep Sick Harmness"
date: 2026-08-29
---

We really need to start having a hard conversation. AI software is going **wildly**. I.e., out of our control. And it will hurt.

Today's my target of interest is DeepSeekHarness - new cool modern agent runtime. 

Before I use something new and tasty in open source, I always checking it's contribution pattern. For example Apache Solr project has quite depressive commits graph - 30 commits per week in average. That's literally one-two full-time developers on project with some small outside help. I wouldn't say this project is being actively developed. More like slowly dying. Compare that to Elasticsearch with 300 commits weekly.

But let's check DSH's contribution.

<img width="1921" height="1673" alt="dsh" src="https://github.com/user-attachments/assets/27981c39-04f3-4e8d-acbe-3145eee574fc" />

One developer committed about 1,400 changes in single week? Wow, that's interesting.

1400 divided by 7 days divided by 12 hours (let's pretend he's a red-eyed person with no life) = 16 commits in 1 hour! One commit every 3-4 minutes. For 5/8 working week it will be 1 commit per minute. During whole week.

I'm not pretending this isn't normal now, or that he actually checked all those changes. Most likely none of you, little vibe-coders, are doing that either. But how we are supposing to rely on something lie this in future?

Maybe now we're supposed to say something like: "but the prompt was written by the author!".

But was it?

What's the point of authoring a commit anymore? Why not instead of commits graph draw just black blot with comment - something happened to codebase and no one knows what, but now it just works.

Maybe our reality is not the best one in term of reliability, but imagine next gen of ai-software could generate it's own code on your machine just in runtime.
