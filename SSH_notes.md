# For clients

## How to connect

**mrto2-167**

```bash
ssh -p 1670 *username*@10.24.55.90
```

**mrto3-167**

```bash
ssh -p 1670 *username*@10.24.55.93
```

## How to download packages

**for yourself:**

```bash
pip3 install --user *packagename*
```

**for all users:** (sudo is important)

```bash
sudo pip3 install --system *packagename*
```

## Configs

**Edit this file:**

```bash
sudo nano ~/.ssh/config
```

**Example:**

```bash
Host mrto3
    HostName 10.24.55.93
    Port 1670
    User mrto3-167
```

And now you can connect to server like this: `ssh mrto3`

## Usefull commands

**Check:** 

```bash
ping 10.24.55.93
```

**Add new user:**

```bash
sudo adduser *username*
```

, then add this user to standart groups:

```bash
sudo usermod -a -G 4,24,27,30,46,120,131,132 *username*
```

## Docker

**Create docker container**

```bash
cd /home/harddisk/epitome-polygon-deep-learning/docker/lydorn/anaconda-tensorflow-geo/sudo docker run --runtime=nvidia -it --name=docker1 -v /home/harddisk/epitome-polygon-deep-learning:/workspace lydorn/anaconda-tensorflow-geo
```

**List of containers**

```bash
sudo docker ps -a
```

**Start container**

```bash
sudo docker start docker1
```

**Run a command in docker**

```bash
sudo docker exec docker1 python3 filename.py
```

**Enter in docker**

````bash
sudo docker attack docker1
````

# For server

## Configs

**Edit this file**

```bash
sudo nano /etc/ssh/sshd_config
```

## Main SHH commands

**Start OpenSSH Server:**

```bash
sudo systemctl start ssh
```

**Stop OpenSSH server:**

```bash
sudo systemctl stop ssh
```

**Restart OpenSSH server:**

```bash
sudo systemctl restart ssh
```

**See status of OpenSSH server:** 

```bash
sudo systemctl status ssh
```
