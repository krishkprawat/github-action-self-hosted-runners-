# github-action-self-hosted-runners-

this repo is for the self hosted runner test project
we have to configure inbound and outbound rules
open http and https ports because aws/github needs to be conenct with each other.
becaues both cant be in same network, github can be public hosted and aws can be in vpc.
Inbound traffic - http - ipv4- port 80 - https -ipv4-
outbound traffic - http - ipv4- port 80 - https -ipv4-

1. open github project - settings- action - runners- + new self hosted runner
2. select runner image (linux)
3. select architecture - amd/arm
4. execute the steps mentioned on the screen (run all commands on ec2)

A self-hosted runner is a machine or virtual environment that you set up and manage yourself to execute GitHub Actions workflows in your GitHub repositories. Unlike GitHub-hosted runners, which are provided and maintained by GitHub, self-hosted runners run on your own infrastructure.

if we are enterprise comoany , we are using private repos. we are more focusd on security .then you have to use self hosted runners.

When to Use Each:
GitHub-Hosted Runners: Use GitHub-hosted runners when you need a quick and straightforward solution, you have minimal customization requirements, and you want to take advantage of GitHub's managed infrastructure. They are well-suited for smaller projects or when you want to avoid the hassle of maintaining runners.

Self-Hosted Runners: Choose self-hosted runners when you require specific custom environments, faster build times, cost control, and the ability to access local resources. They are suitable for larger projects and enterprises with complex requirements.
Use Self-Hosted Runners When:
Custom Environments: You require a high degree of customization for the runner's environment. Self-hosted runners give you full control over the operating system, software, libraries, and tools, allowing you to create a tailored environment.

Access to Local Resources: Your workflows need access to resources that are only available within your local network or on-premises systems. Self-hosted runners can connect to these resources directly.

Security and Compliance: Your organization has strict security and compliance requirements that require fine-grained control over runner access, secrets management, and encryption.

Faster Builds and Execution: You need to optimize build and execution times for your workflows. Self-hosted runners can be equipped with powerful hardware resources to achieve faster performance.

Cost Control: You want to have control over the cost of the infrastructure used for running workflows. Self-hosted runners can run on your existing hardware or cloud instances, potentially leading to cost savings.

Specialized Use Cases: Your project requires specialized software or configurations that are not available on GitHub-hosted runners. This is common for projects with unique tooling or dependencies.

Distributed Workloads: Your workflows involve distributed or parallel processing and require precise control over resource allocation and management.

Use GitHub-Hosted Runners When:
Convenience and Quick Start: You want a convenient and hassle-free way to run CI/CD pipelines without the need for setting up and managing runners. GitHub-hosted runners are ready to use immediately.

Standard Environments: Your project's requirements align with the standard environments provided by GitHub-hosted runners. These runners offer a range of common operating systems and software tools.

Scalability: Your project needs the ability to scale automatically to accommodate increased workflow demands. GitHub-hosted runners can scale based on usage.

Shared Infrastructure: You are working on a small to medium-sized project where resource sharing among users is acceptable.

Cost Predictability: GitHub-hosted runners are included in your GitHub Actions plan, providing cost predictability without the need to manage separate infrastructure costs.

In practice, many organizations use a combination of both self-hosted and GitHub-hosted runners. This allows them to balance convenience, scalability, and customization based on the requirements of their projects. The choice ultimately depends on your specific needs and the trade-offs you are willing to make regarding control, convenience, and cost.






thanks for reading...
