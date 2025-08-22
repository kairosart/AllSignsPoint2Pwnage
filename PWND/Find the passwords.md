
## The users password

The hint for the question is: *The user is automatically logged into the computer*.

Here’s what it means in detail:

- The system is set to **automatically log a user in** when Windows boots (without asking for a password).

- For Windows to do this, it needs the user’s password. Since Windows has no secure way of storing it for auto-login, it is kept in **plain text** inside the Windows Registry.

- Specifically, the password is usually stored in:
	`HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon`

with keys like:

- `DefaultUserName`
- `DefaultPassword`
- `AutoAdminLogon`

If `AutoAdminLogon = 1`, Windows uses `DefaultUserName` + `DefaultPassword` to log in automatically.

### Get the key

#Visctim_machine
Run on the shell you already have:

```
reg query "HKLM\Software\Microsoft\Windows NT\CurrentVersion\Winlogon"
```

![[Users password-20250821200806508.webp]]

> [!Question] What is the Users Password?
> `gKY1uxHLuU1zzlI4wwdAcKUw35TPMdv7PAEE5dAFbV2NxpPJVO7eeSH`

## What is the Administrators Password?

There's a share where only the administrator can access, it's `installs`.

- Go to the directory.
- List the files.
	![[Find the passwords and Admin Flag-20250821201554241.webp]]
- Check the `Install_www_and_deploy.bat` file.
```
type Install_www_and_deploy.bat
```

![[Find the passwords and Admin Flag-20250821201845472.webp]]

> [!Question] What is the Administrador Password?
> `RCYCc3GIjM0v98HDVJ1KOuUm4xsWUxqZabeofbbpAss9KCKpYfs2rCi`

> [!Question] What executable is used to run the installer with the Administrator username and password?
> `PsExec.exe`


## VNC Password

Hint: here are a few versions but some do not work. The version here is known to work: [http://aluigi.altervista.org/pwdrec.htm](http://aluigi.altervista.org/pwdrec.htm).

### Getting the tool
- Download [VNC password decoder 0.2.1](https://aluigi.altervista.org/pwdrec/vncpwd.zip) *(vncpwd).*
- Decompress it.
- Upload `vncpwd.exe` via SMB to the images directory.

### Getting the passowrd

#Visctim_machine 
- Go to `C:\Program Files\uvnc bvba\UltraVNC`.
- There's a file `ultravnc.ini`. See the content an you'll find:
	passwd=B3A8F2D8BEA2F1FA70
- On the `C:\xampp\htdocs\images` run the following:
```
vncpwd.exe B3A8F2D8BEA2F1FA70
```

![[Find the passwords and Admin Flag-20250822111217809.webp]]


> [!Question] What is the VNC Password?
> `5upp0rt9`

**Next step:** [[Sing user privileges]]

