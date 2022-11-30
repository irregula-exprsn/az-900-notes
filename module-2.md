# Core Azure Services

## [Azure Architectural Components](https://learn.microsoft.com/en-us/azure/reliability/availability-zones-overview)

* Regions:
    * Regions are made up of *one or more datacenters* in close proximity.
    * Provide flexibility and scale *to reduce customer latency*.
    * Preserve data residency with a comprehensive *compliance* offering.
  ---
* Availability Zones:
    * Provide protection against downtime due to datacenter failure.
    * Physically separate datacenters within the same region.
    * Each datacenter is equipped with independent power, cooling, and networking.
    * Connected through private fiber-optic networks.
---

## Core Azure Resources
* Azure resources are components like storage, virtual machines, and networks that are available to build cloud solutions.

1. Resource Group:
    * Container to manage and aggregate resources in a single unit.
    * Resources can exist in only one resource group.
    * Resources can exist in different regions.
    * Resources can be moved to different resource groups.
    * Applications can utilize multiple resource groups.
   ---

2. Azure Resource Manager:
    * Provides a *management layer* that enables customers to create, update, and delete resources in their Azure subscription.
   ---

3. Azure Subscription:
    * Provides customers with authenticated and authorized access to Azure accounts.
    * *Billing boundary:* generate separate billing reports and invoices for each subscription.
    * *Access control boundary:* manage and control access to the resources that users can provision with specific subscriptions.
   ---

4. Management Groups:
    * Management groups can include multiple Azure subscriptions.
        ```json
        {
            "ManagementGroups": [
                "Susbscriptions": [
                    "Resource Groups": [
                        "Resources": ["VMs", "VNets", "Functions"]
                    ]
                ]
            ]
        }
        ```
    * Subscriptions inherit conditions applied to the management group.
    * 10,000 management groups can be supported in a single directory.
    * A management group tree can support up to six levels of depth.
   ---

* Azure Compute Services:
    * Azure **compute** is an on-demand computing service that provides computing resources such as disks, processors, memory, networking, and operating systems.

        * VMs:
            * Azure Virtual Machines (VM) are software emulations of physical computers.
            * Includes virtual processor, memory, storage, and networking.
            * IaaS offering that provides total control and customization.
          ---
        * App Services:
            * Azure App Services is a fully managed platform to build, deploy, and scale web apps and APIs quickly.
            * Works with .Net, .NetC Core, Node.js, Java, Phython, or php.
            * PaaS offering with enterprise-grade performance, security, and compliance requirements.
          ---
        * Container Instances:
            * PaaS offering to run containers in Azure, without having to provision any VMs or adopt a higher-level orchestration service.
          ---
        * Kubernetes Service:
            * Lets you orchestrate Docker containerized application deployments with Kubernetes.
          ---
        * Virtual Desktop:
            * Manage virtual desktops and applications to enable corporate network and data access to users, anytime, anywhere, from supported devices.

     ---

* Azure Networking Services:
    * Virtual Network (VNet):
        * Provides an *isolated, private environment* in the cloud.
        * Enables Azure resource to communicate with each other, the internet, and the on-premise networks.
        * Users have control over their virtual networking environment, including selection of their own IP address range, creation of subnets, and configuration of route tables and network gateways.
      ---
    * VPN Gateway (VPN):
        * Provide a *secure connection* between an Azure Virtual Network and an on-premises location *over the internet* to send encrypted data.
        * Allows end users to connect to Azure services through VPN tunneling (Point To Site).
      ---
    * Express Route:
        * Establishes a *dedicated, private network connection* from a location to the cloud provider (not over the Internet).
      ---
    * Load Balancer:
        * Balances the load of incoming Internet traffic into a system or application.
        * Distributes new inbound flows that arrive on the Load Balancer's frontend to backend pool instances, according to rules and health probes.
            * *Inbound flows* is the traffic from the Internet or local network,
            * *Frontend* is the access point for the LB,
            * *Backend pool* is the VMs receiving the traffic,
            * *Rules & health probes* ensures backend instances can receive the data.
        * Uses IP address and port number to determine the receiving VM in the backend pool.
      ---
    * Application Gateway:
        * Layer 7 load balancer.
        * Distributes incoming traffic based on HTTP request properties such as URL and host headers.
        * Supports SSL termination, cookie-based session affinity, and round robin for load-balancing traffic.
      ---
    * Front Door (Content Delivery Network):
        * Distributed network of servers that can deliver low-latency web content to users.
        * Delivers high performance, scalability, and secure user experiences for customer's content and applications.
    ---

* Azure Storage Services:
    * Storage access tiers:
        | Hot | Cool | Archive|
        | :---: | :----: | :-------: |
        | Optimized for storing data that is accessed frequently. | Optimized for storing data that is infrequently accessed and for at least 30 days. | Optimized for storing data that is rarely accessed and stored for at least 180 days with flexible latency requirements. |
      ---
    * Container storage (blob):
        * Provides durable data storage for Azure VMs.
      ---
    * Files:
        * Sets up a highly available network file shares that can be accessed by using the standard Server Message Block (SMB) protocol.
    ---

* Azure Database Services:
    * Cosmos DB:
        * Globally distributed, multi-model database that natively supports multiple data models including key-value pairs, documents, graphs, and columnar.
      ---
    * SQL DB, DB for MySQL, DB for PostgreSQL, & DB for MariaDB:
        * Managed relational database services in which resiliency, scale and maintenance are primarily handled by the Azure platform.
      ---
    * SQL Managed Instance:
        * Allows existing SQL Server customers to *lift and shift* their on-premises applications to the cloud with minimal application and database changes.
    ---

* Azure Marketplace:
    * Allows customers to find, try, purchase, and provision applications and services from hundreds of leading service providers, which are all certified to run on Azure.

---