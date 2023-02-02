## User Identity Management in Google Cloud
- Super Admin has access to everything in Org, folders and projects
- He can add other users by adding roles to the specific user on the specific project
- IAM policy is a list of bindings attached to a project, where binding means a mapping between user and his role
    - For example, if you add a binding for a specific user to a specific role in a specific project. He'll be able to access that specific resource in the project
    
    
## Corporate Directory Federation
- Federate Cloud Identity or Google Workspace with you external identity provider(IdP) such as Active Directory or Azure Active Directory
- Cloud Identity manages Identites, managed using "Identity platform" in GCP
- Enable Single Sign-On
    - Users are redirected to an external IdP to authenticate
    - When users are authenticated, SAML assertion is sent to Google Sign-in
    - For example, Federating Azure AD with Cloud Identity
    
    
