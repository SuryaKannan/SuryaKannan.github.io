---
title: "lock-on"
date: "2026-03-07"
tags: ["python","developer-tooling"]
description: "A deep dive into python package resolvers"
---

What a time to be alive and to be a Python dev. I don't know about you but at work we've been going heavy on Astral's tooling ecosystem, using [uv](https://docs.astral.sh/uv/), [ruff](https://docs.astral.sh/ruff/) and (once its out of beta at the time of writing this) [ty](https://docs.astral.sh/ty/). Not only is their tooling just blazingly fast, but its also really pleasant to work with. 

For this post, i'm going to be diving deep into `uv` and how its internals differ to `pip`, Pythons default package manager. Mostly we will be focussing on the internal dependency solver both use.

There is actually a lot of good stuff out there that I reccomend first:
- [Charlie Marsh's Jane Street talk](https://www.youtube.com/watch?v=gSKTfG1GXYQ) where he talks more about the underlying solver. Made me appreciate how difficult the dependency resolution problem really is.
- [Andrew Nesbitt's deep dive](https://nesbitt.io/2025/12/26/how-uv-got-so-fast.html#fnref:1:1) which shows how updated PEP standards are one of the main drivers behind uv's existance more than the language it was written it. 

TODO: Finish code examples and discuss implementation

The main point of discussion should be about technical decisions behind software projects. Can also discuss how nothing can really last forever and we always need to be creating and updating software. A little sad, but this is the truth of the industry

The only other industry I can think of that this doesn't happen as much in is creative ones like game dev. Even after 500 years, Pacman will still be talked about.
