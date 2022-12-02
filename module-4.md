# Azure Security and Network Security

## Security tools and features

* Security Center:
    * Monitoring service that provides threat protection across both Azure and on-premises datacenters.
        * Provides security recommendations
        * Detect and block malware
        * Analyze and identify potential attacks
        * Just-in-time access control for ports
    * Capabilities:
        * Policy compliance:
            * Run policies across management groups, subscriptions, or tenants.
        * Continuous assessment:
            * Asses new & deployed resources to ensure that they are configured properly.
        * Tailored recommendations:
            * Recommendations based on existing workload with instructions on how to implement them.
        * Threat protection:
            * Analyze attempted threats & impacted resource reports.
  ---

* Sentinel:
    * SIEM and SOAR solution that provides security analytics and threat intelligence across an enterprise.
    ---

* Key Vault:
    * Stores application secrets in a centralized cloud location in order to securely control access permissions and access logging.
        * Secrets management.
        * Key management.
        * Certificate management.
        * Storing secrets backed by hardware security modules (HSMs).
     ---

* Azure Dedicated Host:
    * Provides physical servers that host one or more Azure virtual machines that is dedicated to a single organization’s workload.
    * Benefits:
        * Hardware isolation at the server level.
        * Control over maintenance event timing.
        * Aligned with Azure Hybrid Use Benefits.

---

## Secure network connectivity

* *defense-in-depth* approach:
    * The objective of defense in depth is to protect information and prevent it from being stolen by those who aren’t authorized to access it.
    * Provides multiple levels of protection.
        1. The *physical security* layer is the first line of defense to protect computing hardware in the datacenter.
        2. The *identity and access* layer controls access to infrastructure and change control.
        3. The *perimeter* layer uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users.
        4. The *network* layer limits communication between resources through segmentation and access controls.
        5. The *compute* layer secures access to virtual machines.
        6. The *application* layer helps ensure that applications are secure and free of security vulnerabilities.
        7. The *data* layer controls access to business and customer data that you need to protect.
    * Attacks against one layer are isolated from subsequent layers.
     ---

* Network Security Groups:
    * Filter network traffic to and from Azure resources on Azure Virtual Networks.
        * Set inbound and outbound rules to filter by source and destination IP address, port, and protocol.
        * Add multiple rules, as needed, within subscription limits.
    ---

* Firewall:
    * Stateful, managed Firewall as a Service (FaaS) that grants/denies server access based on originating IP address, in order to protect network resources.
        * Applies inbound and outbound traffic filtering rules,
        * Built-in high availability,
        * Unrestricted cloud scalability, &
        * Uses Azure Monitor logging.
    ---

* Distributed Denial of Service (DDoS) protection:
    * DDoS attacks overwhelm and exhaust network resources, making apps slow or unresponsive.
    * Sanitizes unwanted network traffic before it impacts service availability.
    * Basic service tier is automatically enabled in Azure.
    * Standard service tier adds mitigation capabilities that are tuned to protect Azure Virtual Network resources.
    ---

* *defense-in-depth* is achieved by combining network security solutions.
    * *Perimeter* layer protects your network boundaries with Azure *DDoS Protection* and Azure *Firewall*.
    * *Networking* layer only permits traffic to pass between networked resources with *Network Security Group (NSG)* inbound and outbound rules.

---