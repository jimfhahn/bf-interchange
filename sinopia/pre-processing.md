The original Sinopia data are close to being converted natively because it follows the BIBFRAME ontology.

There are a few places where we may want to pre-process labels that the current BIBFRAME namespace used in the RDF Syntax processing tool is not interpreting. 

An example pre-processing input and output is shown here. Several lables are removed and one URI is added as a pre-processing step. Thereafter the RDF Syntax processing tool Rapper ( https://hub.docker.com/repository/docker/jimfhahn/raptor-rdf-syntax-library ) references the BIBFRAME namespace using this command:

`rapper -i ntriples -o rdfxml-abbrev -f 'xmlns:bf="http://id.loc.gov/ontologies/bibframe/"' -f 'xmlns:bflc="http://id.loc.gov/ontologies/bflc/"' -f 'xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"' -f 'xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"' -f 'xmlns:mads="http://www.loc.gov/mads/rdf/v1#"' -f 'xmlns:skos="http://www.w3.org/2004/02/skos/core#"' -f 'xmlns:rdau="http://rdaregistry.info/Elements/u/"' -f 'xmlns:sinopia="http://sinopia.io/vocabulary/"'  eefaa9d0-3bac-4827-87fc-1e01f9b29904.nt > eefaa9d0-3bac-4827-87fc-1e01f9b29904.xml
`

and produces the output XML found in the pre-processed instance folder. 

This is the example modification, with the original on the left (red are removed lines) and the new pre-processed nq on the right (green is the addition):

<img width="1113" alt="Screen Shot 2022-06-01 at 12 18 50 PM" src="https://user-images.githubusercontent.com/1310509/171465932-ed787bd5-a2d3-4512-bf5e-1c123db2b5f4.png">
