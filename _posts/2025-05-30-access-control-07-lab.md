---
title: "Access Control Lab 7"
date: 2025-05-29
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# User ID controlled by request parameter 

 This lab has a horizontal privilege escalation vulnerability on the user account page.
 To solve the lab, obtain the API key for the user carlos and submit it as the solution.
 You can log in to your own account using the following credentials: wiener:peter 

**Step 1:** Search the GET method with the id=wiener in target sitemap after logging in and send it the to the repeater

![](/assets/img/2025-05-30-access-control-07-lab/2025-05-30-22-46-15.png)

**Step 2:** Change the id=carlos, grab the API key and submit it in the solution

![](/assets/img/2025-05-30-access-control-07-lab/2025-05-30-22-49-42.png)

Solved the lab!
