You need to find out the shares smb has.

```
smbclient -L <MACHINE IP>
```

![[Smb-20250820194949161.webp]]

You can see you have access to the share `images$` and `Users` are accessible.



> [!Question] What is the hidden share where images should be copied to?
> images$


**Next step:** [[SMB testing]]

