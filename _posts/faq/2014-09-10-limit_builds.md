---
title: Limit Builds to Specific Branches
date: 2014-09-10 00:00:00 Z
categories:
- faq
tags:
- faq
- builds
layout: page
---

We don’t have a feature to limit which branches can be built.

We build your project on every push (that is, we run your setup and test commands) to let you know as soon as possible if something is broken. We will only ever run a deployment for the specific branch it is configured on and only after all setup and test commands executed successfully. In our opinion every push to your repository should be tested.
