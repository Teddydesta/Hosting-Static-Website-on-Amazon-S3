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

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/dc972754-af12-4ee0-98ad-6454155812c4)

Head to the bottom of the page and click "Save Changes." As you scroll down the updated page, what catches your eye?

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/6a8571ce-783c-4753-8621-10151dd2bf82)

After successfully enabling static website hosting, a bucket endpoint has been created for testing. You're now ready to proceed.

### Step 3: Add a Bucket Policy that Makes an S3 Bucket Content Publicly Available

Scroll down to Bucket policy and click "Edit" to create a policy to allow public reads.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/65dbe7b3-f2cf-40eb-a5aa-d7c6f78799cd)

We use the Policy Generator to create a bucket policy. Click "policy generator".

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/54a741a5-29b3-4b95-8994-37b6d02851f6)

In the "Policy type" section, choose "S3 Bucket Policy." To grant access to everyone, use the wildcard (*) for Principal. Scroll down to locate "GetObject" under actions, and check the box to authorize users to read objects in the bucket.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/c04f46ab-ccc2-4706-97a6-39272ae6a8a4)

Next, specify the resource name, which will be the Amazon Resource Name (ARN) of the bucket. Return to the "Edit policy" window and copy the ARN as illustrated below.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/3388d15b-8aec-4e64-a0a7-ffc3eb1cd9d6)

Paste the copied ARN into the ARN field and append "/*" to signify it's valid for all objects in the bucket. This configuration allows reading all objects in the bucket. Click "Add Statement" below to apply the changes.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/578c44a1-19ac-4f07-a181-5bcb0cbf6dac)

Click "Generate Policy," then copy the generated JSON policy.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/2412fa7a-ff6c-49ee-89be-d3c229ef5d31)

Paste it into the "Edit Policy" window and click "Save Changes" below.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/0e382407-19af-4bf5-bb6e-737ac9b1d0ca)

### Step 4: Upload Website Files

Next, we need to upload the files for the website to our bucket. We use the following website files in this demo: A webpage(index.html) and other images.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/fba7ffc9-d1ae-463c-bba9-a3f3ffcb9ec6)

Now, proceed to upload the three files to your bucket. Navigate to the "Objects" tab and click on "Upload."

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/c2b4ea69-735e-4881-8255-7b1880f6411f)

After the files are uploaded to bucket from your local machine file explorer, Click "Upload" at the bottom and all the files will be uploaded. We now have the files in our bucket.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/8d7282e4-7172-4e7f-b55f-390b9599805a)

### Step 5: Test and Validate Your Website

To get your bucket endpoint, choose the Properties tab and scroll down to the Static website hosting section at the end of the page. Click on it to open your static website on a new tab.

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/5a3c2d7a-e737-4771-80e5-46749eec554c)

After uploading the files, copy the URL and paste it into your preferred web browser. Upon doing so, the home page (index) should be displayed as follows:

![image](https://github.com/Teddydesta/S3-bucket/assets/86881100/cfd22de1-d9e3-49e2-88e8-77c36ffce35a)

### Conclusion
Bravo on mastering this comprehensive tutorial! To dive deeper into the world of Amazon S3, embark on further exploration [here](https://www.google.com/search?client=firefox-b-d&q=amazon+s3). Your dedication is worthy of applause! Don't miss the opportunity to give that Clap button a try, and ponder following for a treasure trove of insightful articles. Until our next rendezvous! 🚀👏











