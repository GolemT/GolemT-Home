# Basis-Image für Raspberry Pi (ARMv7-Architektur)
FROM arm32v7/debian:latest

# Installiere notwendige Pakete wie curl, git, etc.
RUN apt-get update && apt-get install -y \
    curl \
    qemu \
    qemu-user-static \
    binfmt-support \
    sudo \
    git \
    && apt-get clean

# Setze die notwendigen Emulations-Tools für QEMU ein
COPY qemu-arm-static /usr/bin/

# Optional: Installiere Docker innerhalb der Emulation (falls du innerhalb der emulierten Umgebung weitere Docker-Container betreiben willst)
RUN curl -fsSL https://get.docker.com | sh

# Setze das Arbeitsverzeichnis
WORKDIR /home/pi

# Bereitstellen von Anweisungen oder Standard-Befehlen
CMD ["bash"]
