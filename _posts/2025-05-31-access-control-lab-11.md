---
title: "Access Control Lab 11"
date: 2025-05-30
categories: [Writeups]
tags: [Access Control, Portswigger]
---

# Insecure direct object references
 This lab stores user chat logs directly on the server's file system, and retrieves them using static URLs.
 Solve the lab by finding the password for the user carlos, and logging into their account. 

**Step 1:** Go to the live chat and have a chat, then click on view transcript to download the transcript

![](/assets/img/2025-05-31-access-control-lab-11/2025-05-31-03-29-46.png)

It downloads the transcript with 3.txt

**Step 2:** Find the GET method of the download transcript with 3.txt and send it to the repeater

![](/assets/img/2025-05-31-access-control-lab-11/2025-05-31-03-31-39.png)

**Step 3:** Edit the path with different numbers on the .txt file of the transcript to see if you can get other user's transcripts

![](/assets/img/2025-05-31-access-control-lab-11/2025-05-31-03-33-53.png)

Got the password in one of the transcripts, when changed to 1.txt

**Step 4:** Use that password to login with the username carlos

![](/assets/img/2025-05-31-access-control-lab-11/2025-05-31-03-37-25.png)

Lab Solved!!