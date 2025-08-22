As you're working as sign user you have to know what privileges the user sign has.

#Victim_machine  

Run on the reverse shell.

```
whoami /priv
```

![[Sing user privileges-20250822112058299.webp]]
You can see the SeImpersonateprivilege is enabled.

## Impersonation Privileges[](https://itm4n.github.io/printspoofer-abusing-impersonate-privileges/#impersonation-privileges)

I want to start things off with this quote from [@decoder_it](https://twitter.com/decoder_it): “_if you have SeAssignPrimaryToken or SeImpersonateprivilege, you are SYSTEM_”. That’s a deliberately provocative shortcut obviously, but it’s not far from the truth.

More details at  [Abusing Impersonation Privileges on Windows 10 and Server 2019](https://itm4n.github.io/printspoofer-abusing-impersonate-privileges/).

To run the process you must download the version  for your system from [here](https://github.com/itm4n/PrintSpoofer/releases).

**Next step:** [[Getting root]]
