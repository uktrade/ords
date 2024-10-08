# ORDS

Contains the explanation, schemas and example usage of the Open Regulation Document Standard (ORDS).

## What is ORDS?

ORDS stands for Open Regulation Document Standard. designed for use by all UK Regulators who publish legally enforceable guidance, rules recommendations, consultations and similar documents online in HTML, PDF or any other format. It can also be used by organisations who re-publish or create indexes of regulatory documents, such as RD’s Open Regulation Platform. 

This standard has been developed by the [Regulation Directorate](https://www.gov.uk/government/collections/smarter-regulation) (RD), part of the [Department of Business and Trade](https://www.gov.uk/government/organisations/department-for-business-and-trade), in collaboration with regulators. RD is responsible for co ordinating regulatory reform, working to make UK regulations easier to access, to reduce the compliance costs of businesses.

## What is it used for?

ORDS is designed to be the foundation for wider work to improve access and reuse of Regulator documents online. It aims to provide a consistent set of metadata values for documents published by Regulators that can be used to develop business-centred digital services supporting regulatory compliance, improve search engine optimisation, facilitate document collation, aid document lifecycle management and document indexing.

In an ongoing project the Regulation Directorate is bringing regulatory documents together into one place with the Open Regulation Platform, and to introduce some good practice conventions around document publication.  We hope that this standard will be the first step in making regulator documents machine-readable, fully accessible and more standardised for ease of use by businesses and reuse by reg-tech companies.

## What stage is it at?

Currently, the standard is at v1.0.0, after going through a number of draft iterations. Our policy can be found at [Version Management Policy](https://github.com/uktrade/ords/blob/main/VERSIONCONTROLPOLICY.md)
Changes will be tracked in the [changelog](https://github.com/uktrade/ords/blob/main/CHANGELOG.md).

## How was ORDS developed?

Reviewing the State of the Art: We started out by investigating best practice and conventions for online publishing. We determined that there is no existing data standard designed specifically for regulatory data. We reviewed existing metadata and document mark-up standards widely used for publishing legal and official documents online including:
- [Dublin Core](https://www.dublincore.org/), an international metadata standard for describing digital or physical resources. 
- [Functional Requirements for Bibliographic Records](https://en.wikipedia.org/wiki/Functional_Requirements_for_Bibliographic_Records) (FRBR), an entity relationship model developed by librarians, commonly used as a versioning model in legislation publishing.
- [Data Catalog Vocabulary](https://www.w3.org/TR/vocab-dcat-3/) (DCAT),  a metadata standard recommended by the Central Digital and Data Office for data interchange within government. 
- [European Legislation Identifier](https://eur-lex.europa.eu/eli-register/about.html) (ELI), an EU standard for identifiers and metadata used by European legislation publishers to describe legal documents online.
- [Crown Legislation Mark-up Language](https://legislation.github.io/clml-schema/) (CLML), the XML schema developed by The National Archives to represent legislation published on www.legislation.gov.uk .
- [OASIS LegalDocumentML](https://groups.oasis-open.org/communities/tc-community-home2?CommunityKey=3425f20f-b704-4076-9fab-018dc7d3efbe), (formerly Akoma Ntoso), an international standard for representing legal documents in XML. 

### Consultation
We consulted with academics and data experts who had looked at applying standards to regulation data in other contexts. This included The National Archives team responsible for publishing UK legislation on www.legislation.gov.uk and other international legislation publishers. We created a working group with regulators to gather requirements and to provide feedback on the standard. This, together with in-depth discussions with individual regulators has allowed us to understand the processes and challenges of document publishing as well as the practicalities of implementing and using the standard.

### Create Draft Standard
Using all the information gathered through desk research and consultation we created an initial standard, ORDS version 0.2.

### Feedback and Iteration of the Standard
We have presented this standard to stakeholders through a series of Data Standards Seminars with regulators to gather feedback. We have also conducted exercises to generate sample data compliant with the stand to test the practically of real-world implementation. Through these activities we have obtained feedback that has allowed us to revise and improve the standard. 

We have undertaken significant testing of ORDS with regulatory documents. This started with an initial testing with space sector documents. 

This has expanded to a large-scale tagging of construction sector regulatory documents. Over 600 documents have been tagged across several formats and regulators by 4 different taggers. This test has allowed us to expand our guidance and documentation for the practical implementation of ORDS.

We have also engaged with individual regulators to understand their specific requirements, and how ORDS can be implemented. Our ongoing engagement with the Office for Product Safety and Standards (OPSS) is seeing their team use ORDS to tag and index their regulatory guidance. The resulting metadata will be used both by the Open Regulation Platform, and by OPSS itself to audit and manage its library of guidance.



### Formalisation

We are working with the Data Standards Authority (DSA) to make ORDS an official UK government standard for regulatory metadata. You can find out about this process in the Central Digital and Data Office gov.uk pages that describe how open standards for government are selected.

## Features

### Fields and Dublin Core Compatibility

The majority of the properties in the ORDS standard are a restatement of properties from the Dublin Core vocabulary with a recommended implementation pattern (listed at the end of this document). The four properties created specifically for ORDS are listed below:

|Property Name |Mandatory |
| -------- | ---------|
|Regulatory Topics|	|
|Status|	|
|Date Uploaded|		|
|Related Legislation|	|

Dublin Core Properties:

|Property Name| Mandatory |
| ---------| ---------|
|Title| (x)|
|Identifier| (x)|
|Publisher| (x)|
|Language|	|
|Format|	|
|Description|	|
|Date Issued|	|
|Date Modified|	|
|Date Valid| (x)|
|Audience|	|
|Coverage|	|
|Subject|	|
|Type|		|
|License|	|
|Has Format|	|
|Is Format Of|	|
|Has Version|	|
|Is Version Of|	|
|References|	|
|Is Referenced By|	|
|Has Part|	|
|Is Part Of|	|
|Is Replaced By|	|
|Replaces|	|


The metadata ontology can be found as:
-	A [machine-readable 'Turtle' file](https://github.com/uktrade/ords/blob/main/ORDS.ttl)
-	A text-based file

### Embedding ORDS
ORDS metadata could be embedded in documents, for example using a rubric at the beginning or end of the document. Metadata could be stored in metadata files that are companions to the related document, spreadsheets or in a database. For documents published in HTML you can embed ORDS metadata properties in the file using RDFa or JSON-LD.

## Contributing
Contributions are welcome! Please see the CONTRIBUTING.md file for details on how to get involved. You can submit issues or pull requests to help improve the standard.

## License
The project is licensed under the MIT license. Please see the license page for more details.





## What do I need to know to help?
If you are looking to help with a contribution to the ORDS standard, We love your input. We want to make contributing to this standard as easy and transparent as possible, whether it's:
•	Reporting a bug/issue
•	Discussing the current state of the code
•	Submitting a fix
•	Proposing new features
•	Becoming a maintainer

**We Develop with Github**

We use github to host code, to track issues and feature requests, as well as accept pull requests.

**We Use [Github Three-Flow](https://guides.github.com/introduction/flow/index.html), So All Code Changes Happen Through Pull Requests**

Pull requests are the best way to propose changes to the codebase (we use [Github Three-Flow](https://guides.github.com/introduction/flow/index.html)).

We actively welcome your pull requests:
1.	Fork the repo and create your branch from master.
2.	make your proposed changes
3.	Issue that pull request!

**Any contributions you make will be under the MIT Software License**

In short, when you submit code changes, your submissions are understood to be under the same [MIT License](http://choosealicense.com/licenses/mit/) that covers the project. Feel free to contact the maintainers if that's a concern.

**Report bugs using Github's issues**

To add an issue to GitHub Issues, follow these steps:
1.	Visit the repository: Navigate to the ORDS repository where you want to add the issue. Ensure that you have a GitHub account and are logged in.
2.	Go to Issues: Click on the "Issues" tab located at the top of the repository's page. This will take you to the issues section of the repository.
3.	Create a new issue: On the issues page, click on the green "New issue" button. You will be directed to a new page where you can input the details of the issue.
4.	Provide a title and description: Give your issue a descriptive title that summarizes the problem or feature request. In the description, provide additional information, including steps to reproduce the issue (if applicable) or any specific context.
5.	Add labels and assignees (optional): You can enhance the issue's organization by assigning labels that categorize it, such as "bug," "enhancement," or "documentation." You can also assign the issue to specific team members by mentioning them as assignees.
6.	Submit the issue: Once you have filled in the necessary details, click on the "Submit new issue" button. Your issue will be added to the repository's list of issues, where it can be viewed and tracked by others.
Remember to be clear and concise when describing the issue and providing relevant information. This will help others understand and address the problem effectively.

## Semantic Versioning
We use semantic Versioning, to version tag the ORDS open standard, semantic Versioning is a versioning scheme that uses a three-part number format (X.Y.Z) to convey information about compatibility, changes, and updates. It can be found at [Version Management Policy](https://github.com/uktrade/ords/blob/main/VERSIONCONTROLPOLICY.md).

## What does the Code of Conduct mean for me?

Our Code of Conduct means that you are responsible for treating everyone on the project with respect and courtesy regardless of their identity. If you are the victim of any inappropriate behaviour or comments as described in our Code of Conduct, we are here for you and will do the best to ensure that the abuser is reprimanded appropriately, per our code.
