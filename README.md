# Windows-focused Cybersecurity Threat Intelligence Knowledge Graph

This project integrates MITRE ATT&CK, NVD/CVE, and CWE data for Windows-focused cybersecurity analysis. It separates the knowledge graph into an ontology file and an instance-data file, then analyses the integrated graph with SPARQL queries in Jupyter.

## Repository files

| File | Purpose |
| --- | --- |
| windows-cyber-threat-ontology.ttl | Ontology schema: classes, object properties, domains, ranges, OWL restrictions, and external UCO alignment notes. |
| windows-cyber-threat-instances.ttl | Instance data: ATT&CK techniques and threat actors, Windows products, CVEs, CWEs, severity levels, and their relationships. |
| importdata.ipynb | Reproducible data-import process. It downloads selected records from MITRE ATT&CK and NVD, adds RDF triples, and exports a Turtle graph. |
| analysis.ipynb | Loads the ontology and instance files, then performs SPARQL queries, tables, and visualisations. |

## Data sources and scope

- MITRE ATT&CK Enterprise STIX data: five selected Windows techniques and their associated threat actors.
- NVD CVE API: four selected Microsoft Windows CVEs: CVE-2024-30051, CVE-2024-30078, CVE-2024-38063, and CVE-2024-38080.
- CWE identifiers and CVSS severity values are taken from the selected NVD records.

The graph connects threat actors to ATT&CK techniques and Windows context. It connects CVEs to affected Windows products, CWEs, and severity levels. It does not claim that an ATT&CK technique directly exploits a particular CVE.

## How to reproduce

1. Install Python 3 and open Jupyter Notebook or VS Code with a Python kernel.
2. Run importdata.ipynb from top to bottom if you want to reproduce the selected data-import process. Internet access is required for the MITRE and NVD sources.
3. Run analysis.ipynb from top to bottom. It installs rdflib, pandas, and matplotlib, loads the two published Turtle files, and produces the query results and charts.

## Ontology IRI

https://github.com/Timoseee/windows-cyber-threat-kg/ontology
