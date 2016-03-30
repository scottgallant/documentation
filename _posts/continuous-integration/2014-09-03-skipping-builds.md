---
title: Skipping builds
date: 2014-09-03 00:00:00 Z
categories:
- continuous-integration
tags:
- testing
- faq
weight: 70
---

If you use the classic infrastructure, you can add `--skip-ci` or  `[skip ci]` to the commit message of the last commit before you push and that push will be ignored. Support for skipping builds on the Docker infrastructure will be available soon.

## Ignore pull request merges

When you merge a pull request you can add the `--skip-ci` to the commit message as well.

## Can we limit the branches that are built?

We build all branches you push to your repository. In our opinion every push to your repository should be tested.

We don't have a feature to limit which branches can be built.
