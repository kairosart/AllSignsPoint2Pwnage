
Visit the <MACHINE_IP> web.

![[Web server-20250820205428329.webp]]

You only see a series of images one after another and nothing more on the code.

## Gobuster

Explore the directories and files on the web server.

```
gobuster dir -u http://<MACHINE IP> -w /usr/share/wordlists/dirb/common.txt
```

![[Web server-20250821192430750.webp]]

The most interesting end point is http://10.10.2.71/dashboard/.

![[Web server-20250821192721494.webp]]

**Next step:** [[FTP Server]]