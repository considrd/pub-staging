# pub-staging

This Repository is for submission, review and deployment of proposed Implementer's drafts, Final Specifications and Errata Specifications.


## Process 
for working group co-chairs and/or editors to propose a document for publication...

1. Make sure their github ID is added to *** team in github org *** 
2. Create a branch named in the following format...  *** branch naming ***
3. Push proposed document and its source(s) into the branch
4. Once satisfied, then the co-chair or editor should create a PR

... potentially other steps TBC

Folllowing this, the review process will begin and either the proposed documents will be merged into main and published to openid.net/specs/ or feedback will be provided via github comments on any issues detected with the propoed document.

## Checks
There are checks performed prior to publication that, if failed, may need modification to documents proposed for publication. These are:

### Internal *-<draft>.html Checks
> * Verify html includes “draft” or “final” in document metadata
> * Verify that -nn draft number in the pathname corresponds to the draft number in the specification in non-final drafts
> * Verify that -nn draft has not already been published at openid.net/specs/ (or same for the -final, -IDn, or -erratan versions)
> * Check history section exists (except for final and errata specs)
> * Check Notices section exists
> * Check copyright year is current year
> * Check that the copyright section contains the right text
> * Check naming is conformant to OIDF naming at https://openid.net/wg/resources/naming-and-contents-of-specifications/

### External Checks
Determine which class of submission it is: (**maybe we can use tags for this?**)
> * Working Group draft
> * Implementer's Draft
> * Final Specification
> * Final Specification Incorporating Errata Corrections

Check for presence of file with extension:
> * *-nn.html (required)
> * *-nn.md OR *-nn.xml (either or both if single source) or *-nn.zip if multiple sources
> * Verify that the source draft number -nn matches the html draft number (if a normal draft)
> * Verify that the draft designators are -final if a final specification
> * Verify that the draft designator is -ID*, if an Implementer's Draft
> * Verify that the draft designatore is -errata*, if an Errata spec

More checks:
> * Search name in OIDF site to ensure it is not already present.
> * Ensure name is new or a new iteration number.  If the file is new, verify that the -nn number is -00.
> * Check that publish date is “recent” **within last 7 days?**
> * Check all references exist and are most current version
> * Check that any referenced content in the .md is included in the .html  - Driven by search for references of the form: <{{examples/request/vp_token_type_only.json}}

Publication actions:
> * After checks, publish the source *-<draft>.* and *-<draft>.html to openid.net/specs/.  Also, strip the "-<draft>" from the paths and publish the unversioned source and *.html to openid.net/specs/.
