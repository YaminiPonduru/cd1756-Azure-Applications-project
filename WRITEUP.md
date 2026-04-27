# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
---------------------------------------------------------------------
Deployment Analysis and Decision :

1. Virtual Machine (VM) Analysis :

   Cost:
      Using a Virtual Machine involves higher operational costs because the user must pay for the VM instance continuously, regardless of usage. Additional costs may include storage, networking, and maintenance overhead. There is also indirect cost in terms of time spent managing updates, security patches, and configurations.

   Scalability:
        Scalability in a VM is manual. To handle increased traffic, additional VMs must be created and configured manually. Load balancing and scaling strategies require extra setup, making it less flexible compared to managed services.

   Availability:
        Availability depends on how well the VM is configured. High availability requires setting up multiple VMs, load balancers, and failover mechanisms manually. Without these, the application may face downtime if the VM fails.


Workflow: 

The workflow is more complex. Developers must:

* Manually configure the environment (Python, dependencies, web server)
* Handle deployments using scripts or manual uploads
* Maintain the system continuously
  This increases development and operational effort.

2. Azure App Service Analysis

Cost: 

Azure App Service follows a pay-as-you-use model and reduces operational costs since infrastructure management is handled by Azure. It eliminates the need for maintaining servers, making it cost-effective for web applications.

Scalability:

App Service provides built-in scalability:

* Vertical scaling (changing pricing tier)
* Horizontal scaling (adding instances)
  Auto-scaling can be configured easily, making it highly efficient for handling varying workloads.

Availability: 

App Service offers high availability by default. Azure manages infrastructure, ensuring uptime with minimal manual intervention. Features like load balancing and redundancy are built-in.

Workflow: 

The workflow is streamlined and developer-friendly:

* Easy integration with GitHub for CI/CD
* Automatic deployment on code push
* Built-in monitoring and logging
  This significantly reduces development and deployment complexity.

3. Final Decision
Chosen Solution: Azure App Service 

4. Justification

Azure App Service is the most suitable option for deploying the CMS application because it simplifies deployment and reduces operational overhead. It provides built-in scalability, high availability, and seamless integration with GitHub for continuous deployment. Additionally, it supports secure environment variables for managing sensitive data such as database credentials and API keys. Compared to Virtual Machines, App Service allows faster development, easier maintenance, and better resource management, making it the ideal choice for this application.

------------------------------------
Assess app changes that would change your decision.

Since Azure App Service is used, the application is modified to rely on environment variables for configuration and to follow a stateless design suitable for scalable cloud deployment. This removes the need to manage underlying infrastructure while ensuring easy integration with services like Azure SQL and Blob Storage. If more infrastructure control were required (as in a VM), additional setup such as server configuration, dependency management, and security handling would be necessary.



