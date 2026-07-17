![Python Version](https://img.shields.io/badge/python-3.13-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Repo Size](https://img.shields.io/github/repo-size/FrankFreibothe/agro-geokg)


# agro-geokg

## DEUTSCH

Wissensgraph-gestützte Planung und Analyse landwirtschaftlicher Infrastrukturen

Dieses Projekt ist ein Prototyp, der **räumliche Daten (Felder, OSM-Wege, NDVI-Raster) mit semantischem Wissen** verbindet.  
Ziel ist es, komplexe räumlich-semantische Abfragen zu ermöglichen, z. B.:

- Welche Wege liegen innerhalb bestimmter Testgebiete?
- Mittlerer NDVI auf landwirtschaftlichen Flächen?
- Welche Flächen liegen innerhalb bestimmter Gebiete?

---
## Features

- Integration von GeoJSON-, Raster- und RDF-Daten
- Erstellung eines semantischen Knowledge Graphs
- Berechnung mittlerer NDVI-Werte je Landwirtschaftsfläche
- Verknüpfung räumlicher und semantischer Informationen
- SPARQL- und GeoSPARQL-Abfragen
- Interaktive Visualisierung mit Folium

## Beispielkarte

![NDVI Map](docs/ndvi_map_example.png)

---

## Komponenten

- **Datenhaltung:** GeoJSON, Rasterdaten, RDF/Turtle, Blazegraph
- **Ontologien:** eigene OWL-Domänenontologie, SKOS-Konzepte
- **Integration:** Python (GeoPandas, rasterio, RDFLib, Folium)
- **Abfragen:** SPARQL, GeoSPARQL
- **Visualisierung:** Folium, Matplotlib, Jupyter Notebooks

---

## Jupyter Notebooks

| Notebook | Description |
|----------|-------------|
| 01 | NDVI analysis and visualization |
| 02 | Convert agricultural polygons to RDF |
| 03 | Convert OSM road network to RDF |
| 04 | Convert test area to RDF |
| 05 | Merge RDF datasets into one Knowledge Graph |
| 06 | Execute SPARQL queries |
---
## Technologies

- Python
- GeoPandas
- Rasterio
- RDFLib
- GeoSPARQL
- SPARQL
- SKOS
- Folium
- Jupyter Notebook
---

GeoJSON
        \
Raster -----> Python -----> RDF -----> Blazegraph
        /                     |
OSM --------------------------+
                              |
                           SPARQL
                              |
                         Folium Maps
---
## Example SPARQL Query

```sparql
SELECT ?field ?ndvi
WHERE {
    ?field rdf:type agro:AgriculturalArea .
    ?field agro:meanNDVI ?ndvi .
}
ORDER BY DESC(?ndvi)
```
## Results

The prototype demonstrates how geospatial and semantic technologies can be combined to support spatial decision making.

The resulting Knowledge Graph enables:

- semantic querying with SPARQL
- integration of heterogeneous geospatial data
- enrichment of spatial objects with NDVI information
- interactive visualization of analysis results

---
---

## ENGLISH

Knowledge Graph–based Planning and Analysis of Agricultural Infrastructure

This project is a prototype that **links spatial data (fields, OSM roads, NDVI raster) with semantic knowledge**.  
The goal is to enable complex spatial-semantic queries, e.g.:

- Which roads are located within specific test areas?
- Average NDVI of agricultural plots
- Which areas lie within defined zones?

---

## Example Map

![NDVI Map](docs/ndvi_map_example.png)

---

## Components

- **Data storage:** GeoJSON, raster data, RDF/Turtle, Blazegraph
- **Ontologies:** custom OWL domain ontology, SKOS concepts
- **Integration:** Python (GeoPandas, rasterio, RDFLib, Folium)
- **Queries:** SPARQL, GeoSPARQL
- **Visualization:** Folium, Matplotlib, Jupyter Notebooks

---

## Folder Structure

- `data/` → GIS data (raw & processed)  
- `ontology/` → OWL ontology(ies)  
- `notebooks/` → Jupyter notebooks (NDVI, RDF, visualization)  
- `scripts/` → Python scripts for ETL & SPARQL queries  
- `docs/` → screenshots & technical documentation

## Example Geospatial Workflow

This repository also contains example geospatial analyses implemented in Python.

### NDVI Field Analysis

This notebook demonstrates a small geospatial workflow:

1. Load agricultural field polygons and OSM road data  
2. Calculate mean NDVI values for agricultural fields  
3. Reproject raster data for web visualization  
4. Create an interactive map using Folium

### Workflow

![Workflow](docs/workflow_diagram.png)

### Example Output

![NDVI Map](docs/map_preview.png)
