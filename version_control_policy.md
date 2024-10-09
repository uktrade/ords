# Metadata Version Control Policy
## 1. Purpose 
The ORDS Version Control Policy establishes a standardized approach and guidelines for managing the development, modification and distribution of ORDS. This ensures that all versions of ORDS are tracked, documented ad maintained in a controlled manner, enabling consistency, traceability, and accountability to stakeholders.

## 2. Scope 
This policy applies to ORDS, and any accompanying documentation, schemas, and formats.

## 3. Definitions

-	**ORDS:** Open Regulation Documentation Standard. A metadata standard developed by the Regulation Directorate in the Department for Business and Trade. It is applied to regulatory documents to create a consistent level of information across regulators.
-	**Version Control:** The practice of managing changes to metadata standards in a way that tracks the history of changes, maintains consistency and allows for rollback or updates as needed.
-	**Version:** A unique number or identifier assigned to each change or release of ORDS.
-	**Repository:** A centralised location where metadata standards and related documentation are stored and managed. In the case of ORDS, this is located here.
## 4. Versioning System
### 4.1 Version Numbering Scheme
-	ORDS will follow a structured version numbering system to distinguish between major, minor and patch updates. The format of the version number will be: [Major].[Minor].[Patch]
-	**Major Version:** Significant changes or updates to ORDS that may affect backwards compatibility (e.g. structural changes or schema overhauls)
-	**Minor Version:** Incremental updates that add new features, elements, or guidelines, but do not break existing implementations.
-	**Patch Version:** Small changes such as corrections, clarifications, or bug fixes that do not impact the core functionality or structure.
    
**For example:**  
-	Version 1.0.0: First official release.
-	Version 1.1.0: Minor updates to metadata elements or structure.
-	Version 1.1.1: Small corrections or documentation updates.
### 4.2 Release Types
-	**Draft Version:** Preliminary version of a metadata standard subject to review and approval. Drafts are labelled with a “D” (e.g., 1.0.0-D1)
-	**Approved Version:** Finalised and officially approved versions of the metadata standard that are ready for implementation.
-	**Deprecated version:** Versions of the metadata standard that are no longer supported or recommended for use but are maintained for historical or reference purposes.
## 5. Version Control Process
### 5.1 Change Request and Approval
-	All changes to metadata must be documented through a formal change request process.
-	Stakeholders will be consulted on any major version changes.
-	Change requests and consultation feedback will be reviewed and approved by the ORDS Governance Committee before implementation.
-   Feedback from consultation and notice of the decision will be published on GitHub.
-	Each approved change will result in the increment of the version number following the version numbering scheme.
### 5.2 Documentation of Changes
-	Each new version must be accompanied by a change log that documents the changes, including:
  -	Date of the change
  -	Author or contributor responsible for the change.
  -	Detailed description of the modification.
  -	Impact assessment on systems (e.g. ORP) and processes.
-	The [changelog](https://github.com/uktrade/ords/blob/main/CHANGELOG.md) will be stored with ORDS in the GitHub repository.
### 5.3 Version Identification
-	Each ORDS documentation piece must clearly indicate the current version number in the header.
-	Embedded ORDS must indicate the version of ORDS within the HTML code.
-	Historical versions must be archived with their respective version numbers and release notes for reference.
### 5.4 Version Release and Distribution
-	Once approved, new versions of ORDS will be made available in the GitHub repository.
-	Notifications from the [open.regulation@businessandtrade.gov.uk](mailto:open.regulation@businessandtrade.gov.uk) email will be sent to all relevant stakeholders, including regulators, ORP API users, and RegTech partners.
-	Appropriate documentation will accompany the release of any major or minor version updates.
## 6. Archiving and Deprecation
### 6.1 Archiving
-	Older versions of the metadata standard will be maintained in an archive for reference and auditing purposes.
-	Archived versions will include the complete documentation and change log history.
### 6.2 Deprecation
-	ORDS that is no longer in active use or is superseded by newer versions may be marked as deprecated.
-	Deprecated versions will remain accessible in the archive but will not be recommended for new projects.
## 7. Roles and Responsibilities
### 7.1 ORDS Governance Committee
-	Review and approve proposed changes to the metadata standard.
-	Ensure compliance with version control policies.
-	Oversee the archiving and deprecation of outdated standards.
### 7.2 ORDS Manager
-	Implement approved changes to the metadata standard.
-	Ensure proper versioning and documentation of all updates.
-	Maintain the centralized repository and ensure stakeholders are notified of new versions.
### 7.3 Stakeholders (Regulators, ORP API Users, RegTech partners)
-	Review and implement updates to the metadata standard in their respective systems.
-	Provide feedback on proposed changes and suggest improvements as needed.
## 8. Compliance and Review
-	This policy will be reviewed annually to ensure it remains current and effective.
-	Non-compliance with this policy may result in inconsistent ORDS usage, data quality issues, and operational inefficiencies.
## 9. Effective Date
This policy is effective as of 08/10/2024.
