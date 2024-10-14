# pub-staging

This Repository is for proposal, review and deployment of proposed Work Group Drafts, Implementer's drafts, Final Specifications and Errata Specifications.

## Process 
For working group co-chairs and/or editors to propose a document for publication with support from the OIDF Secretary and their delegates.

1. Make sure their github ID is added to the appropriate team in GitHub (there is one team per WG)
2. Clone the repository
3. Create a branch named in the following format...  __proposed/**__
4. Add the files they wish to propose (this should include at least one .html and the source .md, .xml, .txt) to the Work Group sub-directory
5. Push the updated branch and its source(s) to the remote branch
6. At this point a GitHub Action is triggered that will run a number of checks on the proposed html documents 
7. Once the GitHub action is complete it will email the corresponding WG co-chair team and if successful will also raise a PR automatically and e-mail the Secretary team (if the checks fail then the WG co-chaors should update and re-submit having reviewed the output of the GitHub Action)
8. The Secretarial Team will review the PR and perform any final human checks needed
9. If comfortable with the proposal the Secretarial team will approve the PR
10. When PR is approved another GitHub Action is triggered to deploy the new documents to openid.net/specs
11. When deployment is successful the PR is merged automatically to main

## Checks
There are checks performed prior to publication that, if failed, may need modification to documents proposed for publication. These are:

### Internal *-<draft>.html Checks
> * Verify html includes “draft” or “final” in document metadata
> * Verify that -nn draft number in the pathname corresponds to the draft number in the specification in non-final drafts
> * Verify that -nn draft has not already been published at openid.net/specs/ (or same for the -final, -IDn, or -errata versions)
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
