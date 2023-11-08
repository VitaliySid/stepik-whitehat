Файл сценария /etc/elite:

```
#!/bin/sh
echo "Someone connect on 31337 port" > bla
mail root < bla
```


Обновить файл сервисов /etc/services и записать:
```
elite 31337/tcp
```

Обновить файл /etc/inetd.conf

```
elite stream tcp wait root /etc/elite elite
```

Командой `chmod a+x elite` делаем файл исполняемым и перезагружаем
`inetd`  демон  `/etc/rc.d/init/inetd  restart`. 

Проверка  
```
telnet 127.0.0.1 31337
```