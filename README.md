# Projekt Anleitung

## Inhaltsverzeichnis
1. [Repository klonen](#1-repository-klonen)
2. [Entwicklungsumgebung einrichten](#2-entwicklungsumgebung-einrichten)
3. [README.md erstellen](#3-readmemd-erstellen)
4. [Git verwenden (Commit und Push)](#4-git-verwenden-commit-und-push)
5. [Docker-Container erstellen und verwenden](#5-docker-container-erstellen-und-verwenden)

---

## 1. Repository klonen

Um das Repository zu kopieren, geben Sie den folgenden Befehl ein und ersetzen Sie `<SSH-Schlüssel>` durch den SSH-Link des gewünschten Repositories:

```bash
git clone <SSH-Schlüssel>

## 4. Git verwenden (Commit und Push)

Befolgen Sie diese Schritte, um Änderungen zu committen und hochzuladen:

1. **Änderungen zur Staging-Area hinzufügen**:
    ```bash
    git add .
    ```

2. **Commit erstellen**:
    ```bash
    git commit -m "Beschreibung der Änderungen"
    ```

3. **Änderungen ins Repository hochladen**:
    ```bash
    git push origin main
    ```

    *Hinweis*: Wenn Sie einen anderen Branch verwenden, ersetzen Sie `main` durch den Namen des gewünschten Branches.

## 5. Docker-Container erstellen und verwenden

Mit Docker können Sie Anwendungen in Containern isoliert bereitstellen. Die grundlegenden Schritte dazu sind:

1. **Dockerfile erstellen** (falls noch nicht vorhanden), um alle Schritte für die Containerisierung zu definieren.

2. **Docker-Image bauen**:
    ```bash
    docker build -t <image-name> .
    ```

3. **Container starten**:
    ```bash
    docker run -d -p 3000:3000 <image-name>
    ```

    Dieser Befehl führt den Container im Hintergrund aus (`-d`) und leitet Port `3000` des Containers auf Port `3000` des Hosts weiter.

4. **Docker-Compose verwenden**, um mehrere Container zu verwalten. Erstellen Sie eine `docker-compose.yml` und starten Sie alle Container mit:

    ```bash
    docker-compose up --build
    ```
