# IAM Best Practices
## Principle of Least Privilege(PLP)
- Give least possible privilege needed for a specific role
    - Basic roles are not reconmmended, rather go with predefined roles
- Use service accounts with minimum previleges
    - Use different service accounts for different apps/purposes

## Separation of Duties
- Involve atleast 2 people in specific tasks
    - For example, have separate deployer and traffic migrator roles so that the deployer cant migrate traffic and migrator cannot deploy new version
 
## Constant Monitoring
- Review Cloud Audit logs to audit changes to IAM policies and access to service account keys
    - Arhive Cloud audit logs in cloud storage buckets for long term retention
  
## Use Groups when possible
- Makes it easy to manage users and permissions
    - For example, if a user joins, you can assign him the group, and if he leaves, you can remove him from the group
