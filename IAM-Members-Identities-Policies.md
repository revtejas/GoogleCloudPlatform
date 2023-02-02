# IAM Members/ Identities

- Google Account: Represents a person (as an email address)
- Service Account: Represents an application account (Not person)
- Google Group: Collection of Google & Service accounts
- Google Workspace domain: It provides collaboration services for enterprises
- Cloud Identity domain: Cloud identity is an identity as a Service (IDaaS) solution that centrally manages users and groups

# IAM Policy
- IAM policy can be set at any level of the hierarchy
- Resources inherit the policies of all parents
- The effective policy for a resource is the union of the policy on that resource and its parents
- Policy inheritance is transitive, meaning, Org policies are applied at resource level
- Permission given at higher level overrides the permission given at lower level

## __Predefined Roles:__Organization, Billing and Project Roles

|  Roles | Description  | Use Case  |
|---|---|---|
|  __Billing Account Creator__ | Permissions to create new billing accounts | Finance Team |
|  __Billing Account Admin__ |  Manages billing account but can't create them | Finance Team  |
| __Billing Account User__  | Assigns projects to billing accounts  | Project Owner  |
| __Billing Account Viewer__  | View only access to billing account  | Auditor  |
