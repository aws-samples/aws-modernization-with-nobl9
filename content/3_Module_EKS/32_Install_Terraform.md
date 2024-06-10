---
title: "Install Terraform" # MODIFY THIS TITLE
chapter: true
weight: 2 # MODIFY THIS VALUE TO REFLECT THE ORDERING OF THE MODULES IF APPLICABLE
---

## Install Terraform in CloudShell

### Let's use tfenv
One easy way to install Terraform is using tfenv, a version manager for Terraform.

```bash
git clone https://github.com/tfutils/tfenv.git ~/.tfenv
```

We can take advantage of the fact that `/home/cloudshell-user/bin` is already in the PATH by default in CloudShell:

```bash
mkdir ~/bin
ln -s ~/.tfenv/bin/* ~/bin/
```

```bash
tfenv install 1.5.7
tfenv use 1.5.7
```

That should set you up with a working terraform. Test it with:
```bash
terraform --version
```