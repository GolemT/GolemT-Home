# Verwende ein schlankes JDK 21 Image
FROM amazoncorretto:21

# Setze Arbeitsverzeichnis
WORKDIR /app

# Kopiere die zuvor gebaute JAR-Datei ins Image
COPY app.jar app.jar

# Exponiere Port (falls notwendig)
EXPOSE 8080

# Starte die Anwendung
CMD ["java", "-jar", "app.jar"]
