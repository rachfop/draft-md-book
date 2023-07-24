# Introduction

The Humanitec Platform Orchestrator powers your Internal Developer Platform (IDP) by removing infrastructure bottlenecks and creating golden paths for developers. It does this by enabling developers to request the workloads and resources needed for their application code. The platform team then responds by defining how those resources will be provisioned with the Platform Orchestrator.  


## Overview

This introduction provides an overview of how the Platform Orchestrator works within the context of your IDP:

### Score

Developers use a Workload Specification, known as Score, to describe resources needed to run their application code.
When a developer pushes a change to their code repository, the CI/CD pipeline notifies the Platform Orchestrator of the request to provision resources.

For information on how to connect an existing CI/CD pipeline to notify the Platform Orchestrator, see CI/CD.

### The Humanitec Platform Orchestrator

The Humanitec Platform Orchestrator bridges the gap between developers' application code and the infrastructure used to run it.

When the Platform Orchestrator receives a request for Resources, it matches the request to the baseline configuration designed by the platform team.
For example, if a developer requests a Postgres resource with the Environment name of `developement`, the Platform Orchestrator acknowledges the request and matches the Postgres resource to what’s defined in the Resource Definition. This could include additional Resource Dependencies, such as routes or DNS.

Drivers implement the provisioning of Resource Definitions by either a create, update, or delete action when developers push updates to their Workload.

For more information on Resources, see Resource Definition Overview.
For more information on Drivers, see Drivers, Custom Drivers, or Built-in Drivers.

## Conclusion

Developers define their workload and resource dependencies in a Score file.
Platform teams define how resources are provisioned, with Resource Definitions and matching criteria to specify where to apply the Resources.

The Humanitec Platform Orchestrator removes friction by connecting developer infrastructure needs through an automated provisioning process. This allows developers to focus on writing code rather than configuring for each deployment.

## Next steps


If you’re part of a platform team and interested in powering your IDP with the Humanitec Platform Orchestrator, see what it’s like to build a platform.
If you’re a developer interested in how the Platform Orchestrator works, get started by using a platform.
To understand more about application deployment, head to our tutorial Deploy your Application.
For more info on the Humanitec Platform Orchestrator, check out our Concepts and Philosophy section.
