Enumerate the ftp server to see whether you can access anonymously.

- Connect to the server.

Username: anonymous
Passsword: just enter/

```
ftp <MACHINE IP>
```

![[FTP Server-20250820200546039.webp]]

- List the content.

```
ftp> dir
```

![[FTP Server-20250820200951587.webp]]

There's a file called `notice.txt`.

- Download the file.
```
ftp> get notice.txt
```

![[FTP Server-20250820201413335.webp]]


#Attacking_machine
- See the content of the file.
```
cat notice.txt
```

![[FTP Server-20250820201621364.webp]]

You already have a hint for the first question.

**Next step:** [[Smb]]
