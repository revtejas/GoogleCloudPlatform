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

## Predefined Roles: Organization, Billing and Project Roles

|  Roles | Description  | Use Case  |
|---|---|---|
|  __Billing Account Creator__ | Permissions to create new billing accounts | Finance Team |
|  __Billing Account Admin__ |  Manages billing account but can't create them | Finance Team  |
| __Billing Account User__  | Assigns projects to billing accounts  | Project Owner  |
| __Billing Account Viewer__  | View only access to billing account  | Auditor  |

### Scenarios
- I'm creating a project and I want to associate an existing billing account with the project - Project Creator and Billing Account User
- I'm a billing auditor - Billing Account Viewer

## Predefined Roles: Compute Engine Roles

|  Roles | Description  | Use Case  |
|---|---|---|
| __Compute Engine Admin__ | Complete control of compute - Instances, Images, Load Balancers, Networks, Firewalls  | -  |
| __ Compute Instance Admin__  | CRED operations on virtual machine instances and disks  | -  |
| __ Compute Engine Network Admin__  | Complete access to networking resources (routes, networks, health checks, VPN, Gateways) and READ ONLY access to security resources (firewall rules and SSL certificates)  | -  |
| __ Compute Engine Security Admin__  | Complete access to firewall rules and SSL certificates  | -  |
| __Compute Storage Admin  | Complete access to disks, images, snapshots  | -  |
| __Compute Engine Viewer__  | READ ONLY access to everything in compute  | -  |
| __Compute OS Admin Login__  | Log in to a compute engine instance as an admin user  | -  |
| __Compute OS Login__  | Log in to a compute engine instance as a standard user  | -  |
