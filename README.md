# AWS Load Balancer controller Kubernetes system stack for Wodby

AWS Load Balancer Controller supplies AWS load-balancer integration for Wodby
Kubernetes clusters that require the AWS controller.

This repository defines the Wodby stack manifests and default service
composition for AWS Load Balancer controller.

<!-- wodby:generated:start -->

## Stack contract

- [AWS Load Balancer controller stack on Wodby](https://wodby.com/stacks/aws-lb-controller)
- [Wodby Kubernetes platform](https://wodby.com)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## System service definitions

- [AWS Load Balancer controller system service](https://github.com/wodby/service-aws-lb-controller)

## What's included

| Component / service | Default configuration |
| --- | --- |
| AWS Load Balancer controller<br>`aws-lb-controller` | required; enabled by default |

System services are enabled or disabled according to the cluster provider and
infrastructure configuration.

## Validate the stack manifest

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

<!-- wodby:generated:end -->
