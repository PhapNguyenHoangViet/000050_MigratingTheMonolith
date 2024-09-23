+++
title = "Introduction"
date = "`r Sys.Date()`"
weight = 1
chapter = false
pre = "<b>1. </b>"
+++


### Overview

**Kubernetes (K8s)** is an open source, extensible platform for managing packaged applications and services, facilitating configuration and automating application deployment.

   - In this lab, we will create a simple **Kubernetes Cluster** on **AWS EKS (Elastic Kubernetes Service)**.
   - Then I will deploy the site on the cluster and use **AWS CodePipeLine** for automated deployment.

![CI_CDwithAWSCodePipeline](/images/1-introduction/CI_CDwithAWSCodePipeline.png?width=90pc)

### Content
  1. [Introduction](1-Introduction/)
  2. [Preparation steps](2-Preparation-steps/)
  3. [Create EKS cluster](3-Create-EKS-cluster/)
  4. [Generate Code Pipeline](4-Generate-Code-Pipeline/)
  5. [Resource Cleanup](5-Clean-up-resources/)