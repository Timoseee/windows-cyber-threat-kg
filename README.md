# Windows focused cybersecurity threat knowledge graph

This project has made a cybersecurity threat knowledge knowledge graph for Windows. It integrated ATT&CK and CVE data through RDF triple in a knowledge graph.

## Requirements

### How to reproduce the project

1. Clone repository
2. Install required packages
3. Run importdata.ipynb. This notebook download selected data and put then in the file.
4. Run analysis.ipynb. This notebook loads windows-cyber-threat-ontology.ttl and windows-cyber-threat-instances.ttl. Then it will run the SPARSQL get the information and creates graph base on data

### Data sources

1. MITRE ATT&CK: https://attack.mitre.org/
2. NVD CVE API: https://nvd.nist.gov/developers/vulnerabilities
3. Unified Cyber Ontology (UCO): https://unifiedcyberontology.org/
