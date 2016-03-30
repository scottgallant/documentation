---
title: Deploy via Cloud66
date: 2014-10-22 00:00:00 Z
categories:
- continuous-deployment
tags:
- deployment
- cloud66
---

Integrating [Cloud 66](http://www.cloud66.com/) with Codeship is as simple as copying and pasting a URL!

Once you've deployed your stack with _Cloud 66_, you'll see a **Redeployment Hook** URL on your **Stack Information** page. To trigger a new deployment via Codeship, simply add a **Script** deployment to the project and add the following command:

```bash
curl -X POST -d "" YOUR_STACK_REDEPLOYMENT_URL
```
