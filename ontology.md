# Open Regulation Document Standard (ORDS) Ontology

## Specification

The Open Regulation Document Standard (ORDS) is an RDF vocabulary designed to provide a common set of metadata to describe documents published online by regulatory organisations.

Regulators who publish ORDS metadata for online documents increase discoverability and enable data re-users to more easily combine data from multiple regulatory sources.

The ORDS properties are described below. All properties are optional although users are encouraged to implement all applicable properties for each published document to maximise the usable data available.

You can find examples and some tools to experiment with implementing the standard in the document “ORDS Examples”.

## ORDS Classes:

There is currently only one class defined in the vocabulary. All regulatory documents described by this property are expected to be members of this class.

| Class Name | regulatorDocument |
| --- | --- |
| URI | <https://www.gov.uk/def/ords/regulatorDocument> |
| Label | Regulatory Document |
| Definition | A document published online by a regulator. |
| Subclass of | <http://purl.org/dc/terms/BibliographicResource> |
| Implementation Notes | This class is used to identify and group all documents described by the ORDS metadata. |
| Information Use | It’s useful to have a single property type that can be used to identify all regulator documents. |

## ORDS Properties:

The majority of the properties in the ORDS standard are a restatement of properties from the [Dublin Core vocabulary](https://www.dublincore.org/) with a recommended implementation pattern (listed at the end of this document). The four properties created specifically for ORDS are listed below.

### ORDS Vocabulary Properties:

| Property Name | regulatoryTopics |
| --- | --- |
| URI | <https://www.gov.uk/def/ords/regulatoryTopics> |
| Label | Regulatory Topics |
| Definition | The regulatory subject areas of the document. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | This is the subject area of regulation of the document. Documents can have more than one regulatory topic. |
| Information Use | Recording information on regulatory subjects provides information for search engines, especially to help users find relevant documents when they don't know the exact document they are looking for as well as relating documents in the same regulatory area. |

| Property Name | status |
| --- | --- |
| URI | <https://www.gov.uk/def/ords/status> |
| Label | Status |
| Definition | The legal status of the document. This property is used to determine if a document is in force. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | This is the legal status of the document. Documents should only have one legal status that may need to be updated over time, e.g. if the document is superseded by another document. |
| Information Use | A property to explicitly record the legal status of a document is essential to allow users and search engines to identify legally binding documents. |
| Controlled List | Active |
|| Not active |
|| Superseded |

| Property Name | dateUploaded |
| --- | --- |
| URI | <https://www.gov.uk/def/ords/dateUploaded> |
| Label | Date Uploaded |
| Definition | The date that the document was uploaded to the Open Regulation Platform. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | xsd:date |
| Implementation Notes | The date that the document was first uploaded to the Open Regulation Platform in xsd:date format yyyy-mm-dd, e.g. 2023-12-18. This property should occur once for all documents uploaded to the Open Regulation Platform. |
| Information Use | This value is essential for the management of data in the Open Regulation Platform and for any Open Regulation Platform data re-users to track changes to public data. |

| Property Name | relatedLegislation |
| --- | --- |
| URI | <https://www.gov.uk/def/ords/relatedLegislation> |
| Label | Related Legislation |
| Definition | This property is used to relate a document to the legislation that enables or enforces it |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | xsd:anyURI |
| Implementation Notes | This property should relate the document to the URI of an item of legislation of the [www.legislation.gov.uk](http://www.legislation.gov.uk) website. This property may be repeated if there is more than one related item of legislation. |
| Information Use | Relating documents to legislation allows users to understand (and track) the legal basis for regulations. |

### Dublin Core Vocabulary Properties:

| Property Name | title |
| --- | --- |
| URI | <http://purl.org/dc/terms/title> |
| Label | Title |
| Definition | Title of the document. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | This property should record the title of the document. Documents may have more than one title, especially if printed in multiple languages. |
| Information Use | The document title is essential to identify and display the document correctly. |

| Property Name | identifier |
| --- | --- |
| URI | <http://purl.org/dc/terms/identifier> |
| Label | Identifier |
| Definition | An unambiguous reference to the document, usually a stable URL. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Ideally this identifier should be unique, permanent and provide a mechanism to locate the document, e.g. a URI that resolves. It’s possible that a document may have more than one identifier. In this case some indication of the canonical identifier would be beneficial. |
| Information Use | Recording identifier(s) for documents helps organise data in document management systems and provides a mechanism for citations and referencing. |

| Property Name | publisher |
| --- | --- |
| URI | <http://purl.org/dc/terms/publisher> |
| Label | Publisher |
| Definition | The organisation responsible for the document. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | This property should record the regulator publishing the document. |
| Information Use | It's important to know which organisation is responsible for a document for accountability, provenance and document management. |

| Property Name | language |
| --- | --- |
| URI | <http://purl.org/dc/terms/language> |
| Label | Language |
| Definition | Language(s) the document is written in. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | [ISO 639-3 codes](https://iso639-3.sil.org/) |
| Implementation Notes | This should be used to explicitly record the language(s) the document is written in, which will usually be English, using the three-letter ISO 639-3 code, e.g. “eng”. |
| Information Use | Stating the language(s) of a document helps accessibility, e.g. browsers can be set to default to the Welsh version of a document. |
| Controlled List | eng |
|| cym |

| Property Name | format |
| --- | --- |
| URI | <http://purl.org/dc/terms/format> |
| Label | Format |
| Definition | Format of the document, e.g. PDF, HTML |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://purl.org/dc/terms/MediaType> |
| Implementation Notes | This should be the [Internet Assigned Numbers Authority (IANA) media type](https://www.iana.org/assignments/media-types/media-types.xhtml) of the document, e.g. “application/pdf”. |
| Information Use | Recording the format of a document assists in document management, tracking formats and technical needs for access. |
| Controlled List | PDF |
|| HTML |
|| MS Word |
|| ODF |
|| ODT |
|| Rich Text |

| Property Name | description |
| --- | --- |
| URI | <http://purl.org/dc/terms/description> |
| Label | Description |
| Definition | A brief description of the document. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | This should consist of a sentence or two describing the content and purpose of the document. |
| Information Use | Including a short description of a document can improve search engine optimisation and the way the document appears in search results by providing a text snippet that summarises the document. |

| Property Name | issued |
| --- | --- |
| URI | <http://purl.org/dc/terms/issued> |
| Label | Date Issued |
| Definition | Date that the document was formally issued. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | xsd:date |
| Implementation Notes | The date that the document was formally issued (published) in xsd:date format yyyy-mm-dd, e.g. 2023-12-18. |
| Information Use | The issue date is important to let users know when a document became available and to allow document management and data re-use. |

| Property Name | modified |
| --- | --- |
| URI | <http://purl.org/dc/terms/modified> |
| Label | Date Modified |
| Definition | Date when the document was (last) changed. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | xsd:date |
| Implementation Notes | The date that the document was last changed in xsd:date format yyyy-mm-dd, e.g. 2023-12-18. |
| Information Use | The modified date can be used to tell users and systems that a document has changed since it was last viewed or extracted, i.e. new data is available. |

| Property Name | valid |
| --- | --- |
| URI | <http://purl.org/dc/terms/valid> |
| Label | Date valid |
| Definition | Date when the document is valid. This will be the most recent of date_issued and date_modified. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | xsd:date |
| Implementation Notes | The date that a document is valid. This can be expressed as an xsd:date in the format yyyy-mm-dd, e.g. 2023-12-18 |
| Information Use | When a document is replaced, the previous version often remains accessible. The valid date (range) lets users know if/when the document is relevant. |

| Property Name | audience |
| --- | --- |
| URI | <http://purl.org/dc/terms/audience> |
| Label | Audience |
| Definition | People or organisations that this document is intended for. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | This should be a statement of who the document is addressed to, e.g. businesses, employers, adults, energy suppliers. |
| Information Use | The audience value helps users find the documents relevant to them, especially if there are multiple versions of a document directed to different user groups. |

| Property Name | coverage |
| --- | --- |
| URI | <http://purl.org/dc/terms/coverage> |
| Label | Coverage |
| Definition | The jurisdiction(s) under which the document is relevant. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | [ISO 3166 country codes](https://www.iso.org/iso-3166-country-codes.html) |
| Implementation Notes | This should be the geographical area that the document relates to described in the ISP 3166 standard, e.g. “GB-ENG”, “GB-NIR”, “GB-SCT”, “GB-WLS” or “GB”. |
| Information Use | Some documents may only relate to part of the UK, e.g. valid in England, Wales and Scotland but not Northern Ireland. Recording this information helps users find the jurisdiction and understand if a document is relevant to them. |
| Controlled List | GB  |
|| GB-ENG |
|| GB-WLS |
|| GB-SCT |
|| GB-NIR |
|| GB-ENG GB-WLS |
|| GB-ENG GB-SCT |
|| GB-ENG GB-NIR |
|| GB-SCT GB-WLS |
|| GB-SCT GB-NIR |
|| GB-WLS GB-NIR |
|| GB-ENG GB-WLS GB-SCT |
|| GB-ENG GB-WLS GB-NIR |
|| GB-ENG GB-SCT GB-NIR |
|| GB-WLS GB-SCT GB-NIR |

| Property Name | subject |
| --- | --- |
| URI | <http://purl.org/dc/terms/subject> |
| Label | Subject |
| Definition | Sector(s) covering the document's business area. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | The subject matter of the document. This takes the form of a sector(s) from a controlled list. |
| Information Use | Recording information on document subjects provides information for search engines, especially to help users find relevant documents when they don't know the exact document they are looking for as well as relating documents in the same subject area. |
| Controlled List | Agriculture, forestry and fishing |
|| Mining and Quarrying |
|| Manufacturing |
|| Construction |
|| Utilities |
|| Real estate |
|| Wholesale, Retail and Consumer Services |
|| Food and Drink |
|| Accommodation, Tourism and Leisure Activities |
|| Media and Creative Industries |
|| Transportation and Storage |
|| Financial and Professional Services |
|| Education and Training |
|| Scientific Research, Innovation and Technology |
|| Health |
|| General business regulations |

| Property Name | type |
| --- | --- |
| URI | <http://purl.org/dc/terms/type> |
| Label | Type |
| Definition | Categorisation of the type of regulatory document e.g. Guidance, Standard |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | The type of document being published, e.g. guidance, standard, legisation |
| Information Use | Understanding the document type allows users to put the document into context and see its purpose which may not be evident from the title. |
| Controlled List | Guidance |
|| Statutory Guidance |
|| Standard |
|| Legislation |

| Property Name | license |
| --- | --- |
| URI | <http://purl.org/dc/terms/license> |
| Label | License |
| Definition | The licence regulating reuse of the document. |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range |     |
| Implementation Notes | This property should contain an URI that resolves to the relevant licence governing use of the content, e.g. <http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3> |
| Information Use | The licence information is essential for people looking to reuse or republish regulator information. |

| Property Name | hasFormat |
| --- | --- |
| URI | <http://purl.org/dc/terms/hasFormat> |
| Label | Has Format |
| Definition | A way to relate versions of a document in different formats, e.g. linking the HTML version with a PDF version, inverse of isFormatOf |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of a document in different formats. |
| Information Use | Connecting versions of a document in different formats helps with document management and allows users to easily find their preferred format, which can be important for accessibility. |

| Property Name | isFormatOf |
| --- | --- |
| URI | <http://purl.org/dc/terms/isFormatOf> |
| Label | Is Format Of |
| Definition | A way to relate versions of a document in different formats, e.g. linking the HTML version with a PDF version, inverse of hasFormat |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of a document in different formats. |
| Information Use | Connecting versions of a document in different formats helps with document management and allows users to easily find their preferred format, which can be important for accessibility. |

| Property Name | hasVersion |
| --- | --- |
| URI | <http://purl.org/dc/terms/hasVersion> |
| Label | Has Version |
| Definition | Relating a document to another version, e.g. a new updated version of the document, inverse of isVersionOf |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of different versions of a document. |
| Information Use | Relating different versions of a document, assists with document management and for users to understand the evolution of a document over time. |

| Property Name | isVersionOf |
| --- | --- |
| URI | <http://purl.org/dc/terms/isVersionOf> |
| Label | Is Version Of |
| Definition | Relating a document to another version, e.g. a new updated version of the document, inverse of hasVersion |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of different versions of a document. |
| Information Use | Relating different versions of a document, assists with document management and for users to understand the evolution of a document over time. |

| Property Name | references |
| --- | --- |
| URI | <http://purl.org/dc/terms/references> |
| Label | References |
| Definition | Relating a cited or referenced document, inverse of isReferencedBy |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of documents where one references the other. |
| Information Use | Documents often refer to other documents, including an explicit link provides clarity, improves findability, online display and accessibility. |

| Property Name | isReferencedBy |
| --- | --- |
| URI | <http://purl.org/dc/terms/isReferencedBy> |
| Label | Is Referenced By |
| Definition | Relating a cited or referenced document, inverse of references |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of documents where one references the other. |
| Information Use | Documents often refer to other documents, including an explicit link provides clarity, improves findability, online display and accessibility. |

| Property Name | hasPart |
| --- | --- |
| URI | <http://purl.org/dc/terms/hasPart> |
| Label | Has Part |
| Definition | A way to relate the whole document to a part of a document, where they are referenced or published separately. Inverse of isPartOf |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of part of a document to the whole document (or a higher-level division). |
| Information Use | Relating a part of a document to the whole document aids online navigation and document management. |

| Property Name | isPartOf |
| --- | --- |
| URI | <http://purl.org/dc/terms/isPartOf> |
| Label | Is Part Of |
| Definition | A way to relate the whole document to a part of a document, where they are referenced or published separately. Inverse of hasPart |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of part of a document to the whole document (or a higher-level division). |
| Information Use | Relating a part of a document to the whole document aids online navigation and document management. |

| Property Name | isReplacedBy |
| --- | --- |
| URI | <http://purl.org/dc/terms/isReplacedBy> |
| Label | Is Replaced By |
| Definition | Relating a document that replaces or supersedes the document. Inverse of replaces |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of a document and the document that replaces it. |
| Information Use | It's common for a new document to replace a previous one. Explicitly sharing this relationship can help users find the right documents and understand the relationship between documents as well as document management. |

| Property Name | replaces |
| --- | --- |
| URI | <http://purl.org/dc/terms/replaces> |
| Label | Replaces |
| Definition | Relating a document to the old superseded or replaced document, inverse of isReplacedBy |
| Domain | <https://www.gov.uk/def/ords/regulatorDocument> |
| Range | <http://www.w3.org/2000/01/rdf-schema#Literal> |
| Implementation Notes | Relationship between identifiers of a document and the document that it replaces. |
| Information Use | It's common for a new document to replace a previous one. Explicitly sharing this relationship can help users find the right documents and understand the relationship between documents as well as document management. |
