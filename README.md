## LDPizer

### Aim of the LDPizer
LDPs are data-driven system and their deployment involves deploying both the data and the system. Current solutions for LDP addresse only the latter part. There is currently no solution for automatizing the deployment of data in LDP.  The aim of the LDPizer is to automatize the deployment of RDF and non-RDF data into LDPs.

### How it works:
The LDPizer takes as input:
1. A design document
2. Some parameters provided by the user which includes at least the base URL of the LDP. If for sending POST request, authentication is required, `username` and `password` have to be specified. Currently, the LDPizer support only basic authentication

The design document is written using the [vocabulary](https://github.com/noorbakerally/LDPDesignVocabulary). For information on how the LDPizer process the design document, refer to the [LDPizer repository](https://github.com/noorbakerally/LDPizer) 

### Demonstration:
1. Deploy the [Paris data catalog](https://opendata.paris.fr/api/v2/catalog/exports/ttl) using the [design document](https://github.com/noorbakerally/ISWC2017Demo/blob/master/ParisCatalog.dd.ttl). An instance of an LDP using this design document is running at http://ci.emse.fr/marmotta/ldp
2.  Deploy the [Toulouse data catalog](https://data.toulouse-metropole.fr/api/v2/catalog/exports/ttl) using modifying the data source of the design document for Paris data catalog.
3. Deploy a [dataset](https://github.com/noorbakerally/ISWC2017Demo/blob/master/ParisGeo.ttl) extracted from LinkGeoData using the [SPARQL Construct Query](https://github.com/noorbakerally/ISWC2017Demo/blob/master/ParisGeo.rq) which relates to geographical places in Paris using a [design document](https://github.com/noorbakerally/ISWC2017Demo/blob/master/ParisGeo.dd.ttl)
