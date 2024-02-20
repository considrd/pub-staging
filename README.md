# pub-staging

This Repository is for submission, review and deployment of proposed Implementer's drafts, Final Specifications and Errata Specifications.


## Process 
for WG co-chairs to propose document for publication...

1. Make sure their github ID is added to *** team in github org *** 
2. Create a branch named in the following format...  *** branch naming ***
3. Push proposed documents and their source into the branch
4. Once satisfied then the co-chair should create a PR

... potentially other steps TBC

Folllowing this the review process will begin and either the proposed documents will be merged into main and published to openid.net or feedback will be provided via github comments on any issues detected with the propoed document.

## Checks
There are checks performed prior to publication that if failed may need modification to documents proposed for publication these are 

### Internal .html Checks
> * Verify html includes “draft” or “final” in document metadata
> * Check history section exists (except for final specs)
> * Check Notices section exists
> * Check copyright year is current year
> * Check that the copyright section contains the right copy
> * Check naming is conformant to OIDF naming **add defintion**

### External Checks
Determine which class of submission it is: (**maybe we can use tags for this?**)
> * Implementers Draft
> * Final Specification
> * Errata Specification

Check for presence of file with extension:
> * .html, (required)
> * .md OR .xml (either or both)

Search name in OIDF site to ensure it is not already present
Ensure name is new or an iteration number

Check that publish date is “recent” **within last 7 days?**

Check all references exist and are most current version

Check that any referenced content in the .md is included in the .html  - Driven by search for references of the form: <{{examples/request/vp_token_type_only.json}} 
