# Azure Blob Storage

### What is Azure Blob Storage?

Azure Blob Storage is a scalable and secure object storage service provided by Microsoft Azure. It is designed for storing and managing large amounts of unstructured data such as text, images, videos, documents, and binary data. Blob Storage offers high availability, durability, and global accessibility, making it suitable for various scenarios such as backups, content distribution, archival storage, and application data storage.

### Difference between Blob Storage and the File System of Linux/Windows/Mac (Hierarchical File Storage)

Blob Storage and the file systems of Linux/Windows/Mac (Hierarchical File Storage) differ in their fundamental concepts and usage:

- Blob Storage: Blob Storage is an object-based storage solution where data is organized into containers and blobs. It provides a flat namespace, meaning that each blob has a unique identifier and can be directly accessed using its URL. Blob Storage is optimized for storing and retrieving large volumes of unstructured data and offers features like scalability, redundancy, and tiered storage options.

- File System (Linux/Windows/Mac): The file system of Linux/Windows/Mac follows a hierarchical directory structure where files are organized into directories and subdirectories. It allows for the creation, modification, and deletion of files and directories, and supports file-level operations such as read, write, and execute permissions. File systems are typically used for general-purpose file storage and management within an operating system.

### Advantages/Disadvantages of Blob Storage

Advantages of Blob Storage include:

- Scalability: Blob Storage can scale to accommodate massive amounts of data, allowing organizations to handle growing storage requirements efficiently.
- Durability: Blob Storage offers high durability, ensuring that data remains available even in the event of hardware failures or data center disruptions.
- Accessibility: Blobs can be accessed globally over HTTP or HTTPS, making it easy to distribute and share data with users or applications worldwide.
- Cost-effective: Blob Storage provides cost-effective storage options, including tiered storage, which allows organizations to optimize costs based on the access patterns and importance of data.

Disadvantages of Blob Storage include:

- Limited file system features: Blob Storage is optimized for object storage and lacks some of the advanced file system features found in traditional file systems.
- Increased complexity for certain scenarios: While Blob Storage offers great flexibility, managing and organizing large numbers of blobs can become complex, requiring proper naming conventions and organization strategies.

### Different Tiers

Azure Blob Storage offers different storage tiers to cater to various workload requirements and cost considerations:

1. Hot Access Tier: The Hot tier is optimized for frequent and regular access to data. It offers higher storage costs but lower access costs, making it suitable for frequently accessed data.

2. Cool Access Tier: The Cool tier is designed for infrequently accessed data. It provides lower storage costs but higher access costs compared to the Hot tier. This tier is ideal for data that is accessed less frequently but still requires quick access when needed.

3. Archive Access Tier: The Archive tier is the most cost-effective option, optimized for long-term retention and archival storage. It has the lowest storage costs but incurs higher access and retrieval costs. The Archive tier is suitable for data that is rarely accessed and can tolerate longer retrieval times.

### Parts of Azure Blob Storage: Account, Container, Blobs - How Do They Relate?

- Account: An Azure Blob Storage account serves as a top-level namespace for organizing and managing blobs. It represents a unique storage resource in Azure and provides authentication and access control mechanisms.

- Container: Containers are logical storage units within an Azure Blob Storage account. They act as a way to group related blobs together. Containers are similar to directories in

### Redundancy Types in Azure Blob Storage

Azure Blob Storage offers several redundancy options to ensure data durability and availability. These afect data's criticality, access requirements, and cost considerations.

 LRS (Locally Redundant Storage)

- LRS provides locally redundant storage within a single Azure data center. It replicates data synchronously within three copies stored in separate fault domains within the data center. LRS offers a cost-effective redundancy option for scenarios where high availability across data centers is not required.

 ZRS (Zone-Redundant Storage)

- ZRS replicates data synchronously across multiple availability zones within a region. It ensures high durability and availability by storing three copies of the data in different zones. ZRS provides better protection against failures that affect an entire data center or zone.

GRS (Geo-Redundant Storage)

- GRS provides geo-redundancy by asynchronously replicating data to a paired Azure region, which is physically distant from the primary region. It maintains six copies of the data, three in the primary region and three in the secondary region. GRS offers higher data durability and availability across regions, enabling data recovery in the event of a regional outage.

RA-GRS (Read-Access Geo-Redundant Storage)

- RA-GRS offers the same redundancy as GRS, with the additional capability of read access to the replicated data in the secondary region. This allows read operations on the data even if the primary region is unavailable.

GZRS (Geo-Zone-Redundant Storage)

- GZRS combines the redundancy of ZRS with the geo-replication of GRS. It replicates data synchronously across multiple availability zones within a primary region and asynchronously to a paired secondary region. GZRS provides high durability, availability, and data recovery across zones and regions.

RA-GZRS (Read-Access Geo-Zone-Redundant Storage)

- RA-GZRS combines the features of RA-GRS and GZRS. It offers the highest level of redundancy and availability by providing read access to the replicated data in both the primary and secondary regions.

### Using Blob Storage Code Along

### Adding Cat Jpg to App

1. SSH into Azure VM:

```
ssh -i ~/.ssh/tech241-henry-az-key adminuser@4.234.113.95
```

2. Install Azure CLI:

```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

3. Login to Azure:

```
az login
```

4. Download a cat picture (jpg) to your VM:

```
wget https://m.media-amazon.com/images/I/91HiqSzRYwL._AC_UF894,1000_QL80_.jpg -O newcat.jpg

```

5. Upload the cat picture to Azure blob storage:

```
az storage blob upload --account-name tech241henrystorage --container-name testcontainer --name uploadedcat.jpg --type block --source newcat.jpg
```


6. Set access permissions so it can be viewed by the public:

```
az storage blob set-permission --account-name tech241henrystorage --container-name testcontainer --name uploadedcat.jpg --public-access blob
```

7. Modify the file index.ejs (found in the views folder inside the app folder) - add an `<img>` tag to the HTML to display the uploadedcat.jpg image on the Sparta front page.

Edit the index.ejs file and add the following code:

```
<img src="https://tech241henrystorage.blob.core.windows.net/testcontainer/uploadedcat.jpg"
```

8. Run the app 
