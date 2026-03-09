![Python Version](https://img.shields.io/badge/python-3.13-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Repo Size](https://img.shields.io/github/repo-size/FrankFreibothe/agro-geokg)


## Beispielkarte

![NDVI Map](docs/ndvi_map_example.png)

"# agro-geokg" 



**Wissensgraph-gestützte Planung und Analyse landwirtschaftlicher Infrastrukturen**

Dieses Projekt ist ein Prototyp, der **räumliche Daten** (z. B. Felder, Wege, Glasfasertrassen, Sensorstandorte) mit **semantischem Wissen** verbindet.  
Ziel ist es, komplexe räumlich-semantische Abfragen zu ermöglichen, wie z. B.:

- Welche Felder sind weiter als 200 m von der nächsten Glasfaserleitung entfernt?
- Welche Sensoren messen Bodenfeuchte auf Feldern mit Maisbestand und lehmigem Boden?
- Welche Leitungstrassen kreuzen Naturschutzgebiete oder feuchte Böden?

## Komponenten
- **Datenhaltung:** PostGIS, GraphDB oder Blazegraph  
- **Ontologien:** GeoSPARQL, AGROVOC, eigene Domänenontologie  
- **Integration:** Python (RDFLib, GeoPandas, GDAL)  
- **Abfragen:** SPARQL (GeoSPARQL), ggf. kombiniert mit SQL  
- **Visualisierung:** QGIS, Streamlit/Dash, Leaflet  

## Ordnerstruktur

data/ # GIS-Daten (roh & verarbeitet)
ontologies/ # OWL/Ontologien
notebooks/ # Jupyter-Notebooks (Analyse, SPARQL)
scripts/ # Python-Skripte für ETL & Abfragen
app/ # Streamlit/Dash-App
docs/ # Technische Dokumentation
docker/ # Docker-Configs (PostGIS, GraphDB, Jupyter)
