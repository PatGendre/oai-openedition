qdc format
===================

The qdc format provides the following elements:

1. dcterms:title
-----------------

Title of the document. Non-repeatable.

2. dcterms:alternative
------------------------------------
Alternative title (translated title). Repeatable. An ``xml:lang`` attribute specifies the language of the alternative title.

Available for OpenEdition Journals and OpenEdition Books.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:histoire-education/2589&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:alternative xml:lang="en">The Society for Promoting the Employment of Women in London (1859-late XIXth century): vocational and commercial training for “the surplus woman”</dcterms:alternative>
    <dcterms:alternative xml:lang="de">Der „Verein für Frauenerwerb“ in London (1859 bis Ende des 19. Jahrhunderts) : die kaufmännische Berufsausbildung als Hilfe für „überschüssige Frauen“</dcterms:alternative>

3. dcterms:creator
--------------------------
Author(s) of the document. Repeatable.

Unavailable for Calenda.

.. note :: For Journal Issues and Books, ``dcterms.creator`` provides authors of the issue or the book AND authors of the child articles or chapters.

**Example of a book with multiple authors at chapter level:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/348&metadataPrefix=qdc

4. dcterms:contibutor
---------------------------

Scientific and academic editor of the document. Available for OpenEdition Journals and OpenEdition Books. 

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:cvz/3321&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:contributor>Alvarez Roblin, David</dcterms:contributor>
    <dcterms:contributor>Biaggini, Olivier</dcterms:contributor>


5. dcterms:issued
------------------------
Publishing date of the document on OpenEdition platform. 

If an article was previously published in another format (for instance a print version), the ``dcterms:issued`` element won't provide the date of the previous publishing but only the publishing date of the document on OpenEdition.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/8732&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:issued scheme="W3CDTF">2017-09-01</dcterms:issued>


6. dcterms:accessRights
---------------------------------

Available for the 4 OpenEdition platforms: OpenEdition Books, OpenEdition Journals, Hypothèses et Calenda.

The ``dcterms:accessRights`` element can match the following values :

* ``info:eu-repo/semantics/embargoedAccess`` : articles and journal issues under embargo
* ``info:eu-repo/semantics/openAccess`` : open access document (article, journal issue, book, book section, blog post, event...). At least the html format is freely accessible. The other formats (pdf, epub) may be.
* ``info:eu-repo/semantics/restrictedAccess`` : book and book section in restricted acces.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:ariadnaediciones/158&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:accessRights>info:eu-repo/semantics/openAccess</dcterms:accessRights>


7. dcterms:available
-------------------------

Applicable for OpenEdition Jounals. If ``dcterms:accessRights = "info:eurepo/semantics/embargoedAccess"``, then the ``dcterms:available`` element will provide the end date of embargo (availability date of the document in open access):

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:rfp/5246&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:accessRights>info:eu-repo/semantics/embargoedAccess</dcterms:accessRights>
    <dcterms:available scheme="W3CDTF">2022-01-01</dcterms:available>


8. dcterms:publisher
-----------------------------

``dcterms:publisher`` provides the publisher name.

For OpenEdition Journals and Hypotheses documents ``dcterms:publisher`` provides also the journal or blog title

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:studifrancesi/2636&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:publisher>Rosenberg &amp; Sellier</dcterms:publisher>
    <dcterms:publisher>Studi Francesi</dcterms:publisher>


9. dcterms:identifier
--------------------------------
Identifier of the document. Repeatable.

9.1. URI
^^^^^^^^^
``dcterms:identifier`` with an attribute ``scheme="URI"`` provides the URI of the document.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/5530&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:identifier scheme="URI">http://journals.openedition.org/remi/5530</dcterms:identifier>

9.2. DOI
^^^^^^^^^^
Available for OpenEdition Journals and OpenEdition Books.

``dcterms:identifier`` with an attribute ``scheme="URN"`` and a ``urn:doi`` prefix provides the DOI of the document.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:remi/5530&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:identifier scheme="URN">urn:doi:10.4000/remi.5530</dcterms:identifier>

9.3. ISBN
^^^^^^^^^^
Available for OpenEdition Books.

``dcterms:identifier`` with an attribute ``scheme="URN"`` and a ``urn:isbn`` or ``urn:eisbn`` prefix provides respectively ISBN of the print and electronic version of the book.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/348&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:identifier scheme="URN">urn:eisbn:9782821875470</dcterms:identifier>
    <dcterms:identifier scheme="URN">urn:isbn:9783863951221</dcterms:identifier> 

For OAI records of a book chapter, the ISBN and eISBN provided refer to the parent book of that chapter.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:gup/367&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:identifier scheme="URN">urn:eisbn:9782821875470</dcterms:identifier>
    <dcterms:identifier scheme="URN">urn:isbn:9783863951221</dcterms:identifier>

10. dcterms:isPartOf
----------------------------

Available for OpenEdition Journals.

``dcterms:isPartOf`` with an attribute ``scheme="URN"`` and a ``urn:issn`` or ``urn:eissn`` prefix provides respectively ISSN of the print and electronic version of the journal in which the document was published.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:geocarrefour/10121&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:isPartOf scheme="URN">urn:issn:1627-4873</dcterms:isPartOf>
    <dcterms:isPartOf scheme="URN">urn:eissn:1960-601X</dcterms:isPartOf>

11. dcterms:hasFormat
----------------------------

Available for OpenEdition Journals and OpenEdition Books.

OpenEdition provide partners an access to full text in TEI (`Text Encoding Initiative <http://www.tei-c.org/>`_) format and Raw text format for documents published on OpenEdition Journals and OpenEdition Books. 

Link to TEI structured full text and to Raw text is retrivable in ``dcterms:hasFormat``.

* ``<dcterms:hasFormat scheme="TEI">``: link to structured  XML-TEI Full text (suitable for republication and text and dat mining)
* ``<dcterms:hasFormat scheme="BASICTEI">``: link to full text in the "basicTEI" format witch provide metadata of the document in TeiHeader and raw text in the body section (suitable for text indexing). 

.. note :: Access to Full text in TEI and Raw text format is only available for authorized IP address (OpenEdition partners). More infos :ref:`tei`  

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:geocarrefour/10121&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:hasFormat scheme="TEI">http://journals.openedition.org/geocarrefour/tei/10121</dcterms:hasFormat>
    <dcterms:hasFormat scheme="BASICTEI">http://journals.openedition.org/geocarrefour/basictei/10121</dcterms:hasFormat>


12. dcterms:language
----------------------------------
Document language. RFC1766 format. 

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:cfee/1081&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:language scheme="RFC1766">en</dcterms:language>

.. _type:

13. dcterms:type
-------------------------
Document type

* Possible values for OpenEdition Journals

  * ``issue``
  * ``part``
  * ``article``
  * ``review``
  * ``bibliography``
  * ``introduction``
  * ``archaeological note``
  * ``chapter``
  * ``book``
  * ``other``

* Possible values for OpenEdition Books

  * ``book``
  * ``part``
  * ``chapter``
  * ``bibliography``
  * ``appendix``
  * ``index``
  * ``foreword``
  * ``afterword``
  * ``bibliography``
  * ``review``
  * ``article``
  * ``introduction``
  * ``other``

* Possible values for Hypotheses 

  * ``post``

* Possible values for Calenda 

  * ``call for papers``
  * ``colloquium``
  * ``study days``
  * ``seminar and workshop``
  * ``miscellaneous information``
  * ``scholarship, prize and job offer``
  * ``lectures``
  * ``summer school``
  * ``call for tender``


**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:lectures/27329&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:type>review</dcterms:type>


14. dcterms:rights
---------------------------

Available for OpenEdition Journals and OpenEdition Books. ``dcterms:rights`` may contain license information if provided by the publisher.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:ariadnaediciones/158&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:rights>CC BY-SA 3.0</dcterms:rights>


15. dcterms:extent
-------------------------
Available for OpenEdition Journals and OpenEdition Books.

``dcterms:extent`` may provide the number of pages or the pages range in print edition of the document

**Page range example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:ethnomusicologie/1513&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:extent>240-241</dcterms:extent>

**Number of pages example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:purh/7891&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:extent>132</dcterms:extent>


16. dcterms:spatial
---------------------------
Available for OpenEdition Journals and OpenEdition Books.

``dcterms:spatial`` may contain spatial topics of the document.

**Example:** 
http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:balkanologie/717&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:spatial>Bulgarie</dcterms:spatial>
    <dcterms:spatial>Turquie</dcterms:spatial>


17. dcterms:temporal
-------------------------
Available for OpenEdition Journals and OpenEdition Books.

``dcterms:temporal`` may contain temporal characteristics of the document.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:dam/460&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:temporal>âge du Bronze</dcterms:temporal>
    <dcterms:temporal>Néolithique</dcterms:temporal>

18. dcterms:subjects
---------------------------

18.1 Keywords
^^^^^^^^^^^^^^^^^^

Available for OpenEdition Journals and OpenEdition Books. 
``dcterms:subjects`` with a attribute ``scheme="keywords"`` may contains keywords. An ``xml:lang`` attribute specifies the language of the keyword.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:belgeo/20507&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:subject xml:lang="fr" scheme="keywords">détection de communautés</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">champs d’interactions</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">migration</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">navettes</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">provinces</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">Belgique</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">Census11</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">community detection</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">interaction fields</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">migration</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">commuting</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">provinces</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">Belgium</dcterms:subject>
    <dcterms:subject xml:lang="en" scheme="keywords">Census11</dcterms:subject>

18.2 Other Subjects
^^^^^^^^^^^^^^^^^^^^^^
For OpenEdition Books only, ``dcterms:subjects`` may also contains terms from `BISAC <https://bisg.org/page/BISACSubjectCodes>`_, `BIC <https://ns.editeur.org/bic_categories>`_, `ISI <https://en.wikipedia.org/wiki/Institute_for_Scientific_Information>`_ classification. The ``scheme`` attribute specifies the classification.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:books.openedition.org:pum/21469&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:subject xml:lang="fr" scheme="keywords">environnement</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">protection</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">gestion</dcterms:subject>
    <dcterms:subject xml:lang="fr" scheme="keywords">politique gouvernementale</dcterms:subject>
    <dcterms:subject scheme="ISI">Environmental Studies</dcterms:subject>
    <dcterms:subject scheme="ISI">Political Science</dcterms:subject>
    <dcterms:subject scheme="BISAC">POL044000</dcterms:subject>
    <dcterms:subject scheme="BIC">RND</dcterms:subject>

 
19. dctems:abstract
--------------------------------

``dcterms:abstract`` provides abstracts of the document. Abstacts may be available in several languages specified by the ``xml:lang`` attribute.

**Example:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:yod/2597&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:abstract xml:lang="en">This article argues show that the emergence in the 1990s of a second wave of Holocaust‑era restitution claims was not the result of a shift in mentalities leading to the sudden recognition of past wrongs or the surge of repressed memories but rather part of a larger process involving major transformations in global capitalism and property regimes. Restitution, fashioned as re‑privatization, surfaced in the early 1990s in connection with post‑Communist de‑collectivization and was included in neoliberal reform packages adopted by transitional societies in Central and Eastern Europe. By the end of that decade, restitution attained a much wider significance as a token of justice, memory, and identity. International scrutiny of restitution mechanisms implemented by post‑Communist states turned the restoration of property rights into an indicator of these societies’ commitment to human rights and their willingness to address the legacies of their totalitarian past. As a “travelling concept” linking private property with novel ideas of historical justice on its road from east to west and west to east, restitution gradually changed from a method of advancing privatization and creating new polities to a carrier of the memory of past wrongs. In this entirely new meaning, restitution became the heart of Holocaust survivors’ fin‑de‑siècle call for justice and recognition.</dcterms:abstract>
    <dcterms:abstract xml:lang="fr">Cet article tend à montrer que l’émergence, dans les années 1990, d’une deuxième vague de demandes de restitutions de la part de victimes de la Shoah n’était pas le résultat d’un changement de mentalités qui aurait conduit à la reconnaissance soudaine des fautes du passé ou au retour de souvenirs refoulés, mais qu’elle s’est inscrite dans un processus plus vaste impliquant des transformations majeures dans le capitalisme mondial et le statut de la propriété privée. Cette politique de restitution, conçue comme une nouvelle privatisation, a vu le jour au cours de cette période dans le cadre de la décollectivisation postcommuniste et a été partie intégrante des programmes de réforme néolibérale adoptés par les sociétés en transition d’Europe centrale et orientale. À la fin de cette décennie, elle a revêtu une signification beaucoup plus large en tant que geste symbolique de justice, de mémoire et d’identité. Sous le regard attentif porté au plan international sur les mécanismes de restitution mis en œuvre par les États postcommunistes, la restauration des droits de propriété est devenue un indicateur de l’engagement de ces sociétés dans le domaine des droits de l’homme et de leur volonté d’assumer l’héritage de leur passé totalitaire. En tant que « concept itinérant » liant la propriété privée à des idées neuves de justice historique sur sa route d’est en ouest et d’ouest en est, la restitution a évolué progressivement : d’abord moyen de promotion de la privatisation et de la mise en place de politiques nouvelles, elle est devenue porteuse de la mémoire des fautes du passé. Dans ce sens, la restitution est en cette fin de siècle au cœur de la demande des survivants de la Shoah pour la justice et la reconnaissance.</dcterms:abstract>
    <dcterms:abstract xml:lang="he">תקציר: המאמר מנסה להוכיח כי הגל החדש של תביעות הפיצויים מצד קורבנות השואה בשנות ה-90 של המאה הקודמת אינו פועל יוצא של מנטאליות חדשה כתוצאה מהתעוררותם של זיכרונות מודחקים או מהכרה בשגיאות העבר. הוא מהווה חלק מתהליך רחב יותר של שינויים בתפישת הקפיטליזם העולמי והרכוש הפרטי. מדיניות הפיצויים בתקופה זו היא תוצאה של הפרטה חדשה במסגרת הדה-קולקטיביזם בתקופה הפוסט-קומוניסטית וחלק מרפורמה נאו-ליברלית בחברות המשתנות במזרח אירופה ובמרכזה. בסיומו של עשור שנים זה היא קיבלה משמעות רחבה של מחווה סמלית לצדק, לזיכרון ולזהות. תוך תשומת לב ניכרת לתכנית הפיצויים הבין-לאומית, הפכה החזרת זכויות הרכוש במדינות הפוסט-קומוניסטיות לציון של מחויבותן של אלו לזכויות האדם ולרצונן ליישם את שירשו מן העבר הטוטליטארי. מדיניות הפיצויים, כמושג מובילי הקושר את הרכוש הפרטי לתפישת הצדק ההיסטורי על התוואי שבין מזרח למערב ולהיפך, השתנתה באופן הדרגתי: מאמצעי לקידום ההפרטה וליישום דרכים חדשות, היא הפכה למגלמת זכרן של שגיאות העבר. במובן זה תביעות הפיצויים של ניצולי השואה בסוף המאה הקודמת הן בקשה לצדק ולהכרה.</dcterms:abstract>


20. dcterms:bibliographicalCitation
---------------------------------------------

Available for OpenEdition Journals, for ``issue`` documents only (see :ref:`type`). 

.. note :: Only covers a small part of journal issues.

Elements ``dcterms:bibliographicalCitation.issue`` and ``dcterms:bibliographicalCitation.volume`` provides the issue number ans the volume number.

**Example with issue only:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:beo/787&metadataPrefix=qdc

.. code-block:: xml
    :linenos:
    
    <dcterms:bibliographicCitation.issue>61</dcterms:bibliographicCitation.issue>

 
**Example with issue and volume:** http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:ejas/7622&metadataPrefix=qdc

.. code-block:: xml
    :linenos:

    <dcterms:bibliographicCitation.volume>4</dcterms:bibliographicCitation.volume>
    <dcterms:bibliographicCitation.issue>2</dcterms:bibliographicCitation.issue>

