# MariaDB (ARMv7) für Raspberry Pi als Basis
FROM mariadb:10.5

# Setze Umgebungsvariablen für Datenbank
ENV MYSQL_ROOT_PASSWORD=password
ENV MYSQL_DATABASE=mydatabase
ENV MYSQL_USER=user
ENV MYSQL_PASSWORD=password

# Datenbankport öffnen
EXPOSE 3306

# Startbefehl für MariaDB
CMD ["mysqld"]
