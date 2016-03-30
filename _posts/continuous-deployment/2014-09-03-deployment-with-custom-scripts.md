---
title: Deploy via Custom Scripts
date: 2014-09-03 00:00:00 Z
categories:
- continuous-deployment
tags:
- deployment
- scripts
layout: page
---

Script deployment is useful to define your custom deployment commands or execute another task after or prior to a deployment.

For example:

```shell
# execute rake tasks
bundle exec rake my_rake_task

# run additional tests
# my_test_script.sh lives in the root folder
./my_test_script.sh

# deploy to Amazon S3 or any other server with ssh access
# you can define your keys in the environment variables
```

To get more concrete you can, for example, run a migration on Heroku after your deployment:
![Migration after Heroku Deployment]({{ site.baseurl }}/images/continuous-deployment/script_deployment.png)
