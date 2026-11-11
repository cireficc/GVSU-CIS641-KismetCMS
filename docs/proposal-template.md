Team name:

Team members:

# Introduction

### Project Sponsors

*The person/entity that wants the system/solution.*

- Diamond Consulting LLC
- Property Management companies consulted by Diamond Consulting LLC

### Business Need

*Why we need the new system.*

An MOR Readiness module is necessary for Diamond Consulting to provide and improve its ongoing compliance consulting services to its 15 Property Management clients.

It simultaneously improves the salability of Kismet CMS as a compliance platform to Property Management clients as well as other compliance consulting agencies like Diamond Consulting.

### Business requirement

*What the system will do.*

The MOR Readiness module will:

- allow Property Management clients to manage annual audits (MORs) and its process steps, documentation and timelines across their portfolio of properties
    - allows Diamond Consulting to track MORs alongside clients for shared understanding of critical compliance operations
- provide a calendar view of MORs occurring across a client’s portfolio with key audit status information
- synthesize a Property’s existing system data for the effective year into a single view: regulatory documents and their associated metadata, EIV reports and discrepancies and their upload/resolution status, tenant files selected for review, and other useful system information an Auditor would need to see
- allow Auditors to add audit findings and corrective actions to tenant files selected for review
- allow Auditors to add general audit findings and corrective actions to the MOR
- allow Property Management employees to resolve audit findings, and document resolutions
- allow the Auditor or Property Management employees to close an MOR with a Clearance Letter document upload and an audit completion status
- send **notifications** at each process step of the MOR Audit process and key dates/timelines

### Business Value

*Benefit to the business.*

The following tangible value will be created by implementing the system:

**For Diamond Consulting**

- improves consult efficacy for clients’ compliance and risk management posture by providing tooling for proactive audit preparation
- enables proactive consulting for Properties with high compliance risk and high likelihood of MOR findings, with substantial risk mitigation benefits for client’s business
- increased efficiency in compliance consulting and management across clients frees up consultant time and capacity for higher-value business services

**For Property Management clients**

- proactive compliance and risk management posture by having documentation and data prepared *before* an MOR occurs
    - mitigates risk of lost regulatory and compliance documentation
- mitigate risk of HAP garnishment/recapture due to improper use of mandatory EIV system, or other related high-impact MOR findings
- holistic portfolio-wide view of active MORs, allowing for efficient resource allocation to ongoing and upcoming audits
- highly structured and organized MOR preparation creates operational efficiencies and eases stress on employees in various roles of the organization responsible for preparing the audit

**State agencies/Contract Administrators**

- …

### Special issue

*Other stuff that is implemented.*

- state agency (Contract Administrator) access to MOR Readiness module to perform fully-digital and streamlined Property audits
    - role-based access controls (RBAC) to Property data necessary for an MOR (regulatory documents, tenant files, & EIV reports + discrepancies)
    - digital tenant file audits
    - MOR findings and corrective actions

# Anticipated Technologies

This feature will be built into the Kismet CMS web application. Kismet currently uses Ruby on Rails as the web framework, PostgreSQL as the database, and Google Cloud Storage as the file upload backing store. We already rely on several dependencies to build this kind of functionality into Kismet, including [`carrierwave`](https://github.com/carrierwaveuploader/carrierwave) for file uploads, [`audited`](https://github.com/collectiveidea/audited) for audit and data change history, among others.

# Method/Approach

The plan is for Chris to develop drafts for the Kismet development team of all relevant preliminary artifacts including a System Request, a Software Requirements Specification, a CRC Card diagram, a Class Diagram, and a Sequence Diagram to get the team started. Chris will participate in multiple weekly meetings with the development team to check in on and refine the team's understanding of what we're trying to build, including having them iterate on an AI-generated HTML mockup of the feature based on document specs. After several weeks of conversation and refinement of initial system designs/artifacts, the team will commit to iteratively developing the module without Chris' direct assistance RE: engineering tasks.

# Estimated Timeline

Major milestones:
1. initial system specs/drafts completed by Chris and passed onto team for read-review by 10/14/26.
2. first-pass Q&A and potential revisions to specs/drafts completed by dev team by 10/28/26.
3. first-pass review and refinement of Q&A/revisions completed by Chris + Cyndi (consultant) by 11/4/26.
4. second pass Q&A and potential revisions to specs/drafts completed by dev team by 11/18/26.
5. second-pass review and refinement of Q&A/revisions completed by Chris + Cyndi (consultant) by 11/25/26.
6. module development begins 11/30: first-pass prototype delivered by 12/4.
7. module development continues 12/7: second-pass prototype delivered by 12/11.
8. module development continues 12/14: final MVP delivered by 12/18.
9. MVP bugfixes and refinements begins 12/21: release-MVP ready by 1/2/27.


# Anticipated Problems

General lack of domain knowledge on the development team; this is a **huge** module that utilizes existing system resources/data. For the dev team to wrap their heads around the "big picture" of the new module and its key features while also gaining deeper knowledge of existing system components and data that will be integrated is a _huge_ senior engineer and team management challenge. Given the complexity of the problem we're trying to solve, just getting the team up to speed on the domain challenge is the primary hurdle, followed immediately by junior engineers designing system components that require careful data/model considerations, as well as using existing APIs and developing new ones, all while trying to keep the user experience (UX) minimal, intuitive, and understandable by our non-technical stakeholder audience.
