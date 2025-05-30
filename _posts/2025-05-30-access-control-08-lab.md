---
title: "Access Control Lab 8"
date: 2025-05-29
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# User ID controlled by request parameter, with unpredictable user IDs
 This lab has a horizontal privilege escalation vulnerability on the user account page, but identifies users with GUIDs.To solve the lab, find the GUID for carlos, then submit his API key as the solution.You can log in to your own account using the following credentials: wiener:peter 

**Step 1:** Find a blog written by carlos and then click on his name, find the request in target sitemap

![](/assets/img/2025-05-30-access-control-08-lab/2025-05-30-23-05-53.png)

**Step 2:** In the GET request you can see the user id, so just copy paste in the wiener id parameter

![](/assets/img/2025-05-30-access-control-08-lab/2025-05-30-23-08-45.png)

![](/assets/img/2025-05-30-access-control-08-lab/2025-05-30-23-09-53.png)

Voila! You found the API key. Lab Solved!
