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

# Predefined Roles
## Organization, Billing and Project Roles
* __Organization Administrator:__ Defines Resource hierarchy, defines access management policies, manages other users and roles
* __Billing Account Creator:__ Create Billing Accounts
* __Billing Account Admin:__ Manage Billing accounts, however cannot create a billing account
* __Billing Account User:__ Associate projects with Billing Accounts, typically used in combination with __Project creator__
* __Billing Account Viewer:__ See all Billing Account details
