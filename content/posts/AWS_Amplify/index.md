---
title: "Host your website with AWS Amplify"
date: 2025-09-07T08:06:25+06:00
description: First project of this page is barisaygun.net hosting on AWS
menu:
  sidebar:
    name: Static website on AWS
    identifier: AWS_Amplify
    weight: 10
tags: ["Basic", "Multi-lingual"]
categories: ["Basic"]
---


## Introduction

Hello World!
This is the first project document on my blog and the project is blog itself. This would be a short project relatively because implementation of the project is mostly simple and requirements are clear. 
I can’t include website creation processes or Hugo related parts because in best case I’m amateur on that field. I only want to share what was my requirements, why I choose to proceed with AWS Amplify and what could be the other solutions and what kind of struggles I face on the process. 

## Design Considerations
At the beginning, I needed a blog for myself to post my AWS projects and build a portfolio to support the community. My first consideration was choosing what tool to use for minimum to no coding. After researching my options I reach to conclusion that using Hugo framework and a ready to go theme would best suit for this need.  My other options were using Wordpress or Wix. To maintain simplicity and for only getting a static webpage I proceeded with Hugo. To get started with Hugo and the theme I picked you can check the links in the resources section. 


[Hugo link](https://gohugo.io/getting-started/quick-start/)

[Toha theme link](https://github.com/hugo-toha/toha)

After creating my page on my local device, I created a GitHub account and push everything to this repository. Now only steps remaining is the domain name and hosting options. For domain name you can use any of the domain registrar and I suggest to check some of them to get best price. If you can catch a sale you can get a domain name with better price from standard prices. 

Now for hosting part, my requirements are: 
- No coding needed
- Deployment pipeline without manual intervention
- Reliable, scalable and cheaper option is more preferable
- Serverless

My design considerations with each option as follows: 

## Using a hosting service provider
Prices vary depending on the features you get, specifications of the server or which services you get. 
There is local and global providers which provides different services with different prices. But picking a reliable one is important for not getting any shortages or getting affected by server incidents etc. 
I don’t consider this option because I would like to proceed with AWS services. Which is much more scalable, much more easier to use (for me) and having the biggest provider in the world. 

## AWS Cloudfront + S3
At first I considered using S3 static website hosting with Cloudfront to get scalable, reliable and cheapest price. It could be tricky on the implementation but I’m confident on that part. The reason to not proceed with this option is the struggle to create a deployment pipeline without manual intervention. For every change and implementation on the page I need to do manual operation or using a middleware (which requires coding). So this option is not meet with my no coding requirement.  

## AWS Application LB + ASG + EC2
This is the most classic and flexible option. It’s flexible because you are managing the server. You can create an AMI to meet with your needs and using Auto Scaling Group and Loadbalancer in front of it you get scalable, reliable and flexible infrastructure. It’s not serverless and creating a deployment pipeline will need extra steps. On the cost side it won’t be the cheapest option too. So for this option if you need some certain needs on serverside it is the best practice. But in my case it’s not the best option. 

## AWS Amplify
Amplify offers ready to use pipeline for web applications with GitHub and using Cloudfront under the hood for better performance. It’s serverless, scalable, reliable and easy to use. Most of the operations are automated and after a few clicks your project is on the live. After these circumstances I choose to proceed with AWS Amplify. 



## Implementation
I faced some issues on the implementation with Hugo but following related Hugo document solved the issue on AWS Amplify and this blog gone live in couple of minutes. Issues were caused by nom and Hugo extended version installments. I followed this document and it solves the issues. Changes I made on GitHub is automatically deployed on the live website. Other than amplify.yml file I don’t have much notes on the implementation. It’s just selecting your source and following through. 

## Resources

[Hugo Getting Started](https://gohugo.io/getting-started/quick-start/)

[Toha theme GitHub](https://github.com/hugo-toha/toha)

[AWS Amplify Main Page](https://aws.amazon.com/amplify/)

[Hugo Page for amplify.yml](https://gohugo.io/host-and-deploy/host-on-aws-amplify/)


