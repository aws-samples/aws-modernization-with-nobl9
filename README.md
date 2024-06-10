# AWS Modernization Workshop with Nobl9

## Description

In this workshop, we will walk you through how to set up AWS Observability for your application, and Service Level Objectives (SLOs) on your AWS infrastructure to provide a hands-on experience using AWS services and Nobl9’s SLO-based reliability platform to build reliability and observability into your AWS-hosted product.

 ## High level agenda

* Introduction
* Setup AWS Account and Nobl9
* Setup AWS infrastructure and deploy sample application on EKS
* AWS Observability
* What is SLO and why I should care
* SLO setup with Nobl9
* EKG - ready-to-install package for EKS users

 ## Types of Events
 
 - Self-paced
 - AWS hosted

 ### Learning Objectives

Building off of the One Observability Workshop, you will learn the basics of setting up SLO-based monitoring on a live PetAdoptions application consisting of multiple Application Load Balancers, Amazon EKS, Amazon SNS, Amazon SQS, Amazon S3, Amazon Aurora PostgreSQL, Amazon DynamoDB, and more. You will learn how to integrate SLOs into your application and tune them for user-facing reliability.

## Building the Website

This site is built with Hugo, so you'll need it [installed](https://gohugo.io/getting-started/quick-start/#step-1-install-hugo)

First, clone this repo:

```bash
git clone git@github.com:aws-samples/aws-modernization-with-nobl9.git
```

Ensure you've also cloned the submodules:

```bash
git submodule init
git submodule update
```

Then serve the website with Hugo:

```bash
hugo server
```

## Authors

Contributors names and contact info

* Alex Nauda (@alexnauda)
* Marina Novikova (@mariswa)  

## License

This project is licensed. See the LICENSE.md file for details

## Acknowledgments

* Markdown cheat sheet (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* Learn theme markdown (https://learn.netlify.app/en/cont/markdown/)
* Menu extras and shortcuts (https://learn.netlify.app/en/cont/menushortcuts/) 
* Using Font Awesome Emoji's to help your page pop (https://learn.netlify.app/en/cont/icons/)