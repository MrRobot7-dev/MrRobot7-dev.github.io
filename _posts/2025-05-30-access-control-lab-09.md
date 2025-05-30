---
title: "Access Control Lab 9"
date: 2025-05-29
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# User ID controlled by request parameter with data leakage in redirect 
 This lab contains an access control vulnerability where sensitive information is leaked in the body of a redirect response.To solve the lab, obtain the API key for the user carlos and submit it as the solution. You can log in to your own account using the following credentials: wiener:peter 

**Step 1:** Find the GET method in target sitemap after logging with wiener and change the id to carlos

![](/assets/img/2025-05-30-access-control-lab-09/2025-05-30-23-18-42.png)

It will redirect you to the login page again but you will get the API key so lab solved! 