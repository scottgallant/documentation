---
title: Ignore command on specific branch or run only on a branch
date: 2014-09-10 00:00:00 Z
categories:
- faq
tags:
- faq
- commands
- branch
layout: page
---

## Ignore command on a branch

If you don't want to run a command on a specific branch use the following syntax. In this example we run your command on every branch except gh_pages

```shell
if [ "$CI_BRANCH" != "gh-pages" ]; then YOUR_COMMAND; fi
```

## Run command only on one branch

If you want to run a specific command only on one branch use the following syntax. In this example we run your command only on the master branch.

```shell
if [ "$CI_BRANCH" == "master" ]; then YOUR_COMMAND; fi
```
