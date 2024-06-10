---
title: "Create IAM Role" # MODIFY THIS TITLE
chapter: true
weight: 2 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Connecting Nobl9 to CloudWatch

### Obtain Your Nobl9 Account ID and External ID
In the Nobl9 web application, open [Interations - Data Sources](https://app.nobl9.com/integrations/sources)
- Click the plus (+) button to add a data source
- Click on Amazon CloudWatch
- Click Direct
- Note the **Nobl9 AWS Account ID** and **External ID** fields

### Create the IAM Role

In another tab, open the AWS Console and go to [IAM](https://console.aws.amazon.com/iam/).
1. Choose Roles on the navigation pane
2. Click Create Role
![Screenshots of creating a role](/images/iam-1-create-role.png)
3. Choose AWS account role
![Screenshots of creating a role](/images/iam-2-aws-account.png)
4. Choose Another AWS account. Paste the **Nobl9 AWS Account ID** from the Nobl9 web application here.
5. Select Require External ID. Paste the **External ID** from the Nobl9 web application here.
![Screenshots of creating a role](/images/iam-aws-account-ids.png)
6. Click Next
7. Attach the CloudWatchReadOnlyAccess permission for your account:
![Screenshots of creating a role](/images/iam-cloudwatch-readonly.png)
8. Click Next, name the role (e.g. Nobl9-CloudWatch-Data-Source) and save the role.
9. Copy the ARN of the newly created role.

### Create the Nobl9 Data Source
Back in the Nobl9 web application,
- Paste the ARN you copied from the IAM role.
- In the Project field, type "workshop"
- In the Display Name field, type "CloudWatch"
- Leave the other settings as they are, and click Add Data Source.

You are now ready to create an SLO on CloudWatch data.
