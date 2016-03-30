---
title: Pushing to Heroku fails
date: 2014-09-10 00:00:00 Z
categories:
- faq
tags:
- faq
- build error
- heroku
layout: page
---

In case your deployment to Heroku fails with an error message similar to this:

```shell
Fetching repository, done.
To git@heroku.com:my-project.git
 ! [rejected]        12a898d34f0be4df6231e76aa767001f0396bd9 -> master (fetch first)
error: failed to push some refs to 'git@heroku.com:my-project.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

That error is saying that on Heroku are later changes than those you want to push, so it stops.

## Solution

* You can pull the latest changes from the Heroku repository locally and then push to GitHub / BitBucket again
* or configure the Heroku deployment to _force push_ instead. If you decide to follow this route, we recommend disabling this setting afterwards again.
