---
title: "Access Control Lab 12"
date: 2025-05-30
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# Multi-step process with no access control on one step
This lab has an admin panel with a flawed multi-step process for changing a user's role. You can familiarize yourself with the admin panel by logging in using the credentials administrator:admin.
To solve the lab, log in using the credentials wiener:peter and exploit the flawed access controls to promote yourself to become an administrator.

**Step 1:** Login as admin and then change the user carlos to admin to capture it's POST request

![](/assets/img/2025-05-31-access-control-lab-12/2025-05-31-04-00-20.png)

This POST request shows that carlos has been upgraded to admin, it is confirmed and the session cookie is there.

**Step 2:** Now login as wiener and capture it's GET request id=wiener. After that copy it's session cookie.

![](/assets/img/2025-05-31-access-control-lab-12/2025-05-31-04-04-22.png)

**Step 3:** Paste the session cookie(wiener) in the POST request of carlos and change the username to wiener.

![](/assets/img/2025-05-31-access-control-lab-12/2025-05-31-04-06-56.png)

What it does is, the server takes the admin role POST request and processes it without proper access controls which upgrades the username wiener to administrator.

Lab Solved!

