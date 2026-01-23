# CD Pipeline: Deploy Application from Jenkins to EC2 (TWN Bootcamp)

Dieses Repository dient als **Dokumentation / Referenz auf GitHub** für mein Bootcamp-Projekt.  
Der vollständige Code liegt auf GitLab.

[GitLab Repository] https://gitlab.com/coffeezon3/java-maven-app.git

---



## Projektbeschreibung

Dieses Projekt zeigt, wie man eine Anwendung **automatisch über eine Jenkins-Pipeline auf einer AWS EC2-Instanz deployt**, inklusive Docker-Containerisierung.  

**Ziele:**

1. AWS EC2-Instanz für Deployment vorbereiten (Docker installieren).  
2. SSH-Key-Credentials für die EC2-Instanz in Jenkins anlegen.  
3. Continuous Deployment-Pipeline erweitern:
   - Jenkins baut das Image
   - Jenkins SSH auf EC2
   - Deployment des neuen Docker-Images  
4. Sicherheitsgruppe in EC2 konfigurieren, um den Zugriff auf die Webanwendung zu erlauben.  

---

## 🛠 Technologien

- **Cloud / Infrastruktur:** AWS EC2  
- **CI/CD:** Jenkins Pipeline  
- **Containerisierung:** Docker  
- **Betriebssystem:** Linux  
- **Programmiersprachen & Tools:** Java, Maven, Git, GitLab  
- **Container Registry:** Docker Hub  

---

## Deployment Schritt-für-Schritt

> Hinweis: Um die Anwendung lokal oder auf EC2 zu starten, klone bitte das GitLab-Repo.

```bash
# GitLab-Repo klonen
git clone https://gitlab.com/techworld-with-nana/react-nodejs-example.git
cd react-nodejs-example

# Optional: Docker-Image bauen
docker build -t react-nodejs-example .

# Docker-Container auf EC2 starten
docker run -p 8080:8080 react-nodejs-example

Frontend-Port (Docker-Container): 3080

Backend-Port (Docker-Container): 8080

Auf EC2 läuft der Container aktuell unter:

CONTAINER ID   IMAGE                                PORTS
0b9af121a81d   asdhka/react-nodejs-example:latest   0.0.0.0:8080->8080/tcp

 Jenkins Pipeline Schritte

Build Stage: Maven Build der Anwendung.

Docker Stage: Erstellen und Pushen des Docker-Images in Docker Hub.

Deploy Stage: SSH auf EC2 und Deployment des neuen Docker-Images.

 Hinweise:

GitHub dient nur als Referenz / Dokumentation für das Projekt.

Alle Änderungen werden über GitLab verwaltet.

Aus Sicherheitsgründen keine Secrets / Keys in GitHub pushen.








