# SPARQL-Datrans
## Introduction
This repository includes a list of SPARQL queries that enable to transform the data of BIM models in IFC4 to the SimModel specification.
Two alternatives are provided depending on the format of the source:

Input (source):

RDF model expressed according to the ifcOWL ontology.

XML document expressed according to the ifcXML XSD schema.


Transformation languages:

(1) **SPARQL Construct** queries (source: RDF models)

(2) **SPARQL-Generate** queries (source: XML documents)


Output:

RDF model expressed according to the SimModel ontology.


## Usage
You can implement a routine to process SPARQL queries using some of the existing libraries (Jena, DotNetRDF, etc.) depending on the programming language you prefer (Java, C #, etc.).

- Apache Jena Library: https://jena.apache.org/download

- DotNetRDF library: https://www.dotnetrdf.org/

Alternatively, we provide a Java utility that enables to transform IFC RDF models expressed according to the ifcOWL ontology, and IFC XML models expressed according to the ifcXML XSD schema, into SimModel RDF models.

To convert an input RDF model (IFC4/ifcOWL) to an output RDF model (SimModel):

java -jar datrans.jar -c <input_file.rdf> <output_file.rdf>

To convert an input RDF model (IFC4/ifcXML) to an output RDF model (SimModel): 

java -jar datrans.jar -g <input_file.xml/.ifcxml> <output_file.rdf>


## Test files
This repository contains some test files used to check the result of the data transformations carried out through the both SPARQL languages. You can find these files in the 'tests' folder. Note that these are tests performed with BIM models and exported to IFC4 in the STEP and XML format. Tools can be used to transform the files in STEP format into RDF. For example <a href="https://github.com/pipauwel/IFCtoRDF">IFCtoRDF</a>.


## Publications
The following article refers to the context in which the development of the queries in both SPARQL languages has been carried out:

- Publication currently in revision.

Other related publications:

- Sicilia, Á., & Costa, G. (2017, December). Energy-Related Data Integration Using Semantic Data Models for Energy Efficient Retrofitting Projects. In Multidisciplinary Digital Publishing Institute Proceedings (Vol. 1, No. 7, p. 1099). https://www.researchgate.net/publication/321581536_Energy-Related_Data_Integration_Using_Semantic_Data_Models_for_Energy_Efficient_Retrofitting_Projects

- Costa, G., & Sicilia, Á. (2017, November). Methodology for data integration using SPARQL Constructs in the AEC industry. In Proceedings of the 5th Linked Data in Architecture and Construction Workshop (LDAC2017), Dijon, France (pp. 13-15). https://www.researchgate.net/publication/320870777_Methodology_for_data_integration_using_SPARQL_Constructs_in_the_AEC_industry

- O’Donnell, J., See, R., Rose, C., Maile, T., Bazjanac, V., & Haves, P. (2011). SimModel: A domain data model for whole building energy simulation. In 12th Conference of International Building Performance Simulation Association (pp. 382–389). Sydney. Retrieved from http://escholarship.org/uc/item/70c7j74t.

- Pauwels, P., Corry, E., & O’Donnell, J. (2014). Representing SimModel in the web ontology language. American Society of Civil Engineers, 2271–2278. http://doi.org/http://dx.doi.org/10.1061/9780784413616.282.


## License
Licensed under the Apache License, Version 2.0.


## Acknowledgements
Part of this work has been conducted within the project "Optimised Energy Efficient Design Platform for Refurbishment at District Level", which has received funding from the European Union Horizon 2020 Framework Pro-gramme (H2020/2014-2020) under grant agreement n° 680676.


## Issues - contact
You can report any errors that you found to the authors: goncal.costa@salle.url.edu, alvaro.sicilia@salle.url.edu.


