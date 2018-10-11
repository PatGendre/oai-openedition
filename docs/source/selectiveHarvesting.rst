Selective Harvesting
========================

The repository allows selective harvesting, by set and by date. Two simple sample queries:

* http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=journals:chs for retrieving a list of records from the journal Crime, History & Societies
* http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&from=2013-03-13 for retrieving a list of records added or updated since 13 march 2013.


Selective harvesting by set
------------------------------

**Example**

* For retrieving the document metadata from the Publications de l’École française de Rome only, you will have to query the ``books:efr`` set: http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=books:efr
* For retrieving metadata from all OpenEdition Journals documents, you will have to query the ``journals`` set: http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&set=journals


More info about available sets: :ref:`sets` 


Selective harvesting by date
------------------------------
The repository allows harvesting by date, i.e. harvesting of records added or updated before or after a specified date

The parameters to use are from or until. The date can have the ``dd-mm-yyyy`` format or the ``dd-mm-yyyyThh:mm:ssZ`` format.

**Example**

http://oai.openedition.org/?verb=ListRecords&metadataPrefix=oai_dc&from=2017-03-13T16:47:48Z will retrieve a list of records added or updated since the 13 march 2017 at 4.47 pm.
