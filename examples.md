
# Open Regulation Document Standard (ORDS) Implementation Examples

The following examples detail the application of the Open Regulation Document Standard to some sample documents.

In these examples we will populate a metadata table for each document. This table could be added directly to the beginning or end of an online document.

This data can also be expressed in machine readable format. This could be serialised in a variety of formats embedded within the documents or held separately in a database. One encoding option, embedding RDFa metadata in HTML documents, is also included for reference.

---

## Example 1

**Document:** “Working at height: A brief guide” (Health and Safety Executive)

Note that not all properties will be relevant or known for every document. In this example there is only one version of the document so there are no relationships to alternative formats or versions. The document references other publications but is not itself referenced by any other documents. It’s an independent document published as one file so there are no references to parts or a parent document. We have no information on documents that are replaced by this document or those that supersede it. 

### ORDS Metadata


| Property Name | Value |
|---------------|--------|
| **Title** | Working at height: A brief guide |
| **Identifier** | https://www.hse.gov.uk/pubns/indg401.htm <br> ISBN: 9780717664900 <br> Series code: INDG401 (rev2) |
| **Publisher** | Health and Safety Executive |
| **Language** | eng |
| **Format** | application/pdf |
| **Description** | This brief guide describes what employers need to do to protect their employees from falls from height. Falls from height are one of the biggest causes of workplace fatalities and major injuries. Work at height means work in any place where, if there were no precautions in place, a person could fall a distance liable to cause personal injury. Common causes are falls from ladders and through fragile roofs. The Work at Height Regulations 2005 aim to prevent death and injury from a fall from height. |
| **Date Issued** | 2014‑01‑27 |
| **Date Modified** | 2014‑01‑28 |
| **Date Valid** | 2014‑01‑27 |
| **Audience** | Employers |
| **Coverage** | GB‑ENG <br> GB‑SCT <br> GB‑WLS |
| **Subject** | Safety <br> Construction |
| **Type** | Guidance |
| **License** | https://www.hse.gov.uk/copyright.htm |
| **Regulatory Topics** | Construction <br> Buildings |
| **Status** | Active |
| **Date Uploaded** | 2014‑01‑27 |
| **Has Format** | |
| **Is Format Of** | |
| **Has Version** | |
| **Is Version Of** | |
| **References** | https://www.legislation.gov.uk/id/uksi/2005/735 <br> http://www.hse.gov.uk/risk/risk-assessment.htm <br> http://www.hse.gov.uk/involvement <br> http://www.hse.gov.uk/work-at-height/wait/index.htm <br> https://www.hse.gov.uk/pubns/books/hsg33.htm |
| **Is Referenced By** | |
| **Has Part** | |
| **Is Part Of** | |
| **Is Replaced By** | |
| **Replaces** | |
| **Related Legislation** | https://www.legislation.gov.uk/id/uksi/2005/735 |

---

## Example 2

**Document:** “SR2021 No 15: storage and mechanical treatment of waste paper, cardboard and plastic for recovery” (Environment Agency)

### ORDS Metadata


 Property Name | Value |
|---------------|--------|
| **Title** | SR2021 No 15: storage and mechanical treatment of waste paper, cardboard and plastic for recovery |
| **Identifier** | SR2021 No 15 <br> https://www.gov.uk/government/publications/sr2021-no-15-storage-and-mechanical-treatment-of-waste-paper-cardboard-and-plastic-for-recovery/sr2021-no-15-storage-and-mechanical-treatment-of-waste-paper-cardboard-and-plastic-for-recovery |
| **Publisher** | Environment Agency |
| **Language** | eng |
| **Format** | text/html |
| **Description** | The Environmental Permitting (England & Wales) Regulations 2016 - Chapter 4 Standard rules |
| **Date Issued** | 2022‑03‑16 |
| **Date Modified** | 2023‑12‑14 |
| **Date Valid** | 2017‑01‑01 |
| **Audience** | Operators of regulated waste facilities |
| **Coverage** | GB‑ENG |
| **Subject** | Business <br> Environment |
| **Type** | Statutory guidance |
| **License** | https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/ |
| **Regulatory Topics** | Environment <br> Waste <br> Paper <br> Cardboard <br> Plastic <br> Recycling |
| **Status** | Active |
| **Date Uploaded** | |
| **Has Format** | |
| **Is Format Of** | |
| **Has Version** | |
| **Is Version Of** | |
| **References** | |
| **Is Referenced By** | |
| **Has Part** | |
| **Is Part Of** | |
| **Is Replaced By** | |
| **Replaces** | |
| **Related Legislation** | https://www.legislation.gov.uk/id/uksi/2016/1154 <br> https://www.legislation.gov.uk/id/ukpga/2006/16 <br> https://www.legislation.gov.uk/id/eudr/2008/98 |

---

## Create Your Own Examples

### ORDS Metadata Template

| Property Name | Value |
|---------------|--------|
| **Title** |  |
| **Identifier** |  |
| **Publisher** |  |
| **Language** |  |
| **Format** |  |
| **Description** |  |
| **Date Issued** |  |
| **Date Modified** |  |
| **Date Valid** |  |
| **Audience** |  |
| **Coverage** |  |
| **Subject** |  |
| **Type** |  |
| **License** |  |
| **Regulatory Topics** |  |
| **Status** |  |
| **Date Uploaded** |  |
| **Has Format** |  |
| **Is Format Of** |  |
| **Has Version** |  |
| **Is Version Of** |  |
| **References** |  |
| **Is Referenced By** |  |
| **Has Part** |  |
| **Is Part Of** |  |
| **Is Replaced By** |  |
| **Replaces** |  |
| **Related Legislation** |  |

---

If you want to experiment with adding machine readable data to HTML documents using RDFa you can use the implementation instructions in [Instructions](instructions.md).
