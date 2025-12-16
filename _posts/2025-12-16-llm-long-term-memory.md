---
layout: post
title: "LLM's long-term memory vol.2"
date: 2025-12-16
---

Recent days people talking that chatgpt seems to be using RAG for personalized memory. Not sure how far it from truth now, but some day for sure we should have persistent long-term memory for LLMs. Or fast way to access larger context data.

In case of software apps, with every new feature added to project it becomes larger and larger and more metadata. For effective access better to structurize and compress that data. It is like auto-updating documentation in every pull request: agent make changes to code so should make change in documentation; improving and simplifying.

It reminds me how our memory works - every day you getting some information (completely new or improving existing), and our brain re-indexing that data making new connection between neurons. But since we can't re-train model for every use case, we only can make context better and better for each run.

P.S. some idea to test:

1. Split project documentation in `./doc` folder by leveles: top view architecture, entities diagram, integrations, dependencies, etc.
2. Make custom agent controller script that runs planning > retrieving > generation loop.
3. Add custom state like "get-more-info" that will re-run generating with context loaded from some md file.

Theoretically it should reduce amount of context loaded on each step.
