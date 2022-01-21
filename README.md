# Hack The Box Cheatsheet
Cheatsheet con comandos e información útil para HTB

# Linux 

## Directorios y Archivos utiles
Puertos escuchando en formato Hex\
```/proc/net/tcp```

Resumen general del sistema\
```/proc/sched_debug```

Output de consola del proceso especificado\
```/proc/{PID}/cmdline```

## Comandos y pipes utiles

Reemplazar \n por verdaderos saltos de linea\
```sed 's/\\n/\n/g'```


## Python 
Elevar shell\
```python3 -c 'import pty; pty.spawn("/bin/bash")'```

Cuando uso Requests y el texto en el GET se desencodea\
```urllib.parse.quote('/')```

# Nmap

Quick Scan\
```nmap  -p-  --min-rate=1000 -T4```

Deep Scan\
```nmap -sS -A -sC -sV -p- --min-rate 5000```

