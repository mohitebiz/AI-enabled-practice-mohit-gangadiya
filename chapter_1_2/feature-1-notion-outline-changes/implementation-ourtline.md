### Implementation Plan

Phase 1: Multiple Version Comparison
Backend: 
- An API to be exposed for figuring out the differences of 2 versions specified - user's latest reviewed version & latest version of the page. This API should be reusable for version to version comparison

Frontend: 
- A support to be added in the current history immediate version comparison - with a list of versions to compare with any version. 
- Support to view differences of multiple version side by side.  

Database:
- No major database level changes needed.
- Future: If need to cache the differences for performance or frequently checked version - additional development will be required.

#### Assumption:
- As versions are being already stored in the history 

Phase 2: Manage User Version Viewed Status
Backend: 
- An API endpoint to be built that receives user token - extract user id and page id. For that page - find the latest version viewed by the user and compare the with the current latest version of the page. Returns a flag to manage the actions in the frontend.
- A PUT API to be build for updating the latest version reviewed of the page by user.

Frontend:
- Integrate an API to figure out if user has unreviewed changes for the pages. Based on the status - show proper action or information.
- Integrate a screen for multiple (jumped) version differences.
- Add alert when user leaves the page to mark the version viewed and integrate the API to update the status.

Database:
- Need an entity to maintain track of the page + user for view status. 
- If needed: if we need a audit log for when the version is viewed - we might need to modify the schema or add another entity to maintain the log. 