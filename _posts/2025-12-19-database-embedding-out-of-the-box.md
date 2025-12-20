---
layout: post
title: "Out of the box SQL database embedding"
date: 2025-12-19
---

Imagine you doing something like `INSERT INTO post_id, post_summary VALUES (42, "some very long text")` and later when search you can use `SELCT ... WHERE post_summary VECTOR SEARCH "some semantic question here"` and sql returns to you specific posts that closer by meaning.

Ofc it is not possible now, and most likely won't be any time soon, but how cool it could be to have everything integrated into some mysql/postgre/sqlite without openai api, tokens and tons of logic.

How cool it would be to have such sqlite database and use it in android/ios apps, desktop apps that works without internet or on IoT devices or even cars. With modern text to speech and small language models it could be real wonderful future.