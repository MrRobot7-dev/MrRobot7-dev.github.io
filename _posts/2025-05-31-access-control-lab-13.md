---
title: "Access Control Lab 13"
date: 2025-05-30
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# Referer-based access control
This lab controls access to certain admin functionality based on the Referer header. You can familiarize yourself with the admin panel by logging in using the credentials administrator:admin.
To solve the lab, log in using the credentials wiener:peter and exploit the flawed access controls to promote yourself to become an administrator. 

**Step 1:** Login as admin and change the user carlos to admin and find the GET request in HTTP history, send it to repeater.

![](/assets/img/2025-05-31-access-control-lab-13/2025-05-31-04-16-42.png)

**Step 2:** Now login as wiener and capture it's GET request id=wiener and copy it's session cookie.

![](/assets/img/2025-05-31-access-control-lab-13/2025-05-31-04-19-58.png)

**Step 3:** Now in GET request of carlos admin change, copy the cookie of wiener and change the username to wiener. We did that because the referer in the carlos GET request is of the admin page so now the website will process it without checking access control and wiener will be upgraded to admin.

![](/assets/img/2025-05-31-access-control-lab-13/2025-05-31-04-21-53.png)

AND boom lab Solved!!!