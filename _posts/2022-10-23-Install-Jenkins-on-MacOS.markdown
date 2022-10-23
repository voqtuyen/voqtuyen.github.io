---
layout: post
title:  "Install Jenkins on MacOS!"
date:   2022-10-23 11:17:05 +0700
categories: Jenkins ci/cd devops
---

# Intall Jenkins on MacOS

## 1. Install Jenkins using Docker
```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v YOUR-LOCAL-PATH:/var/jenkins_home jenkins/jenkins:lts
```

## 2. Setup Jenkins
- Open browser and go to localhost:8080
- Login to Jenkins using administrator password. Default password can be obtained by running 
  ```bash
  docker logs JENKINS-CONTAINER-ID
  ```
- Install suggested plugins

## 3. Setup ngrok
- Register for ngrok account
- Install ngrok
  ```bash
  brew install ngrok/ngrok/ngrok
  ```
- Connect your account:
  ```bash
  ngrok config add-authtoken YOUR-AUTHNTICATION-TOKEN-FROM-NGROK.COM
  ```
- Start a HTTP tunnel forwarding to your local port 8080:
  ```bash
  ngrok http 8080
  ```
  
