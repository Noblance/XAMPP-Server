# Self-made XAMP-like Server

Dieses Repo ist nur für Docker-unterstützende Systeme !!!


### Schritte zur Installation:

1. Sicherstellen, dass man jegliche Form von Docker-Unterstütung installiert hat

2. in das gewünschte Directory in der CMD/Terminal <code>#git clone https://github.com/Noblance/XAMPP-Server.git</code> eingeben

3. Um den Server zu starten <code>#docker compose up -d</code> im selben Verzeichnis in CMD/Terminal eingeben

4. Um den Server zu stoppen  <code>#docker compose stop/down</code> oder Ctrl+C


### Konfigurationen:
1. Die Datenbank-Daten (Passwort, Datenbankname, Benutzername) sind im docker-compose.yml
2. unter app/public sind die Web-Server files
3. Der Port, mit der auf die Webseite zugegriffen wird kann in der docker-compose.yml geändert werden
4. um die Konsole beim Starten zu entfernen (was auch simplere Fehlermeldungen reduziert) in der PHP.Dockerfile folgendes eintragen:
```
FROM php:fpm

RUN docker-php-ext-install pdo pdo_mysql
```
evt. danach noch ein <code>#docker compose build</code> durchführen und dann wieder <code>#docker compose up -d</code>
