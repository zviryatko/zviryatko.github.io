---
layout: post
title: "Finite State Machine is the Key"
date: 2025-09-10
excerpt_separator: <!--more-->
---

To make AI solutions reliable and output result more deterministic we should put the borders on it, fit the results to some mold. And the key to it is Finite State Machine, let me explain:

Imagine you building chatbot that runs some linux commands (or just random mcp commands), it parses the text, extracts actions and arguments, searches all mcp commands that matches that actions and call it. Sounds simple, right?
But when you have, let's say, 5 commands, your chatbot app now able to produce 5! different flows that not depends on arguments! It's 120 possible permutations! But who have app with only 5 actions?

The solution for it lays down in providing Finite State Machine app results, to reduce number of permutations between actions. It will dramaticaly reduce number of outcomes and makes it more predictable.
In general I think it is better to use AI now to generate such predictable apps on the fly for solving incoming tasks, rather than using LLM for "predicting" output results with reasoning.
