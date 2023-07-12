# Build a platform

Platform Engineers build their Internal Developer Platforms (IDP) by leveraging the Humanitec Platform Orchestrator and Score.

## Why build an Internal Developer Platform with Humanitec?

Humanitec provides a platform-agnostic Workload specification called Score. Score eliminates configuration management between local and remote environments, meaning, developers can deploy their applications to any environment without having to change their configuration.

The Humanitec Platform Orchestrator works as a deployment engine that enables Platform Engineering teams to build golden paths for developers. This means that Platform Engineering teams can build a self-service model for developers to deploy their applications to the cloud and developers can deploy their applications without having to wait for the Platform Engineering teams to do it for them.

## What does the Platform look like?

We offer multiple ways to work with the Humanitec Platform Orchestrator.

You can use the Humanitec Platform Orchestrator UI, API, or CLI to manage your applications, environments, deployments, and more.

In some cases, a Terraform provider is also available.

## How does it work?

The Humanitec Platform Orchestrator allows you to configure and ship confidently, independently, and fast by providing a self-service model for developers to deploy their applications to the cloud.

Inform the Humanitec Platform Orchestrator that your applications are ready to deploy by connecting your CI pipeline to the Humanitec Platform Orchestrator.

For example, when a developer pushes code changes out to GitHub, the CI pipeline will build the application and push it to a container registry.

Because the Humanitec Platform Orchestrator applies the approach of _dynamic configuration management_ your application and infrastructure configurations are generated with by applying abstract requests, known as _workload specifications_ to baseline configurations provided by the platform engineering team.

## Next steps

Gain access to the Humanitec Platform Orchestrator by creating an Organization and connect your infrastructure to start building.

### Gaining access

An Organization Administrator or Manager can invite new users to join an existing Organization in Humanitec. An invitation involves sending an email that contains a one-time link that the invited User can follow to associate either their GitHub or Google Account with the Organization in Humanitec. The link expires after 7 days. If the link has expired before a User has accepted the invite, a new invite can be sent.

Users can be invited to an existing Organization from the Organization Settings.

1. Select **Organization settings** from the Organization menu.
2. In Organization Settings, select the **Organization members** tab.
3. Add the email address of the User to invite in the **Email** text box on the left hand side.
4. Select a role for the User to invite from the **Role** dropdown on the right hand side. Be aware that you will only have the option to invite Administrators to your Organization if you are an Administrator yourself.
5. To invite a user, select **Send invite**.

<!--
For more information, see [Organization Roles]({{< relref "/platform-orchestrator/security/rbac" >}}).
-->

### Connect your infrastructure

You can connect your infrastructure in many ways.

The easiest way to get started it to let the Humanitec know that your applications are ready to deploy, by connecting your CI pipeline to the Humanitec Platform Orchestrator.

- Connnect CI
- K8 cluster
- Database

#### Reference architecture

**Coming soon**

Alternatively, you can leverage the Reference architecture to quickly build the infrastructure for your Internal Developer Platform with the Humanitec Platform Orchestrator.
