# Node.js (ARMv7) für Raspberry Pi als Basis
FROM node:latest

# Erstelle Arbeitsverzeichnis
WORKDIR /app

# Klone das Repository
RUN git clone https://github.com/GolemT/Kochservice.git

# Wechsle ins Verzeichnis und installiere die Abhängigkeiten
RUN cd Kochservice && npm install

# Setze das Arbeitsverzeichnis für den laufenden Container
WORKDIR /app/Kochservice

# Build der App erstellen
RUN npm run build

# Starte die App
CMD ["npm", "start"]
