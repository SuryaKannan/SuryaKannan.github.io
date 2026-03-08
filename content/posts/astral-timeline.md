---
title: "Python developers are spoilt"
date: "2026-03-07"
tags: ["python","developer-tooling","astral"]
---

What a time to be alive and to be a Python dev. I don't know about you but at work we've been going heavy on Astral's tooling ecosystem, using [uv](https://docs.astral.sh/uv/), [ruff](https://docs.astral.sh/ruff/) and (once its out of beta at the time of writing this) [ty](https://docs.astral.sh/ty/). Not only is their tooling just blazingly fast, but its also really pleasant to work with. 

For this post, i'm going to be diving deep into `uv` and how its internals differ to `pip`, Pythons default package manager.

There is actually a lot of good stuff out there that I reccomend first:
- [Charlie Marsh's Jane Street talk](https://www.youtube.com/watch?v=gSKTfG1GXYQ) where he talks more about the underlying solver. Made me appreciate how difficult the dependency resolution problem really is.
- [A podcast Charlie was on](https://www.youtube.com/watch?v=0wmz6RyVoFw) where he talks more about the why of uv.
- [Andrew Nesbitt's deep dive](https://nesbitt.io/2025/12/26/how-uv-got-so-fast.html#fnref:1:1) which shows how updated PEP standards are one of the main drivers behind uv's existance. 

As I was consuming all of this stuff, I took some notes which will actually be the basis of this post. [If you wanna see my messy handwriting check here]()

AIM:  - Toy implementation + real codebase pinpointing + concrete examples showing the difference
