# The Humanitec Platform Orchestrator

Build your enterprise-grade Internal Developer Platform with the Humanitec Platform Orchestrator and Score.

### What is it?

The Humanitec Platform Orchestrator is a set of interfaces (Web UI, CLI, API) which enables Platform Engineering teams to remove bottlenecks by letting them build golden paths for developers.

- Platform Engineering teams leverage the Humanitec Platform Orchestrator to provide a self-service model for developers to deploy their applications to the cloud.

- Developers use the workload specification [Score](./score.md) to generate the necessary configuration to deploy an application. The Humanitec Platform Orchestrator handles the infrastructure provisioning and deployment, defined by the Platform Engineering team, freeing up developers to focus on their applications.

### Key features

Key features of the Humanitec Platform Orchestrator include:

- Generates application and infrastructure configurations from workload specifications.
- Executes deployments and manage the lifecycle of resources.
- Integrates with adjacent tools like image registries, secrets managers, and CI/CD tools.
- Provisions resources through Drivers.
- Creates dynamic environments and deploy to them.
- Diffs, rolls back, debugs, inspect deployments.
- Promotes deployments between environments.
- Spins up new environments.

<!--
- **Application management**: Manage your applications, environments, deployments, and more.
- **Deployment engine**: Deploy your applications to any environment without having to change your configuration.
- **Self-service model**: Provide a self-service model for developers to deploy their applications to the cloud.
- **Dynamic configuration**: Leverage dynamic configuration to enable developers to deploy their applications to any environment without having to change their configuration.
-->

### How does it work?

Developers create a request to build their applications, and the Humanitec Platform Orchestrator pushes the changes through each environment, with the help of _Resource Definitions_ and _Drivers_. A request can be a `git push` to a code repository like, GitHub, GitLab, or Bitbucket.

The Platform Orchestrator receives the request and looks at the workload specification (like Score) in the code repository to determine what resources the application needs. It then finds the resource definitions, with Resource Matching, that match those resource types and the current environment. These resource definitions specify which driver to use for provisioning each resource.

The Platform Orchestrator calls the necessary drivers and passes them the configuration from the resource definitions. The drivers then provision the resources by calling APIs, using IaC tools, or other means.

Once the resources are provisioned, the Platform Orchestrator deploys the application code to the environment. It continues promoting the application through each environment, re-provisioning resources at each step based on the environment-specific resource definitions.

The Platform Orchestrator also handles ongoing management of environments, resources and deployments. It provides an API, CLI and UI to monitor the status of environments, deployments, and resources, manage resource definitions, revert deployments, create new environments, and more.

With the Humanitec Platform Orchestrator, Platform Engineering teams can ensure standardization across every deployment provisioned by the platform.

## Integrations and extensions

Integrate with your favorite developer tools to provide a self-service model for developers to deploy their applications to the cloud.

_Resource definitions_ tell the Platform Orchestrator how to resolve the abstract request from the workload specification (Score, for instance) to the correct _Driver_. This configuration can be done through the UI, API, CLI or the Terraform Provider (in beta).

Resource definitions define how a particular resource type should be provisioned in a given context. They contain:

- The resource type they apply to (e.g. postgres, aws-s3-bucket).
- Matching criteria to determine in which contexts they should be used (e.g. env_type: "production").
- Driver configuration detailing how the resource should be provisioned (e.g. AWS credentials, Docker image to use).
- Optionally, default values for the resource.

When the Platform Orchestrator needs to provision a resource, it will:

1. Look at the resource type requested (e.g. postgres)
2. Find all resource definitions matching that type
3. Filter those to find the best match for the current context (using the _Matching Criteria_)
4. Use the selected resource definition to determine which Driver to use and how to configure it
5. Provision the resource through the Driver, using any default values from the definition and values provided for the specific resource request.

Resource definitions define how resources should be created in a standardized way, and Drivers implement that provisioning through various tools and APIs. The Humanitec Platform Orchestrator brings these together to provision resources based on workload specification Score.

## Score

The workload specification Score provides a developer-centric and platform-agnostic Workload specification to improve developer productivity and experience. Score eliminates configuration management between local and remote environments.

### What is it?

Score is made up of two components, the _Score Specification_ and a _Score Implementation CLI_.

The _Score Specification_ is a developer-centric definition that describes how to run a Workload. As a platform-agnostic declaration file, `score.yaml` presents the single source of truth on a Workloads runtime requirements and works to utilize any container orchestration platform or tooling.

The _Score implementation (CLI)_ is a conversion tool (such as `score-compose` or `score-humanitec`) for developers and teams used to generate platform-specific configuration (such as `docker-compose.yam`l or a Delta Set) from the Score Specification.

### Key features

Score provides a set of features that enable developers to focus on their code and Platform Engineering teams to focus on the infrastructure.

- **Reduces cognitive load**: Score eliminates configuration management between local and remote environments.
- **Eliminates configuration mismanagement**: Score provides a single source of truth on a Workloads runtime requirements.
- **Separation of concerns between dev and ops**: Score enables developers to focus on their code and Platform Engineering teams to focus on the infrastructure.

## Next steps

If you are a platform team interested in building with the Humanitec Platform Orchestrator, you can get started by [building a platform](/home/build_a_platform.md).
If you are a developer interested in using the Humanitec Platform Orchestrator, you can get started by [using a platform](/home/use_a_platform.md).
