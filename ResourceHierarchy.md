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
