# Transcriptomics EDAM

Transcriptomics EDAM is an ontology developed to model experimental processes and related entities in computational transcriptomics experiments.

## Features

This ontology was developed to improve the __coverage__ of objects, processes, and intermediate states commonly encountered in transcriptomics workflows. It combines the original EDAM ontology (v1.25) and STATO. It also contains terms extracted from transcriptomics publications.

- We introduce an upper-level class, `data status`, to represent transformations where the data type and format remain unchanged but the data content changes.
For example, a dataset may become _filtered_ without changing its file format or structural type.
- We add a `Database` branch, reflecting the fact that database references often implicitly indicate both data types and associated operations.
Due to the large number of named databases, only a representative subset is included in the core ontology (see the `withoutDatabases` folder).
The `withDatabases` folder contains a more comprehensive collection of database names curated manually and sourced from the Nucleic Acids Research (NAR) database collection. However, this version is less actively maintained, as it introduces significant overhead during normalisation.
- To better represent statistical objects and analytical operations, we import relevant branches from an existing statistics ontology.
- We include object properties that capture biological and analytical semantics, such as `has input` and `has means`.
While expressive, their practical use is currently limited due to the high curation cost required for consistent application.
- To further improve coverage, we collected frequently used transcriptomics-related entities from the literature and added them to the ontology.
Definitions and synonyms for these classes were generated using large language models and are currently presented as a flat list.

> During transcriptomics methodology development, this ontology is continuously updated based on manual inspection and practical modelling needs.

### Example Modelling Use Cases

1. How should the statement
“The gene lists were filtered based on differential expression analysis”
be normalised and represented semantically?

2. If a study uses the Gene Expression Omnibus, what types of analyses are implied, and which data formats should be expected and modelled?

### Stats
> withoutDatabase

|Version|Total classes| Branch operation| Branch topic | Branch data| Branch format|
|--|--|--|--|--|--|
|0.0.2|

