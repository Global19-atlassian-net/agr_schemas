[![Build Status](https://travis-ci.org/alliance-genome/agr_schemas.svg?branch=development)](https://travis-ci.org/alliance-genome/agr_schemas)
Alliance JSON Ingest Schemas and Data Dictionary
================

This directory contains JSON schemas used to define data for integration into the Alliance of Genome Resources and defines the data dictionary of the Alliance data store.


Validation
----------
The python script "agr_validate.py" can be used to validate a JSON entry against a schema for testing/development purposes.
Usage is as follows: 
`agr_validate.py -d test_data.json -s base_schema.json`

For the basic Gene info file run
   `./agr_validate.py -d <your_new_gene_file.json> -s  gene/geneMetaData.json`
for the disease info file run
   `./agr_validate.py -d <your_new_disease_file.json> -s  disease/diseaseMetaDataDefinition.json`
and for the allele info file run
   `./agr_validate.py -d <your_new_allele_file.json> -s  allele/alleleMetaData.json`

The java script "agr_validate_schema.sh" can be used to validate that the schema file itself conforms to the draft-4 version of the JSON schema spec and will run on PR into master.  

For validating all schema files in a branch: 
`./agr_validate_schema.sh`


Data Dictionary
---------------

The Alliance Data Dictionary is a set of information that describes the content, format and structure of the nodes and relations in the Alliance data store. metaschema.yaml defines the potential content of each sub-schema.  Each file is named according to its corresponding node label.  

