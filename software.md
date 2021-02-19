# HuBMAP Product Offerings: Project Management, Communication, Tracking, & Reporting

### Last Updaed: 2/19/2021 

## Description:
The purpose of this document is to categorize HuBMAP efforts through a product management lens in order to structure conversations around, work linkages to, and dependencies among software development level [epics and features.](https://www.kbp.media/themes-epics-features-user-stories/)

Linked entries below direct you to the associated code repository if one is present.

## [Infratructure/ Base Product](https://camo.githubusercontent.com/60ffedef9700a05ce2cd48d800edc1cf1057f48cc0b5db228d4d0dffd5a3f40c/68747470733a2f2f646f63732e676f6f676c652e636f6d2f64726177696e67732f642f652f32504143582d31765131495356616e696c567433766577553674656b5669724f78507054734b4d53337a586138744c304a354a6a6454397a53396164675869766d315a6358786f79435f6c6374496c485659684a75492f7075623f773d39323226683d343038)
- [API Gateway](https://github.com/hubmapconsortium/gateway/blob/test-release/README.md)
- [Common Coordinate Framework (CCF)](https://github.com/hubmapconsortium/hubmap-ontology/blob/master/README.md)
- [Pipeline Container Orchestration](https://github.com/hubmapconsortium/ingest-pipeline) 
- [Documentation](https://github.com/hubmapconsortium/portal-docs/blob/master/README.md) (on Portal)
  - [CCF Checklist and SOPs](https://hubmapconsortium.github.io/ccf/index.html)
  - [MC-IU Onboarding videos](https://hubmapconsortium.github.io/ccf/index.html)
  - [IVMOOC](https://hubmapconsortium.github.io/ccf/index.html)
- Hybrid Cloud Infrastructure
- [Identity system](https://github.com/hubmapconsortium/uuid-api/blob/test-release/README.md)
- [Knowledge Graph](https://github.com/hubmapconsortium/ontology-api/blob/master/README.md)
  - [Schema](https://github.com/dbmi-pitt/UMLS-Graph/blob/master/README.md)
  - Ontology ingest & API service
  - Base biomedical ontologies
- [Microservices Architecture](https://github.com/hubmapconsortium/commons/blob/test-release/README.md)
  - [Provenance services](https://github.com/hubmapconsortium/provenance-metadata-services/blob/master/README.md)
- [Provenance Graph](https://github.com/hubmapconsortium/entity-api/blob/test-release/README.md) (+ core [database](https://github.com/hubmapconsortium/neo4j-docker/blob/master/README.md) using Docker)
- [User registration](https://github.com/hubmapconsortium/member-ui/blob/master/README.md)
- Monitoring services
- [Data Ingest](https://github.com/hubmapconsortium/ingest-ui/)
- [Data Search](https://github.com/hubmapconsortium/search-api/)
## Tissue/ sample prep/ core data
- Dataset generation by data providers (TMCs, RTIs, TTDs)
  - [See list of assays on Portal](https://portal.hubmapconsortium.org/docs/assays)
- DOI generation (DOI registration service)
- [Protocols registration tool](https://www.protocols.io/workspaces/human-biomolecular-atlas-program-hubmap-method-development)(protocols.io)
## Spatial registration and semantic annotation (via 3D collision detection)
- [ASCT+B Reporter](https://github.com/hubmapconsortium/ccf-asct-reporter/blob/develop/README.md)
- [CCF reference objects](https://github.com/hubmapconsortium/ccf-3d-reference-object-library/blob/master/README.md) (body, organs)
- [CCF registration tool](https://github.com/hubmapconsortium/ccf-3d-registration/blob/master/README.md) (RUI)
## Data & Metadata
Antibody registration tool
Data & metadata standards & documentation
Data ingest tool (data & metadata, sample, assay, antibody report, contributor)
File transfer interface (Globus)
Manual dataset ingest tools
Manual donor data ingest process
Sequencing data dbGaP submission tool
Tissue & donor registration tool
