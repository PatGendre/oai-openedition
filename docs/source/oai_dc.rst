oai_dc format
===================

The oai_dc format provides th following elements

dc:title
-----------------

Title of the document. Non-repeatable.

dc:creator
-----------------
Author(s) of the document. Repeatable.

Unavailable for Calenda (records of the set ``events``)

For Journal Issues and Books, ``dc.creator`` provides authors of the issue or the book AND authors of the child articles or chapters.

**Example of a book with multiple authors at chapter level**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/348&metadataPrefix=oai_dc

dc:contibutor
-----------------
Unused


dc:date
-----------------
Publishing date of the document on OpenEdition platform. 

If an article was previously published in another format (for instance a print version), the ``dc:date`` element won't provide the date of the previous publishing but only the publishing date of the document on OpenEdition.

For OpenEdition Journals only, and according to `OpenAIRE 3.0 guidelines (Embargo End Date) <https://guidelines.openaire.eu/en/latest/literature/field_embargoenddate.html#dc-date-embargo>`_, if ``dc:rights = "info:eu-repo/semantics/embargoedAccess"``, then an extra ``dc.date`` element with a prefix ``info:eu-repo/date/embargoEnd/`` will provide the end date of embargo (availability date of the document in open access):

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/8732&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:

    <dc:rights>info:eu-repo/semantics/embargoedAccess</dc:rights>
    <dc:date>info:eu-repo/date/embargoEnd/2021-01-01</dc:date>

dc:publisher
-----------------

``dc:publisher`` provides the publisher name.

For OpenEdition Journals and Hypotheses documents ``dc:publisher`` provides also the journal or blog title

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:studifrancesi/2636&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:publisher>Rosenberg &amp; Sellier</dc:publisher>
    <dc:publisher>Studi Francesi</dc:publisher>


dc:identifier
-------------------
Identifier of the document. Repeatable.

URL
^^^^
``dc:identifier`` provides without prefix the URL of the document.

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/5530&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:

    <dc:identifier>http://journals.openedition.org/remi/5530</dc:identifier>

DOI
^^^^^^^
Available for OpenEdition Journals and OpenEdition Books.

``dc:identifier`` with ``urn:doi`` prefix provides the DOI of the document.

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/5530&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:

    <dc:identifier>urn:doi:10.4000/remi.5530</dc:identifier>

ISBN
^^^^^^
Available for OpenEdition Books.

``dc:identifier`` with ``urn:isbn`` and ``urn:eisbn`` prefix provides respectively ISBN of the print and electronic version of the book.

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/348&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:identifier>urn:eisbn:9782821875470</dc:identifier>
    <dc:identifier>urn:isbn:9783863951221</dc:identifier>

For OAI records of a book chapter, the ISBN and eISBN provided refer to the parent book of that chapter.

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/367&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:identifier>urn:eisbn:9782821875470</dc:identifier>
    <dc:identifier>urn:isbn:9783863951221</dc:identifier>

dc:language
-----------------
Document language. RFC1766 format. 

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:cfee/1081&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:language>en</dc:language>

dc:type
-----------------
Document type

OpenEdition Types
^^^^^^^^^^^^^^^^^^^^^^

* Possible values for OpenEdition Journals

  * ``issue``
  * ``article``
  * ``review``
  * ``section``
  * other non-controlled values

* Possible values for OpenEdition Books

  * ``book``
  * ``chapter``
  * ``bibliography``
  * other non-controlled values

* Possible values for Hypotheses 

  * ``post``

* Possible values for Calenda 

  * ``appel a contribution``
  * ``colloque``
  * ``journee d'etude``
  * ``seminaire``
  * ``informations diverses``
  * ``bourse prix et emploi``
  * ``cycle de conferences``
  * ``ecole d'ete``
  * ``appel d'offres``

OpenAIRE Types (OpenEdition Journals and Openedition Books)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For OpenEdition Journals and OpenEdition Books, and according to `OpenAIRE 3.0 guidelines (Publication Type) <https://guidelines.openaire.eu/en/latest/literature/field_publicationtype.html>`_, an extra ``dc.type`` element with a prefix ``info:eu-repo/semantics/`` will provide the publication type with the following vocabulary:

* ``info:eu-repo/semantics/article``
* ``info:eu-repo/semantics/review``
* ``info:eu-repo/semantics/book``
* ``info:eu-repo/semantics/bookpart``
* ``info:eu-repo/semantics/other``

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:lectures/27329&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:type>review</dc:type>
    <dc:type>info:eu-repo/semantics/review</dc:type>


dc:rights
-----------------

License
^^^^^^^^

Available for OpenEdition Journals and OpenEdition Books. 
``dc:rights`` may contain license information if provided by the publisher.


OpenAIRE Access Level (OpenEdition Journals and Openedition Books)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For OpenEdition Journals and OpenEdition Books, and according to `OpenAIRE 3.0 guidelines (Access Level) <https://guidelines.openaire.eu/en/latest/literature/field_accesslevel.html>`_, an extra ``dc.rights`` element with a prefix ``info:eu-repo/semantics/`` will provide the publication type with the following vocabulary:

* ``info:eu-repo/semantics/embargoedAccess``
* ``info:eu-repo/semantics/restrictedAccess``
* ``info:eu-repo/semantics/openAccess``

**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:ariadnaediciones/158&metadataPrefix=oai_dc

.. code-block:: xml
    :linenos:
    
    <dc:rights>CC BY-SA 3.0</dc:rights>
    <dc:rights>info:eu-repo/semantics/openAccess</dc:rights>


dc:coverage
-----------------


dc:subjects
-----------------


dc:source
-----------------


dc:description
-----------------


