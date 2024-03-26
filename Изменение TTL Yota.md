# Linux

```bash
sudo iptables -t mangle -A POSTROUTING -j TTL --ttl-set 65
```

Добавить задачу в crontab через cronie:
```bash
EDITOR=nano crontab -e
```
```bash
@reboot sudo iptables -t mangle -A POSTROUTING -j TTL --ttl-set 65
```

# Windows

1. Открыть regedit.exe
2. В *HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters* создать DWORD (32-bit), присвоить имя DefaultTTL и значение 65 в десятичном исчислении

[Wub для Windows](https://disk.yandex.ru/d/oaAM9HHeURgUBA)

