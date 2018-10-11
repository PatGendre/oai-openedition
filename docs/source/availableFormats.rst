Available Formats
============================

Records are available to all in the following metadata formats:

* ``oai_dc``: Dublin Core
* ``qdc``: Qualified Dublin Core
* ``mets``: Metadata Encoding and Transmission Standard

The METS format is available only for journal issues and books. It is not available for blogs, Calenda events, and electronic journals publishing streamed articles.

Furthermore, OpenEdition’s partners have access to full text in TEI (Text encoding initiative) format of OpenEdiiton Journals and OpenEdition Books documents. 

It allows retrieving and indexing the full text of the documents. If you want to get an access to the OpenEdition’s TEI, please contact us at contact@openedition.org.

TEI full text and raw full text for partners
------------------------------------------------------

Link to TEI structured full text and to raw text is also retrivable from OAI in ``qdc`` format.
``qdc`` records provide 2 elements :

* ``<dcterms:hasFormat scheme="TEI">``: link to structured  XML-TEI Full text (suitable for republication and text and dat mining)
* ``<dcterms:hasFormat scheme="BASICTEI">``: link to full text in the "basicTEI" format witch provide metadata of the document in TeiHeader and raw text in the body section (suitable for text indexing). 

If you need to get an access to the OpenEdition’s TEI as a partner, please email us at contact@openedition.org.


**Example**

http://oai.openedition.org/?verb=GetRecord&identifier=oai:revues.org:terrain/16916&metadataPrefix=qdc

.. code-block:: xml
   :linenos:

    <?xml version="1.0" encoding="UTF-8"?>
    <OAI-PMH xmlns="http://www.openarchives.org/OAI/2.0/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.openarchives.org/OAI/2.0/ http://www.openarchives.org/OAI/2.0/OAI-PMH.xsd">
      <responseDate>2018-10-11T20:34:26Z</responseDate>
      <request verb="GetRecord" identifier="oai:revues.org:terrain/16916" metadataPrefix="qdc">http://oai.openedition.org/</request>
      <GetRecord xmlns:qdc="http://epubs.cclrc.ac.uk/xmlns/qdc/" xmlns:dcterms="http://purl.org/dc/terms/">
        <record>
          <header>
        <identifier>oai:revues.org:terrain/16916</identifier>
        <datestamp>2018-10-09T10:04:10Z</datestamp>
        <setSpec>journals</setSpec>
        <setSpec>journals:terrain</setSpec>
        <setSpec>openaire</setSpec>
          </header>
          <metadata>
        <qdc:qualifieddc xmlns:dcterms="http://purl.org/dc/terms/" xmlns:qdc="http://epubs.cclrc.ac.uk/xmlns/qdc/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://purl.org/dc/terms/ http://dublincore.org/schemas/xmls/qdc/2006/01/06/dcterms.xsd http://epubs.cclrc.ac.uk/xmlns/qdc/ http://epubs.cclrc.ac.uk/xsd/qdc.xsd">
          <dcterms:title>Y a-t-il une différence entre « Roms » et « Roumains » ?</dcterms:title>
          <dcterms:type>article</dcterms:type>
          <dcterms:creator>Olivera, Martin</dcterms:creator>
          <dcterms:abstract xml:lang="fr">À première vue, les ethnologues sont bien les spécialistes des « différences » : longtemps ils ont voulu saisir ce qui faisait la singularité de divers groupes humains. Leur discipline a ainsi largement contribué à enrichir (et à ordonner) le vaste tableau de la « diversité culturelle » sur la planète. Au cours des quarante dernières années, l’anthropologie s’est toutefois détournée des approches « primordialistes » ou « essentialistes » des identités collectives. La plupart des chercheurs considèrent aujourd’hui que ces dernières ne sont jamais données mais toujours construites et, plus encore, qu’elles sont en perpétuelle co-construction. Se définir soi-même implique de définir des « autres », voisins proches ou lointaines figures exotiques. C’est ce qu’illustre cet article en partant d’une question en apparence simple : quelle différence y a-t-il entre les « Roms » et les « Roumains » ? Il montre pourquoi on ne peut rendre compte de « différences » que d’un certain point de vue, et pourquoi il importe de rappeler que celles-ci sont toujours relatives et provisoires, même lorsqu’elles se donnent comme évidentes et éternelles. En effet, les figures de l’identité et de l’altérité ne s’(entre)inventent pas de manière hasardeuse, elles sont un produit de l’histoire et visent à agir sur le monde. Elles sont donc éminemment politiques. Sur tous ces points, le cas des « Roms » et des « Roumains » est exemplaire, comme on va le voir.</dcterms:abstract>
          <dcterms:publisher>Association Terrain</dcterms:publisher>
          <dcterms:isPartOf scheme="URN">urn:issn:0760-5668</dcterms:isPartOf>
          <dcterms:publisher>Terrain</dcterms:publisher>
          <dcterms:isPartOf scheme="URN">urn:eissn:1777-5450</dcterms:isPartOf>
          <dcterms:language scheme="RFC1766">fr</dcterms:language>
          <dcterms:issued scheme="W3CDTF">2018-10-01</dcterms:issued>
          <dcterms:identifier scheme="URI">http://journals.openedition.org/terrain/16916</dcterms:identifier>
          <dcterms:accessRights>info:eu-repo/semantics/openAccess</dcterms:accessRights>
          <dcterms:hasFormat scheme="TEI">http://journals.openedition.org/terrain/tei/16916</dcterms:hasFormat>
          <dcterms:hasFormat scheme="BASICTEI">http://journals.openedition.org/terrain/basictei/16916</dcterms:hasFormat>
        </qdc:qualifieddc>
          </metadata>
        </record>
      </GetRecord>
    </OAI-PMH>



