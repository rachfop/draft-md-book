# Use a platform

Developers use Score a workload specification, to deploy their applications to their Internal Developer Platform.
The Humanitec Platform Orchestrator then takes care of the rest.

## Why use an Internal Developer Platform?

Internal Developer Platforms (IDP) enable developers to deploy their applications to the cloud without having to wait for the Platform Engineering team to do it for them.

Developers can deploy their applications to the cloud using the Humanitec Platform Orchestrator without having to know the underlying infrastructure.

This helps speed up development and deployment cycles and enables developers to focus on what they do best: writing code.

## What does the platform look like?

With Score and the Humanitec Platform Orchestrator, you can deploy your applications with a `git push` and allow your Platform Engineering team to manage the underlying infrastructure.

## How does it work?

Score simplifies the management of infrastructure, by relying on _dynamic configuration management_.

With Score, declare your resources, such as databases, queues, and caches, as abstract requests, known as _workload specifications_ and the Humanitec Platform Orchestrator will generate the configuration for you.

The Humanitec Platform Orchestrator simplifies the management of infrastructure by relying on _dynamic configuration management_. With this, you can declare your resources, such as databases, queues, and caches, as abstract requests, known as _workload specifications_, and the Humanitec Platform Orchestrator will generate the configuration for you.

The Orchestrator uses Drivers to implement the platform and to create or update infrastructure resources. These Drivers, which can be built-in or custom, establish connections to your infrastructure and can be used to connect to different cloud providers such as AWS, Google Cloud, and Azure. They fulfill a Driver Interface that allows the Orchestrator to create and destroy resources as required by deployments. Drivers typically call APIs associated with managed services using the credentials provided by resource accounts.

Resource accounts are identities used to provision and manage resources through dynamic resource definitions. They can represent a range of identities, including cloud provider service accounts, VPN accounts, SSH accounts, and other credentials.

## Next steps?

Your Platform Engineering team should have already built a platform with the Humanitec Platform Orchestrator.

Get access to your team's organization and start deploying your applications to the cloud.

### Gaining access

You should be invited by your organization and have credentials through Single Sign-on (SSO).
Check your email or reach out to your Platform Engineering team for more information.

### Developing Apps and Workloads with Humanitec
