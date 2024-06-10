---
title: "Other TargetGroup SLOs" # MODIFY THIS TITLE
chapter: true
weight: 3 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Other types of SLOs
Now that you've created an SLO on an ALB TargetGroup, consider some similar SLOs you can create using similar data.

### Error Rate
Create a Ratio SLO on the error rate of your TargetGroup, based on HTTP status codes
- Good count
  - Metric Name: **HTTPCode_Target_2XX_Count**
  - Statistic Function: **Sum**
- Total count
  - Metric Name: **RequestCount**
  - Statistic Function: **Sum**

### Availability
A Threshold SLO tracking whether a sufficient number of service instances are staying up and passing health checks. Can
catch and measure the impact of brief outages that may occur during planned or unplanned restarts, such as during
releases or incident response actions.
- Metric Name: **HealthyHostCount**
- Statistic Function: **Minimum**

### Reachability / Traffic
Threshold SLO making sure that each instance of a service is receiving a minimum amount of traffic. A gap may indicate
that traffic has stopped reaching a given instance -- or the entire group.
- Metric Name: **RequestCountPerTarget**
- Statistic Function: **Minimum**
