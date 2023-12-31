## Ресурсы
- База данных открытых SSL/TLS-сертификатов, которые были выданы для доменных имен  
[Certificate Search](https://crt.sh/)
- Изучение известной информации о домене и связанных с ним ресурсов  
[dnsdumpster](https://dnsdumpster.com/)
- [OSINT Framework](https://osintframework.com/)
- [Awesome OSINT](https://github.com/jivoi/awesome-osint)
- [Кибер-разведка в компании на основе OSINT](https://habr.com/ru/companies/tensor/articles/706656/)
- [СПАРК](https://spark-interfax.ru/) – это система, собирающая всю доступную информацию о компаниях и извлекая из нее знания, помогает получать подробную информацию о бизнесе организаций и о привязанных к нему информационных активах, сайтах и доменных именах.  
- RIPE (Réseaux IP Européens) – это некоммерческая организация, которая занимается управлением и распределением ресурсов IP-адресации и автономных систем в странах Европы, Ближнего Востока и Центральной Азии. На ее сайте https://apps.db.ripe.net/db-web-ui/fulltextsearch можно найти различные данные (включая доменные имена), связанные с владельцем выделенных ему сегментов IP-адресов.  

## Утилиты

- Инструмент для сбора информации об инфраструктуре ([описание](https://kali.tools/?p=4325))
```
amass enum -v -src -ip -d cyber-ed.ru
```  

- Команда позволяет получить информацию о доменном имени  
```
host cyber-ed.ru  //linux
nslookup -qtype=mx cyber-ed.ru  //win
```

## Цели

- Обнаружение доменных имен, принадлежащих организации
- Обнаружение “живых” хостов в сети и составления списка их IP-адресов
- Определение актуального статуса сетевых портов узлов из списка
- Определение типа и версии операционной системы на исследованных машинах
- Определение версий ПО или служб, которые находятся на сетевых портах
- Сбор информации об используемых технологиях на веб-сайте

## Полезные ссылки
- [Process of OWA Enumeration?](https://infosecinterview.com/posts/process-of-owa-enumeration/)