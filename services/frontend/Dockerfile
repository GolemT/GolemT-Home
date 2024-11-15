# Node.js (ARMv7) für Raspberry Pi als Basis
FROM node:latest

# Erstelle Arbeitsverzeichnis
WORKDIR /app

# Klone das Repository
RUN git clone https://gitlab.com/GolemT-Development/kochservice/angular_frontend.git

# Wechsle ins Verzeichnis und installiere die Abhängigkeiten
RUN npm install -g pnpm

# Setze das Arbeitsverzeichnis für den laufenden Container
WORKDIR /app/angular_frontend

RUN git pull && pnpm install

# Build der App erstellen
RUN pnpm build

# Starte die App
CMD ["pnpm", "start", "--host", "0.0.0.0"]
