### Problem Framing:

The current system has ability to view or compare the page's history. A user can view the history of any specific page and can compare immediate versions. Users are unable to check what have been modified since the last review. 

### Constraint 
Major technical constraint at the moment is no 2 versions can be compared with each other if they are not immediate. 
For example: A page has v0 to v5, v3 cannot be compared to v5 directly. V3 should be either compared to V2 or V4 only. 

### Goal
The end goal of the feature is to build a way, that users can directly check difference of the version they reviewed last and the current version. This helps them figure out the actual changes directly, without jumping through the versions history one after the other.

For example: 
- Page : Intent Spec
- Versions: v0 to v5 (Latest)
- User A: viewed version - v3

When user comes back to the page, he/she should be easily identify the action / button on the page to view the differences - v3 to v5.

### Underlying Solution
This feature requires a shadow feature to be built first before proceeding on the actual feature.

- Phase 1: Comparing 2 non immediate versions
- Phase 2: Managing last viewed version per user per page & updating the last viewed version


### Assumptions
- An immediate version comparison feature has been provided. 
- Non immediate feature comparison is a missing feature.
- Currently, system does not track what version has been viewed by any user.
