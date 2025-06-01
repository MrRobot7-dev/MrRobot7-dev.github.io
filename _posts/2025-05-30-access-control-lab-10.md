---
title: "Access Control Lab 10"
date: 2025-05-29
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# User ID controlled by request parameter with password disclosure
This lab has user account page that contains the current user's existing password, prefilled in a masked input.
To solve the lab, retrieve the administrator's password, then use it to delete the user carlos.
You can log in to your own account using the following credentials: wiener:peter 

**Step 1:** After logging in, check the GET method and the prefilled password of wiener 

![](/assets/img/2025-05-30-access-control-lab-10/2025-05-30-23-50-27.png)

So it means if we change the user id to administrator we will get the password of the admin prefilled

**Step 2:** Change the user id and then check the value of the password in the response field.

![](/assets/img/2025-05-30-access-control-lab-10/2025-05-30-23-53-36.png)

**Step 3:** After getting the password log in as admin and delete the user carlos

![](/assets/img/2025-05-30-access-control-lab-10/2025-05-30-23-55-14.png)

Lab Solved!


