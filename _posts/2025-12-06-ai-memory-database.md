---
layout: post
title: "AI memory database"
date: 2025-12-06
---

Chain of Thoughts was extended by Memory of Thoughts by simple in-between hidden responses and keeping instructions.md or todo.md files for better planning. But this data keeps growing.

Recently friend of mine shared his practical case - storing instructions in git commit. Easy to read by AI, connected to PR code changes. But does't it make sense to use in long term? Imagine you see reasoning of AI bot from 5 years old generated code. Or some other model see that.

Anyway, keeping lot of .md files for every feature is not comfortable. Maybe we should make some local sqlite storage for that? Or better to use document database. It'll have a lot of context in between, without lot of files. With auto clean after it's done or by some time.

Or store it in cloude as part of source code storage. Kinda AI-documentation-storage-service, maybe wiki engine. With references to jira or other task tracker.
