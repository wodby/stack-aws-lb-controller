# AWS Load Balancer controller Kubernetes system stack for Wodby

AWS Load Balancer Controller supplies AWS load-balancer integration for Wodby
Kubernetes clusters that require the AWS controller.

This repository defines the Wodby stack manifests and default service
composition for AWS Load Balancer controller.

- [Wodby Kubernetes platform](https://wodby.com)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## System service definitions

- [AWS Load Balancer controller system service](https://github.com/wodby/service-aws-lb-controller)

## What's included

| Component / service | Default configuration |
| --- | --- |
| AWS Load Balancer controller (`aws-lb-controller`)<br>`aws-lb-controller` | required; enabled by default |

System services are enabled or disabled according to the cluster provider and
infrastructure configuration.

## Role in Wodby infrastructure

Wodby installs this stack as a cluster-owned system app when it is required by
the Kubernetes provider or selected infrastructure configuration. It is not a
template for user-deployed applications.

Installation order, enabled services, and settings can vary by cluster type.
Wodby coordinates its lifecycle with cluster provisioning and infrastructure
upgrades.

## Platform maintenance

Changes can affect existing clusters. Preserve stack service names and service
references unless the backend provisioning and upgrade paths are updated at the
same time.

Wodby platform maintainers can validate the manifests with:

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

See the [stack manifest reference](https://wodby.com/docs/2.0/stacks/template/) and the [managed services index](https://github.com/wodby/services).
