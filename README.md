# Windows-focused cybersecurity threat knowledge graph

This project integrates MITRE ATT&CK Enterprise 19.2 and selected NVD CVE records into a Windows-focused RDF knowledge graph.

## Project files

Keep these files in the same directory:

- `importdata.ipynb`
- `analysis.ipynb`
- `windows-cyber-threat-ontology.ttl`
- `windows-cyber-threat-instances.ttl`

Run Jupyter from this directory so the notebooks read and write the expected files.

## Requirements

```bash
pip install rdflib pandas matplotlib jupyter
```

Internet access is required to download the pinned ATT&CK 19.2 data and the four selected NVD records.

## How to reproduce the project

1. Clone this repository and open a terminal in the repository directory.
2. Start Jupyter with `jupyter notebook`.
3. Open `importdata.ipynb` and select **Kernel > Restart Kernel and Run All Cells**.
4. Confirm that `windows-cyber-threat-instances.ttl` is saved in this directory. The current graph contains 760 instance triples.
5. Open `analysis.ipynb` and run all cells. It downloads the ontology and current instance file from this GitHub repository and produces the SPARQL results and charts.
6. The integrated graph contains 808 triples: 48 ontology triples and 760 instance triples.

## Expected data summary

- 132 threat actors
- 5 attack techniques
- 4 attack tactics
- 4 vulnerabilities
- 5 weaknesses
- 2 severity levels
- 18 operating systems

## Data sources

1. [MITRE ATT&CK](https://attack.mitre.org/)
2. [NVD CVE API](https://nvd.nist.gov/developers/vulnerabilities)
3. [Unified Cyber Ontology](https://unifiedcyberontology.org/)
