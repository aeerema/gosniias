# For clients

## How to connect

**mrto2-167**
`ssh -p 1670 *username*@10.24.55.90`

**mrto3-167**
`ssh -p 1670 *username*@10.24.55.93`

## How to download packages

**for yourself:**
`pip3 install --user *packagename*`

**for all users:**
`sudo pip3 install --system *packagename*` 
(sudo is important)


## Configs

**Edit this file:**
`sudo nano ~/.ssh/config`

**Example:**

---
```
Host mrto3
    HostName 10.24.55.93
    Port 1670
    User mrto3-167
```
---
And now you can connect to server like this: `ssh mrto3`

## Usefull commands
**Check:** 
`ping 10.24.55.93`

**Add new user:**
`sudo adduser *username*`
, then add this user to standart groups:
`sudo usermod -a -G 4,24,27,30,46,120,131,132 *username*`

# For server

## Configs

**Edit this file**
`sudo nano /etc/ssh/sshd_config`

## Main SHH commands

**Start OpenSSH Server:**
`sudo systemctl start ssh`

**Stop OpenSSH server:**
`sudo systemctl stop ssh`

**Restart OpenSSH server:**
`sudo systemctl restart ssh`

**See status of OpenSSH server:** 
`sudo systemctl status ssh`
