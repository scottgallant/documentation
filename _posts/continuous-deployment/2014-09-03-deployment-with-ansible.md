---
title: Deploy via Ansible
date: 2014-09-03 00:00:00 Z
published: false
categories:
- continuous-deployment
tags:
- deployment
- ansible
layout: page
---

Ansible is fully supported on the Codeship.

## Install ansible
To install ansible run

```shell
pip install ansible
```

as part of your setup commands. We will cache ansible for your next build so the install task should be faster.

## Run ansible in Script Deployment
To deploy with Ansible, set up a Script Deployment and run exactly the same Ansible commands you would use to deploy from your local machine.

## Install SSH Key on your server
To be able to SSH into your servers, make sure you've set up your SSH public key as an authorized key on your servers.
