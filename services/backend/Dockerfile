# OpenJDK (ARMv7) für Raspberry Pi als Basis
FROM amazoncorretto:21

# Erstelle Arbeitsverzeichnis
WORKDIR /app

RUN yum install git -y

# Klone das Repository
RUN git clone https://gitlab.com/GolemT-Development/kochservice/Kochservice_Backend.git

# Kopiere den Code
RUN cd Kochservice_Backend && chmod +x ./gradlew && ./gradlew build

# Setze das Arbeitsverzeichnis für den laufenden Container
WORKDIR /app/Kochservice_Backend

# Starte die Anwendung
CMD ["./gradlew", "bootRun"]
