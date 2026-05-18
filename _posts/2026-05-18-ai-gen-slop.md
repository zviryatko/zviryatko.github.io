---
layout: post
title: "AI generated slop"
date: 2026-05-18
---

There is something worng with AI generated code. The code itself is mostly fine, it still statistically best of what we have up today. Until LLM Agents could create better than human code regularly. The wrong part is not the code, but the task. Well, not really the main goal of app, or main idea, but the action items that must be done for implementing ideas.

The is something definitely wrong with implementation in AI-coded apps. Let me explain.

Recent news about AI app from Milla Jovovich that called [Memory Palace](https://github.com/MemPalace/mempalace) delighted everyone, despite actress learnied how to build AI app and blah-blah-blah. Ofcourse she didn't act alone, which is ok. And I don't think person who could be actress aren't smart enough to learn other things. The problem I see is in prompt itself:

> Wrong is worse than slow.

https://github.com/MemPalace/mempalace/blob/main/mempalace/mcp_server.py#L641C103-L641C128

The thing is - does it really necessary? I mean, if not providing that instruction it will give you faster solution but... less precise? What can qualify prediction results - less accurate?

Obviously we can't control the way how long LLM can generate text that way. It is possible by CoT or any similar way by giving more and more instructions. Double-check instructions, self-correct instruction. Running second llm call to check previous results. But not telling that slow response is ok.

You may think that it is just one random repo with prompt created not by professionals, and I'll tell you about Spec-kit from GitHub team. Does GitHub developes are good enough to make good prompts?

The Spec-Kit is a tool that transform the way how you develop your app, like Test-Driving-Development. The main idea is that you keep text-only specifications in core of app and uses agents to generate the shell. It was popular in era of Ruby, where people wants to keep the trace for every feature they adds. I.e. reason to have any line of number, like related github issue in commit. So here is example from Spec-Kit documentation:

> /speckit.clarify Focus on security and performance requirements.

https://github.github.com/spec-kit/quickstart.html#step-4-refine-and-validate-the-spec

And my question is the same - what if I don't tell AI Agent to focus on Security and Performance? Would it make slow and leaky app? Well, when it is, than we ducked up. 🦆🦆🦆

<hr />

I've tried ChatGPT with `Wrong is worse than slow.` and without on simple Fibonacci function:

<img width="6144" height="3244" alt="Screenshot From 2026-05-18 14-00-37" src="https://github.com/user-attachments/assets/036720b3-da7f-4c77-89a8-de39f6ca8d8f" />

Not sure how to react on this, IMHO prompt added some useless mess.

Another thing with `Focus on security and performance requirements`, this one I've tested specifically on PHP - and things becomes more interesting:

<img width="6144" height="3244" alt="Screenshot From 2026-05-18 14-27-18" src="https://github.com/user-attachments/assets/88944469-1232-40f4-9005-1f144826ec0c" />

First of all it added HTTPS and CSP headers, to prevent potential xss. Also added CSRF token, to avoid another potential vector of attack (which makes not much sense for that example, but if you use in real app it is important). And the last this more secured prompt it generated html escape code that actually more secure: `htmlspecialchars($value, ENT_QUOTES | ENT_SUBSTITUTE, 'UTF-8');` with extra `ENT_QUOTES | ENT_SUBSTITUTE` flags, that prevents XSS.

And to be honest here is the problem - AI will generate not secure code, and if you are not an expert, you even won't find that. But even if you add prompt to make it super-duper-secure-and-fast it could make it better or it could not. You neven know.
