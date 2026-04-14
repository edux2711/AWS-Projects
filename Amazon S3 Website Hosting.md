
# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Eduardo Gonzalez  
**Email:** edux2711@gmail.com

---

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use S3 to host a static website. I'm doing this project to learn about AWS and cloud services and how they can be to store objects in the cloud and host websites.

### Tools and concepts

Services I used were S3 and bucket policies. Key concepts I learnt include static website hosting and policy management.

### Time, challenges, and wins

This project took me approximately 1.5 hours. 

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open Amazon S3 and create storage space to store the website files. 

### How long it took to create the bucket

Creating an S3 bucket took me a few minutes.

### Region selection

The Region I picked for my S3 bucket was N. Virginia, because it is the closest region available, which helps to reduce costs and improve speed.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means that no other AWS account in the world can use the same bucket name.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload files inside the bucket to create the website.

### Files I uploaded

I uploaded two files to my S3 bucket: an index.html file and a folder containing images.

### How the files work together

Both files are necessary for this project: index.html defines the structure, and the folder contains content to populate the website.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure the S3 bucket for static website hosting to make the site available on the internet.

### Understanding website hosting

Website hosting allows websites to be visible on the internet by anyone by storing HTML files on a web server.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I enabled the static website hosting property inside the S3 bucket settings.

### Access Control Lists (ACLs)

An ACL is a way to configure permission settings inside a bucket.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is an URL that directs users to the hosted website.

### What I saw when I tested the endpoint

When I first accessed the bucket endpoint URL, I received a 403 Forbidden error. The reason for this error was that objects in a bucket are public by default but the files are still private.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make the website files in S3 publicly accessible to allow anyone to view the content in the files.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I made the files inside the bucket publicly accessible.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to set up a bucket policy to prevent people from deleting the index.html file.

### Understanding bucket policies

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy prevents me from deleting the index.html file inside the S3 bucket.

---

---
