mets format
=================

The ``mets`` (Metadata Encoding and Transmission Standard) format is available for books and journal issues (more info about types :ref:`types`). The aim of this format is to describe the metadata and the complete structure of the volume (book or journal issue). 

The ``mets`` format is documented on the Library of Congress website: http://www.loc.gov/standards/mets/.

The list of available records in mets format can be found through OAI: http://oai.openedition.org/?verb=ListIdentifiers&metadataPrefix=mets (use :ref:`rToken` to retrieve the complete list).

In OpenEdition OAI, a ``mets`` record is divided into 3 main parts : one ``mets:structMap``, one ``mets:fileSec`` and several ``mets:dmdSec``.


.. _metsstructmap:

1. mets:structMap
---------------------

The ``structMap`` element describes the tree structure of the volume.

``mets:div`` elements are nested to describe the hierarchial organisation of the volume, parts, texts. Each ``mets:div`` element is qualified with the following attributes:

* ``TYPE``:  :ref:`List of document types <types>` 
* ``ORDER``: sequence number whitch defines the order of the documents relative to the parent ``div`` element.
* ``DMDID``: refer to the ``ID`` of the relevant ``mets:dmdSec`` element.
* ``LABEL``: descriptive label (buggy FIXME)


Each ``mets:div`` element refering to a document file have one or several ``mets:fptr`` child element, with a ``FILEID`` refer to the ``ID`` of the relevant ``mets:file`` element.


2. mets:filSec
----------------------

TODO


3. mets:dmdSec
--------------------------

TODO


