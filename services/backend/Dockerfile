# OpenJDK (ARMv7) für Raspberry Pi als Basis
FROM amazoncorretto:21

# Erstelle Arbeitsverzeichnis
WORKDIR /app

RUN yum install git -y

# Klone das Repository
RUN git clone https://gitlab.com/GolemT-Development/kochservice/Kochservice_Backend.git

# Setze das Arbeitsverzeichnis für den laufenden Container
WORKDIR /app/Kochservice_Backend

# Kopiere den Code
RUN git pull && chmod +x ./gradlew && ./gradlew build

# Starte die Anwendung
CMD ["./gradlew", "bootRun"]
