# Setup-Anleitung für das Projekt agro-geokg

Diese Anleitung beschreibt, wie du die Entwicklungsumgebung und die notwendigen Komponenten für das Projekt einrichtest.

---

## Voraussetzungen

- Python 3.8 oder höher installiert  
- Git installiert  
- Docker installiert (optional, für Container-Lösung)  
- Microsoft C++ Build Tools (für Windows-Nutzer, zur Installation von GDAL)

---

## Projekt klonen

## Virtuelle Umgebung erstellen und aktivieren
```bash
git clone https://github.com/DeinGitHubBenutzername/agro-geokg.git
cd agro-geokg

python -m venv venv
# Windows
venv\Scripts\activate

# Linux/macOS
source venv/bin/activate

## Abhängigkeiten installieren

pip install -r requirements.txt

## Docker-Container starten
cd docker
docker-compose up -d

## Optional Jupyter Notebook starten
jupyter notebook

## Stramlit-App starten 
streamlit run app/main.py

