---
title: Campus Network Login
date: 2022-01-11 16:43:00 +08:00
---

Though universities will usually provide internet access, Captive Portal authorization is required to use the campus network. In my university, the network will reset daily. So I have to log in many times every day to make my phone, laptop or tablet connect to the internet.

It is quite disturbing to enter a username and password to log in when I hurried to the classroom in haste. That is why I need a tool to finish the auth process as soon as I connect.

# Capture Packets

Open browser, then turn to Captive Portal web page but don't log in for now.  Developer tools are needed to capture login information, it can be either opened in the browser menu (Shortcut Ctrl\+Shift\+I in Chrome) or by pressing 'F12' on the keyboard. Click the *Network* tab, enter username and password and log in. All the activities will be recorded. Look in the *Name* column after the loading process is done, and search for a request using the post method. In my case, it's a request sent to https://61.177.7.1:4430/login, All the data we may use is in it.

This work can be done on iOS or Android also. But on our campus, the website uses HTTPS protocol and a self-signed certification, which means it needs extra works to be captured by MITM.

**2022/1/11 Update:**
Accidentally found that the website can be accessed through HTTP, and the port is 90. This will avoid SSL certification problems on iOS.

# Find the Request

Export these requests, and then search with vscode. It is likely to be a post request. Try common keywords first, such as password, username. Then we can easily get what we want. 

# Calculate the Password

# Send the Request



