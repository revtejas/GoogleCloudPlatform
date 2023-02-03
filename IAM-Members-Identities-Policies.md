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
| __Compute Instance Admin__  | CRUD operations on virtual machine instances and disks  | -  |
| __Compute Engine Network Admin__  | Complete access to networking resources (routes, networks, health checks, VPN, Gateways) and READ ONLY access to security resources (firewall rules and SSL certificates)  | -  |
| __Compute Engine Security Admin__  | Complete access to firewall rules and SSL certificates  | -  |
| __Compute Storage Admin__  | Complete access to disks, images, snapshots  | -  |
| __Compute Engine Viewer__  | READ ONLY access to everything in compute  | -  |
| __Compute OS Admin Login__  | Log in to a compute engine instance as an admin user  | -  |
| __Compute OS Login__  | Log in to a compute engine instance as a standard user  | -  |

## Predefined Roles: App Engine Roles (CRUD - Create, Read (get/list), Update, Delete)

|  Roles | Description  | Use Case  |
|---|---|---|
|  __App Engine Creator__ | applications(CD), Responsible for creating an application | - |
|  __App Engine Admin__ | applications(RU), services/instances/versions(CRUD),operations | -  |
| __App Engine Viewer__  | applications/services/instances/versions(R),operations | - |
| __App Engine Code Viewer__  | appengine.versions.getFileContents (ONLY role that can view code) | - |
| __App Engine Deployer__ | versions(CRD),applications/services/versions(R) - Deploy a new version of an app | - |
| __App Engine Service Admin__ | versions(RUD), applications(R), services/instances(CRUD),operations: split or migrate traffic, Start and stop a version | - |

App Engine Roles DO NOT allow us to
- view and download application logs
- view monitoring charts in the cloud console
- enable and disable billing

## Predefined Roles: Google Kubernetes Engine Roles

|  Roles | Description  | Use Case  |
|---|---|---|
|  __Kubernetes Engine Admin__ | Complete access to clusters and kubernetes API objects | - |
|  __Kubernetes Engine Cluster Admin__ | Provides access to management of clusters (cannot access kubernetes API objects - Deployments, Pods etc. | - |
| __Kubernetes Engine Developer__  | Manage kubernetes API objects (and read cluster info) | - |
| __Kubernetes Engine Viewer__  | Get/list cluster and kubernetes API objects | - |

## Predefined Roles: Google Cloud Storage Roles

|  Roles | Description  | Use Case  |
|---|---|---|
|  __Storage Admin__ | storage.buckets.*, storage.objects.* | - |
|  __Storage Object Admin__ | storage.objects.* | - |
| __Storage Object Creator__  | storage.objects.create | - |
| __Storage Object Viewer__  | storage.objects.get, storage.objects.list | - |

Note:
- Container Registry stores container images in Cloud Storage buckets
- Control access to images in Container Registry using Cloud Storage permissions
- Storage Admin can create buckets and play with objects
- Storage Object Admin CANNOT create buckets but can play with objects in a bucket

## Predefined Roles: Google Cloud BigQuery Roles

|  Roles | Description  | Use Case  |
|---|---|---|
| __BigQuery Admin__ | bigquery.* | - |
| __BigQuery Data Owner__ | bigquery.datasets.* , bigquery.models.* , bigquery.routines.* , bigquerytables.* (Does NOT have access to Jobs) | - |
| __BigQuery Data Editor__  | bigquery.tables.(create/delete/export/get/getData/getIamPolicy/list/update/updateData/updateTag), bigquery.models.* , bigquery.routines.* , bigquery.datasets.(create/get/getIamPolicy/updateTag | - |
| __BigQuery Data Viewer__  | get/list bigquery.(datasets/models/routines/tables) | - |
| __BigQuery Job User__ | bigquery.jobs.create | - |
| __BigQuery User__ | BigQuery Data Viewer + get/list (jobs, capacityCommitments, reservations etc) | - |

Note:
- To see data, you need either BigQuery User or BigQuery Data Viewer roles
- You CANNOT see data with BigQuery Job User roles
- BigQuery Data Owner or Data Viewer roles do NOT have access to jobs

## Predefined Roles: Google Logging and Service Account Roles

|  Roles | Description  | Use Case  |
|---|---|---|
| __Logs Viewer__ | Read all logs exceot Access Transparency logs and Data access audit logs | roles/logging.viewer |
| __Private Logs Viewer__ | Logs Viewer + Read Access Transparency logs and Data Access audit logs | roles/logging.privateLogViewer |
| __Logging Admin__ | All permissions related to Logging | roles/logging.admin |
| __Service Account Admin__ | Create and manage service accounts | roles/iam.serviceAccountAdmin |
| __Service Account User__ | Run operations as the service account | iam.serviceAccountUser |
| __Service Account Token Creator__ | Impersonate service accounts (create OAuth2 access tokens, sign blobs or JWTs, etc) | iam.serviceAccountTokenCreator |
| __Service Account Key Admin__ | Create and manage (and rotate) service account keys | roles/iam.serviceAccountKeyAdmin |

