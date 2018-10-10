Selective Harvesting
========================

The repository allows selective harvesting, by set and by date. Two simple sample queries:

* http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=journals:chs for retrieving a list of records from the journal Crime, History & Societies
* http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&from=2013-03-13 for retrieving a list of records added or updated since 13 march 2013.


Selective harvesting by set
------------------------------
The repository allows selective harvesting with the set parameter. The repository is divided in two kinds of set: platform sets, and publication sets.

The platform sets are:

* A journals set, containing all records from Revues.org.
* A books set, containing all records from OpenEdition Books.
* A blogs set, containing all records from Hypotheses.
* An events set, for all records from Calenda.

As for the publication sets, they allow retrieving records from specific publication within a platform (except Calenda). The name of the publication sets follows the pattern ``<platform set ID>:<publication ID>``:

==============================  =============
Set name Pattern                Example
==============================  =============
journals:<journal website ID>   journals:chs
books:<publisher website ID>    books:obp
blogs:<blog ID>                 blogs:cpa
==============================  =============

Examples

* For retrieving the document metadata from the Publications de l’École française de Rome only, you will have to query the ``books:efr`` set: http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=books:efr
* For retrieving metadata from all OpenEdition Journals documents, you will have to query the ``journals`` set: http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=journals

The comprehensive list of the sets can be retrieved with the query http://oai.openedition.org/?verb=ListSets

More info: :ref:`sets` 

