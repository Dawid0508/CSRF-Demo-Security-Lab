## CSRF-Demo-Security-Lab
Autorzy: <br />
[Michał Chmiel](https://github.com/Spren3) <br />
[Mateusz Sznurawa](https://github.com/mateusznu) <br />
[Dawid Gruszecki](https://github.com/Dawid0508) <br />

Repozytorium stworzone w celu zapoznania się z atakami OWASP CSRF, [podatnościami](https://owasp.org/www-community/attacks/csrf) oraz ich [zapobieganiu.](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)

Jako część projektu dokonaliśmy zmian w naszej [aplikacji](github.com/Spren3/FileStorageSite) by pokazać jej podatności na ataki Cross-site Request Forgeries.
Instrukcje do zadań opisano w katalogu [tasks](https://github.com/Dawid0508/CSRF-Demo-Security-Lab/tree/main/tasks/tasks.md). Zadania dają szansę przeprowadzenia ataków CSRF i ochrony przed nimi na własną rękę! <br/>

## Przygotowanie środowiska
Do uruchomienia aplikacji należy skorzystać z **docker-compose**.
### Windows i macOS
**Docker-compose** wchodzi w skład **Docker Desktop**, jeśli więc to oprogramowanie jest zainstalowane, **instrukcję można pominąć**.

1. Zainstaluj **Docker Desktop**: Pobierz i zainstaluj Docker Desktop z oficjalnej strony: https://www.docker.com/products/docker-desktop
2. Sprawdź instalację:
```sh
docker-compose --version
```


### Linux
1. Pobierz plik binarny **Docker Compose**:
```sh
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
2. Nadaj uprawnienia do wykonania:
```sh
sudo chmod +x /usr/local/bin/docker-compose
```
3. Sprawdź instalację:
```sh
docker-compose --version
```

<br/> 

### Następnie sklonuj repozytorium na własne urządzenie:
```sh
git clone https://github.com/Spren3/FileStorageSite
```
Uruchom polecenie docker-compose up -d, aby zbudować obrazy i uruchomić kontener w tle:
```sh
docker-compose up -d --build
```

<br/> 

**Aplikacja powinna być dostępna pod adresem** _localhost:1000_.
Jeśli chcesz zatrzymać kontener, użyj:
```sh
docker-compose down
```
By ponownie uruchomić:
```sh
docker-compose up -d
```
**Dostęp do aplikacji ogranicza statyczne hasło**
```sh
hasło: MbappeDurant
```

### Przydatne polecenia
1. By połączyć się z Docker Exec (i móc wykonywać polecenia wewnątrz kontenera):
```sh
docker exec -it <nazwa_kontenera> bash
```
Nazwa kontenera do sprawdzenia przez _docker ps_, pole _NAMES_. 

<br/> 

2. Wyświetlenie zawartości tabel _files_ i _directories_ (wewnątrz Docker Exec):
```sh
php /tmp/show_db_files.php
php /tmp/show_db_dirs.php
```
