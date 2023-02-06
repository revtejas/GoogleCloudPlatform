Now let’s examine how you can use Cloud Storage for unstructured data storage.

Cloud Storage is a fully managed scalable service that has a wide variety of uses.
A few examples include serving website content, storing data for archival and disaster recovery,
and distributing large data objects to end users through Direct Download.

Cloud Storage’s primary use is whenever binary large-object storage (also known as
a “BLOB”) is needed for online content such as videos and photos, for backup and
archived data, and for storage of intermediate results in processing workflows.

### what is object storage?
Object storage is a computer data storage architecture that manages data as “objects”
and not as a file and folder hierarchy (file storage), or as chunks of a disk (block storage).
- These objects are stored in a packaged format that contains the binary form of the actual
data itself, relevant associated metadata (such as date created, author, resource type,
and permissions), and a globally unique identifier.
- These unique keys are in the form of URLs, which means object storage interacts well
with web technologies.
- Data commonly stored as objects includes video, pictures, and audio recordings.
- Cloud Storage is Google’s object storage product.
- It allows customers to store any amount of data and to retrieve it as often as needed.

In this lesson, we’ll learn more about Cloud Storage use cases, features, and pricing.
- There are four primary storage classes in Cloud Storage, and stored data is managed
and billed according to which class it belongs in.
- The first is Standard Storage.
Standard Storage is considered best for frequently accessed, or “hot,” data.
It’s also great for data that is stored for only brief periods of time.
- The second storage class is Nearline Storage.
This is best for storing infrequently accessed data, like reading or modifying data once
per month on average.
Examples include data backups, long-tail multimedia content, or data archiving.
- The third storage class is Coldline Storage.
This is also a low-cost option for storing infrequently accessed data.
However, as compared to Nearline Storage, Coldline Storage is meant for reading or modifying
data, at most, once every 90 days.
- The fourth storage class is Archive Storage.
This is the lowest-cost option, used ideally for data archiving, online backup, and disaster
recovery.
It’s the best choice for data that you plan to access less than once a year, because it
has higher costs for data access and operations and a 365-day minimum storage duration.

Although each of these four classes has differences, it’s worth noting that several characteristics
apply across all these storage classes.
These include: 
- Unlimited storage with no minimum object size
requirement
- Worldwide accessibility and locations,
- Low latency and high durability 
- A uniform experience, which extends to security
tools, and APIs
- Geo-redundancy if data is stored in a multi-region
or dual-region.
So this means placing physical servers in geographically diverse data centers to protect
against catastrophic events and natural disasters and load-balancing traffic for optimal performance.

### Cloud Storage files are organized into buckets.
A bucket needs a globally unique name and a specific geographic location for where it
should be stored, and an ideal location for a bucket is where latency is minimized.
For example, if most of your users are in Europe, you probably want to pick a European
location--either a specific Google Cloud region in Europe, or else the EU multi-region.

The storage objects offered by Cloud Storage are “immutable,” which means that you
do not edit them, but instead a new version is created with every change made.

Administrators can either allow each new version to completely overwrite the older one or keep
track of each change made to a particular object by enabling “versioning” within
a bucket.

If you choose to use versioning, Cloud Storage will keep a detailed history of modifications
-- that is, overwrites or deletes -- of all objects contained in that bucket.

If you don’t turn on object versioning, by default new versions will always overwrite
older versions.

With object versioning enabled, you can list the archived versions of an object, restore
an object to an older state, or permanently delete a version of an object, as needed.
Cloud Storage also offers lifecycle management policies for your objects.
For example, you could tell Cloud Storage to delete objects older than 365 days, or
to delete objects created before January 1, 2013, or to keep only the 3 most recent versions
of each object in a bucket that has versioning enabled.

We’ll look more closely at object lifecycle management in just a few minutes.
Cloud Storage’s tight integration with other Google Cloud products and services means that
there are many additional ways to move data into the service.
For example, you can import and export tables to and from both BigQuery and Cloud SQL.
You can also store App Engine logs, Firestore backups, and objects used by App Engine applications
like images.
Cloud Storage can also store instance startup scripts, Compute Engine images, and objects
used by Compute Engine applications.
