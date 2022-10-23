---
layout: post
title:  "Install Jenkins on MacOS!"
date:   2022-10-23 11:17:05 +0700
categories: Jenkins ci/cd devops
---

# Intall Jenkins on MacOS

## 1. Install Jenkins using Docker
{% highlight bash %}
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v YOUR-LOCAL-PATH:/var/jenkins_home jenkins/jenkins:lts
{% endhighlight %}

## 2. Setup Jenkins
- Open browser and go to localhost:8080
- Login to Jenkins using administrator password. Default password can be obtained by running 
  {% highlight bash %}
  docker logs JENKINS-CONTAINER-ID
  {% endhighlight %}
- Install suggested plugins

## 3. Setup ngrok
- Register for ngrok account
- Install ngrok
  {% highlight bash %}
  brew install ngrok/ngrok/ngrok
  {% endhighlight %}

- Connect your account:
  {% highlight bash %}
  ngrok config add-authtoken YOUR-AUTHNTICATION-TOKEN-FROM-NGROK.COM
  {% endhighlight %}

- Start a HTTP tunnel forwarding to your local port 8080:
  {% highlight bash %}
  ngrok http 8080
  {% endhighlight %}
  
