---
layout: post
title: "AI security flood"
date: 2026-05-19
---

In the last few months, AI was used quite aggressively for searching vulnerabilities, so obviously it touched linux kernel (even Torvalds complained about it https://lkml.org/lkml/2026/5/17/896) and some other, literally all, open source projects. It was a month of security updates. Now it's still fast but controlled, people making patches before every kid in a school exploits it. But it may not be the same in the next months.

I think it can go much faster, and people won't be able to fix everything in time, and AI tools will become cheaper, so more bugs are found, or tools won't become so cheap, and people will just stop searching for security holes, maybe only in big and very popular projects, just to get the hype.

So what to do for the huge number of open-source projects on GitHub, for those that have a few hundred stars but are not popular enough to get scanned by some AI-security-enthusiasts? The answer is pretty simple.

GitHub has a security advisor bot that can automatically check your project dependencies from packages.json, Cargo.toml, composer.json, go.mod, etc. But for regular, automatic AI analysis, it will be quite expensive, I believe. I don't think even Microsoft could afford that level of useless resources.

In world of pluggable systems like WordPress, there are always plugin directories, or catalogs. And there are moderators doing security checks for the most popular tools.

I think it's time for GitHub to add a security team that goes through some very popular open-source repos, does Claude Mythos magic, and does centralized security maintenance for very popular repos that don't have their own security team. That will be the price for hosting on GitHub and downloading from it.
