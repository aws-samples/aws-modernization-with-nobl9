---
title: "Install EKG" # MODIFY THIS TITLE
chapter: true
weight: 3 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Install EKG

### Clone the EKG repo locally
For this workshop, we'll use a specific branch that is preconfigured to run within the One Observability PetSite cluster.
```bash
git clone https://github.com/nobl9/ekg.git
cd ekg
git checkout aws-workshop
```

Next, we need to make sure that we are logged into the cluster, using the config name `PetSite`:
```bash
aws eks update-kubeconfig --name PetSite --region $AWS_REGION --alias PetSite
```


If you are working in Cloud9, you can navigate to Source Control panel on the left and click **Clone Repository** and enter above URL and select top directory as location:
![Cloud9 EKG Git Repo](/images/nobl9-select-ekg-repo.png)

![Cloud9 EKG Git Folder](/images/nobl9-select-ekg-folder.png)

![Cloud9 EKG Structure](/images/nobl9-ekg-structure.png)

Make sure to cd to top folder and navigate to ekg folder in the terminal as well.

### Configure EKG
Let's create the tfvars file from this template:
```bash
cp terraform.tfvars.example terraform.tfvars
```

Then edit terraform.tfvars with your editor of choice, filing out each field:
- The AWS region (whatever region you are in)
- The EKS cluster name should be `PetSite`
- You can copy your Nobl9 Organization ID from the Settings screen in Nobl9 (bottom of left sidebar)

Now you need to create Nobl9 access keys and set some environment variable.
- Go to Settings > [Access Keys](https://app.nobl9.com/settings/keys)
- Create an access key
  - Description: `terraform`
  - Don't close this window yet
- Set these environment variables in CloudShell:
```bash
export TF_VAR_nobl9_client_id="<your Nobl9 Client ID>"
export TF_VAR_nobl9_client_secret="<your Nobl9 Client Secret>"
```

### Install EKG
```bash
terraform init
terraform apply
```

Now you can navigate to Dashboards on the left panel and find EKG connected to your Nobl9 account for PetSite cluster:

![EKG Service in Nobl9 UI](/images/nobl9-ekg.png)