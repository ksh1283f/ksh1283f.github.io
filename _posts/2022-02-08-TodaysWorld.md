---
layout: post
title: (iOS) TodaysWorld
tags: [iOS]
---

# TodaysWorld
***

<p align="left">
    <img src="https://img.shields.io/badge/Xcode-11.0-blue">
    <img src="https://img.shields.io/badge/iOS-13.2-green">
</p>

>TodaysWorld is a simple news app. you can see the top headline of your country or other countries with options
<p align="left">
    <img src="/assets/TodaysWorld/Imgs/Example.gif" width = "200">
</p>

## Prerequisite
***
1. NEWS API
    - Go to News API [NewsApi link](https://newsapi.org/)
    - If you don't have your account, please sign up and get api key.
    - before step is done, open your xcode, make directory <b>ApiKey</b> and make <b>apiKey.plist</b>  
    ![DirectoryExample.png](/assets/TodaysWorld/Imgs/DirectoryExample.png) 
    - set the key <b>apiKey</b> and insert api key you made into the value  
    ![apiKey.PlistExample](/assets/TodaysWorld/Imgs/apiKeyPlistExample.png)  

2. Firebase Authentication
   - Implement Firebase Authentication [Firebase Auth docs](https://firebase.google.com/docs/auth/ios/google-signin?authuser=0)

## Storyboard
***
![Storyboard](/assets/TodaysWorld/Imgs/storyboard.png)

## Notice
***
> Your top headlines article would be selected according to your device's first language. Therefore if the article's language is not your country's, please check <b>Settings -> Language</b>




