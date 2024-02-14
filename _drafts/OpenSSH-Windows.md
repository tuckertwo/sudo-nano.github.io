---
layout: post
title: "How to do a Better Than Default Install of OpenSSH on Windows"
date: 2024-01-26 22:00:00 -0700
tags: windows security tutorial ssh
categories: drafts
hidden: true
--- 

## Install OpenSSH Server 
1. Open "Manage Optional Features" in your settings. 
2. Click "Add a feature" at the top. 
3. Search for OpenSSH Server 
4. Click "Install"

## Configure OpenSSH Server
Windows stores the configuration file in `C:\ProgramData\ssh\`. Edit the file `sshd_config`. 

### Change the port 
There are uncountably many bots constantly scanning the internet for easy computers to compromise, and one of the largest targets is any sort of SSH connection. If you leave port 22 open, you'll experience a barrage of attacks upon it. Changing the port to basically anything else will fix this. 

There's a line in `sshd_config` that says `#Port 22`. Change "22" to a different port and uncomment the line. Remember what port you set, because we'll need to set a firewall rule to allow it later. 

### Disable Password Authentication
Passwords can be guessed. Technically, authentication keys can be as well, but it's astronomically less likely. Additionally, using key-based authentication is much more convenient once set up, as you don't have to remember a password (unless you choose to set a password on your SSH key). 

Scroll down to the section of `sshd_config` for password authentication: 
```
# To disable tunneled clear text passwords, change to no here! 
#PasswordAuthentication yes
#PermitEmptyPasswords no
```

Change the "yes" after PasswordAuthentication to "no" and then uncomment the line to disable password authentication. 

### Disable Insecure Algorithms
The algorithms `ecdh-sha2-nistp256`, `ecdh-sha2-nistp384`, and `ecdh-sha2-nistp521` should be disabled because they are likely backdoored by the NSA. 

## Make OpenSSH Server Start Automatically 
1. Open Services 
2. Go to OpenSSH SSH Server, double click on it, and change its startup type to "Automatic". Click the "Start" button to start it now. 
3. Do the same for OpenSSH Authentication Agent. 

## Add a Firewall Exception
1. Go to Control Panel > System and Security > Windows Defender Firewall 
2. Verify that your SSH server is functioning by disabling your firewall and attempting to SSH into your server. (This helps determine that any further problems are from firewall rule errors, and not server configuration errors.) Re-enable your firewall after this is done. 
3. Click on "Advanced Settings" in the sidebar 
4. Create a new inbound rule. Select "Port" for the type of rule, then specify TCP and the port that you put in your configuration file. Select "Allow the connection". Keep all boxes checked under "When does this rule apply?"
5. Save the firewall rule.
6. SSH into your server again to verify that the firewall rule worked. 

## Bonus: Evaluate your SSH security with `ssh-audit`

