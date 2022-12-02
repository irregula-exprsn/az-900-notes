# Azure Identity, governance, privacy and compliance

* Authentication:
    * Identifies the person or service seeking access to a resource.
    * Requests legitimate access credentials.
   ---
* Authorization:
    * Determines an authenticated person's or service's level of access.
    * Defines what they can access and what they can do with it.
---

## Identity Services

* Core Identity Services:
   * MFA:
        * Provides additional security for customer identities by requiring two or more elements for full authentication.
            1. *Something you know*.
            2. *Something you possess*.
            3. *Something you are*.
   ---
    * Azure Active Directory (AAD):
        * Cloud-based identity and access management service.
        * Capabilities:
            * Authentication (employees sign-in to access resources).
            * Single sign-on (SSO).
            * Application management (Authorization).
            * Business to Business (B2B).
            * Business to Customer (B2C) identity services.
            * Device management.
        * Uses *Conditional Access* to bring signals (user location, IP Address, Device, Application) together, to make decisions, and enforce organizational policies for access.

---

## Azure Governance Features

* Role-based Access Control (RBAC):
    * Allows fine-grain access management.
    * Segregates duties within the team and grant only the amount of access to users that they need to perform their jobs.
    * Enables access to the Azure portal and controls access to resources.
    ---
* Resource locks:
    * Protect your Azure resources from accidental deletion or modification.
    * Manage locks at *subscription, resource group, or individual resource levels* within Azure Portal.
    *  | Lock Type | Read | Update |Delete |
        |:---------------:|:------:|:-------:|:--------:|
        | CanNotDelete| Yes | Yes | No |
        | ReadOnly | Yes | No | No |
    ---
* Tags:
    * Provides metadata for Azure resources & logically organizes resources into a taxonomy.
    * Very useful for rolling up billing information.
    ---
* Policy:
    * Helps to enforce organizational standards and to assess compliance at-scale.
    * Provides governance and resource consistency with *regulatory compliance, security, cost, and management*.
    * Evaluates and identifies Azure resources that do not comply with organinization's policies.
    * Provides built-in policy and initiative definitions, under categories such as
        * Storage,
        * Networking,
        * Compute,
        * Security Center, and
        * Monitoring.
    ---
* Blueprints:
    * Makes it possible for development teams to rapidly build and stand up new environments.
    * Development teams can quickly *build trust* through organizational compliance with a set of built-in components (such as networking) in order to speed up development and delivery.
        * Policy Assignments
        * Resource Groups
        * Azure Resource Manager Templates
        * Role Assignments
    ---
* Cloud Adoption Framework:
    * Approach to cloud adoption in Azure.
        1. Strategy: *Define business justifications and expected outputs.*
        2. Plan: *Align actionable adoption plans to business outcomes.*
        3. Ready: *Prepare the cloud environment for the planned changes.*
        4. Migrate: *Migrate and modernize existing workloads.*
        5. Innovate: *Develop new cloud-native or hybrid solutions.*
        6. Govern: *Govern the environment and the workloads.*
        7. Manage: *Operations management for the cloud and hybrid solutions.*
    * Best practices from Microsoft employees, partners, and customers with tools, guidance, and narratives for strategies and outcomes.
---


## Azure Privacy & Compliance

* Trust Center:
    * Learn about security, privacy, compliance, policies, features, and practices across Microsoft’s cloud products.
    ---
* Compliance Documentation:
    * Microsoft offers a comprehensive set of compliance offerings to help your organization comply with *national, regional, and industry-specific* requirements that govern the collection and use of data.
    ---
* Sovereign Regions:
    * Azure Government:
        * Meets the security and compliance needs of US federal agencies, state and local governments, and their solution providers.
    * Azure China:
        * Microsoft is China’s first foreign public cloud service provider, in compliance with government regulations *operated by 21Vianet*.
---