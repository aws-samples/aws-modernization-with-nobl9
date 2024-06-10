---
title: "Locate Your ALB" # MODIFY THIS TITLE
chapter: true
weight: 2 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Where to start with an ALB

### A Look at PetAdoptions
First let's take a quick look at the web application. Obtain the URL of the PetAdoptions application by running:
```bash
aws ssm get-parameter --name '/petstore/petsiteurl'  | jq -r .Parameter.Value
```
Paste the URL into a web browser, and explore the example web application if you'd like. In this module,
we're going to focus just on this front end, so you don't need to go very deep right now. As you can see, there is a
web front end that is user facing.

### Application Architecture

Here is the PetAdoptions application architecture again. Let's focus on the ALB that is balancing the
**PetSite-FrontEnd service**:
![Image diagram of PetAdoptions Application Architecture with the PetSite-FrontEnd ALB and TargetGroup highlighted](/images/PetAdoptions_architecture_ALB_TG.png)

### Quick Refresher on ALBs
An Application Load Balancer is a Layer 7 load balancer that has rich functionalty to route traffic in various
configurations. The "front end" of the load balancer (facing the consumers of the services) is shared across multiple
"back ends" accessing the services, which are called TargetGroups. In the PetAdoptions architecture we see that the ALB
nearest the users is balancing traffic to the PetSite-FrontEnd service and also a separate PetAdoptionsHistory-API service. For now we want to focus
just on the PetSite-FrontEnd service, or rather on its TargetGroup.

### Finding this TargetGroup in the AWS Console
- Go to the Compute > EC2 section of the AWS Console
- Click on TargetGroups on the left side under Load Balancing
![TargetGroups location in left sidebar](/images/TargetGroups.png)
- We can recognize the TargetGroup we want from its name, which will start with `Servic-PetSi-`
![Example of a TargetGroup whose name starts with Service-PetSi-](/images/Servic-PetSi_TargetGroup.png)


When working to set SLOs on your own applications, it helps to know some of the details of the application architecture,
or to work with someone who knows it well, such as a lead developer or site reliability engineer who is familiar with
the specific application.

**Click on the TargetGroup with the name starting with `Servic-PetSi-`**