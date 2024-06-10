---
title: "Module - ALB"
chapter: true
weight: 2
---

## Module - ALB

### Setting SLOs on an Application Load Balancer <!-- MODIFY THIS SUBHEADING -->

Amazon's Application Load Balancer is a popular infrastructure component found in many application architectures in AWS.

Because load balancers route traffic to application services, they make an ideal place to set SLOs. You might think to
set SLOs on the health of the load balancer itself, especially if there is a known failure
mode related to the load balancer -- such as, say, traffic that spikes faster than an ALB can adaptively scale.

SLOs on ALB health are certainly a valid use case. However, a more typical use of SLOs on an ALB is to set SLOs on the behavior 
of the services behind it, using the ALB as a convenient pulse point to measure the performance and stability of the
services themselves. That's what we'll do in this module.

{{% notice warning %}}
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be architected to build a solution while demonstrating best practices along the way. These examples are not intended for use in production environments.
{{% /notice %}}
