## Resource hierarchy in GCP
- Organization -> Folder -> Project -> Resources
- Resources are created in projects
- A folder can contain multiple projects
- An Org can contain multiple folders

## Recommendation for Enterprises
- Create separate projects for different environments
    - Complete isolation between test and production environments
- Create separate folders for each department
    - Isolate production of one department from another
    - We can create shared folder for shared resources
- One project per application per environment
    - For example, let's consider two apps: "A1" and "A2"
    - Let's assume we need two environments: "DEV" and "PROD"
    - In ideal world, we will create four projects: A1-DEV, A1-PROD, A2-DEV, A2-PROD
        - Isolates environement from each other
        - DEV changes will not affect PROD
        - Grant all DEVs complete access(create, delete, deploy) to DEV Projects
        - Provide production access to operations teams only
        
  











## Component's of IAM's access management system
### Groups:
- A scalable way to organize users

### Policies:
- Define what identities have access to specific resources

### Permissions:
- Fine-grained access control on a resource

### Resources:
- Fundamental components of all google cloud services

### Roles:
- Collection of permissions determining what a user can do

### Memebers(or Identities):
- Unique ID associated with an account

### Benefits of using a groups from the beginning
- Security admin dont have to manually change permissions for users that are hired, fired or moved across teams
- Minimie mistakes 
- Works even with existing systems like Active directory

### How to minimize internal threat
- Create groups to simplify security
- Reduce harm from disgruntled employees
- Prevent hacked accounts

More to be continued...
