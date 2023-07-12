# The Humanitec Platform Orchestrator

Build your enterprise-grade Internal Developer Platform with the Humanitec Platform Orchestrator and Score.

### What is it?

The Humanitec Platform Orchestrator is a set of interfaces (Web UI, CLI, API) which enables Platform Engineering teams to remove bottlenecks by letting them build golden paths for developers.
Platform Engineering teams leverage the Humanitec Platform Orchestrator to provide a self-service model for developers to deploy their applications to the cloud.

The Platform Orchestrator uses _dynamic configuration_ and _declarative infrastructure_ which enables developers to deploy their applications to any environment without having to change their configuration.

### Key features

The Humanitec Platform Orchestrator provides a set of features that enable Platform Engineering teams to build golden paths for developers.

Such features include:

- **Application management**: Manage your applications, environments, deployments, and more.
- **Deployment engine**: Deploy your applications to any environment without having to change your configuration.
- **Self-service model**: Provide a self-service model for developers to deploy their applications to the cloud.
- **Dynamic configuration**: Leverage dynamic configuration to enable developers to deploy their applications to any environment without having to change their configuration.

### How does it work?

Developers create a request to build their applications, and the Humanitec Platform Orchestrator pushes the changes through each environment, with the help of _Drivers_.
Platform Engineering teams define how resources are provisioned with Resource Definitions.
To achieve this, a developer might use the workload specification [Score](#score), to define how their workload should run and the Humanitec Platform Orchestrator responds by:

1. Determining the required resources with dynamic configuration.
2. Using Drivers to create, update, or delete the required resources based on Resource Definitions.
3. Injecting the required configuration and secrets into the applications.
4. Provisioning the resources and running the final deployment.

With the Humanitec Platform Orchestrator, Platform Engineering teams can ensure standardization across every deployment provisioned by the platform.

## Integrations and extensions

Integrate with your favorite developer tools to provide a self-service model for developers to deploy their applications to the cloud.

The Humanitec Platform Orchestrator supports a variety of extensions in the form of Drivers. Drivers are HTTP Web Services that implement the [Humanitec Driver API](https://developer.humanitec.com/drivers/reference/api-spec/), serving as the underlying code that runs to provision resources. They're crucial for integrating the Orchestrator with various other systems and services, as they perform operations and changes to the infrastructure.

Depending on their implementation, Drivers' behavior can range from simple to complex. For instance, the static Driver merely returns pre-canned values with no side-effects, whereas the Terraform Driver executes Terraform, returns outputs from Terraform, and usually leads to infrastructure being created, updated, or destroyed.

Platform Engineering teams leverage Drivers in Resource Definitions, which outline how resources are provisioned. In essence, Drivers are responsible for creating, updating, and deleting resources based on a unique ID and producing outputs that can are injected into Workloads or referenced in other Resource Definitions.

An essential part of the Resource Definitions is Driver Inputs. These are the specific parameters passed to the Resource Driver that performs the provisioning of a resource. The schema of the Driver Inputs depends on the particular Driver. For instance, provisioning a DNS resource with the `humanitec/dns-cloudflare` Driver necessitates the Cloudflare Zone ID and the parent domain to be specified. In contrast, the `humanitec/dns-wildcard` Driver only requires the parent domain.

By utilizing Drivers and specifying appropriate resource definitions, you can easily extend and customize the capabilities of the Humanitec Platform Orchestrator to suit your needs and integrate with the tools and platforms you are already using.

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
