# Write-up Template

### Application Requirement




- Since users could be more or less per time, we should be able to scale up 
  or down.

### What we don't care about
- The Operating System - App is not complex, so we don't need to change 
  anything on this layer
- Multiple languages - The project is built with a single language python 
  hence, we don't need multiple language feature

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
```
  - Cost
  AppService:  No Pay-as-you-Go option, you keep paying even when yout 
  using but still cheaper than VM
  VM: They are more expensive
  
  - Scalability
  VM - Provides more scalability
  Appservice -  Scalable but not as much as VM since it's restricted on 
  size. Auto -scaling is a plus
  
  - Availability
  VM - Multiple VMs can be grouped to provide high availability, scalability, and redundancy.
  AppService -  High availability
  
  - Workflow
  VM - Deployment is more time consuming
  App Service- Quick and painless deployment with built in supported languages
```

- *Choose the appropriate solution (VM or App Service) for deploying the app*

  I chose `App Service` because of the reasons below.
- Since this is a simple webapp, 14GB of memory and 4 vCPU cores per instance 
  would be good enough for deployment.
- I don't need to control the underlying operating system or use any 
  custom software.
- It is more cost-effective compared to VM - I can set the amount of hardware 
  allocated to host the application.
- High availability - It supports both Vertical and Horizontal scaling  
  auto-scaling, I can scale on demand.
- With support for GitHub, Azure DevOps, or any Git repo, deployment is easy.

### Assess app changes that would change your decision.
Some change that might affect my last decision
- Support for another language that is not currently supported by App Service.
- If the application becomes more complex, and I need to have more OS control 
  e.g. for security reasons
- Increase in the number of user to the extent that 14GB of memmory and 
  4vCPU cores become insufficient.
