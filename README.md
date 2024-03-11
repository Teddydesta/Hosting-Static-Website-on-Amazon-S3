### Elevate Your Web Presence: A Step-by-Step Guide to Hosting a Static Website on Amazon S3
![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/5c05186d-fd90-4963-af92-fb448b9c550b)

### Introduction
In today's world, a swift and cost-effective website is vital, be it for a blog, small business, or portfolio. Amazon Web Services (AWS) stands out, offering an excellent platform - Amazon S3 - for hosting static websites. This article walks you through deploying your website effortlessly on AWS S3, ensuring a fast, reliable, and scalable online presence. Whether you're a seasoned developer or just starting your web journey, this guide equips you with everything needed to launch your site seamlessly on AWS S3.
This tutorial guides you through hosting a static website on S3. Ideal for scenarios like data collection surveys, and local business websites where site updates are infrequent. Key steps:

- Create S3 Bucket
- Configure Bucket for Website Hosting
- Enable Public Access
- Upload HTML Files
- Test and Validate Your Website

**Prerequisites**

1. AWS Account:

- For a safer demo, create an AWS account [here](https://aws.amazon.com/), using an IAM user rather than the root account.

2.  Console Navigation:

-  Familiarity with navigating the AWS Management Console is helpful.

-  I'll supplement guidance with ample snapshots for your ease.

### Step 1: Creating an S3 Bucket

- I'll supplement guidance with ample snapshots for your ease.
- Log in to your AWS IAM user account

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/329d22ca-801b-41d1-a1a4-bd8131a88d67)
**Search for S3 in the console and select S3.**
![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/2795a86a-3ba0-46cd-bb70-120f8c1fee34)

Enter the bucket name and choose the region where you want the bucket to be located. ensuring the bucket name's uniqueness across all AWS accounts and regions.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/174a3632-f6c6-4209-b622-9ff43edd3b83)
After setting a name and selecting a region click on the "create bucket" button.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/5750628a-55e8-4b8b-98ff-0f0a233989d2)

Navigate down the page, and to allow public access to an S3 bucket, uncheck the "Block all public access" checkbox. A warning will appear below; confirm your choice by checking the checkbox to acknowledge the current settings and enable public access to the bucket.
![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/09e1c11c-71d9-401a-a244-c5a219a0e020)

### Step 2: Enable Static Website Hosting
Scroll down, uncheck "Block all public access" to lift Amazon S3's default public access restriction for the bucket. Confirm your choice by clicking the checkbox below, acknowledging the current settings and enabling public access to the bucket.
Keep the Hosting type as the default (Host a static website), and input the precise name for the Index document that will function as your static webpage file. Similarly, enter the exact name for the Error document if you wish to create a custom web page for 4XX class errors. Note that this section is case-sensitive, so ensure the names you provide are an exact match.
