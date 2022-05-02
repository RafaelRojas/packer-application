# Application Golden Image repo for Big project

This repo creates an application AWS AMI that installs a microblog in Flask (python3) on an ec2 instance of Ubuntu 20.04.2 LTS base AMI.


This project uses GitHub Actions (GHA) to build an AMI on AWS us-east-2 using packer, AWS secret manager, AWS IAM special roles and api keys. The resulting AMI is dynamically used on Terraform code (using terraform cloud) to build/rebuild an ASG.


This project is not production ready and it's use is just for teaching and learning purposes. 


Works:

* Build pipeline. AMI builds.
* Secrets. Keys are well kept.
* Teffarom plan on TFCloud is triggered.

TODO:

* TFCloud plan/build is hacky, sometines it triggers planning, sometimes won't.
* A lot of *best practices* are missing in the AMI build. A better structure is possible.
* Proper secret rotation.
* Ading a dependency or security scanning tool for vulnerability alert/auto-build. 
