
# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Eduardo Gonzalez  
**Email:** edux2711@gmail.com

---

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use AWS IAM to control who is authenticated and authorized in an AWS account. I'm doing this project to learn by launching an EC2 instance, then controlling who has access to it by creating some IAM policies and user groups. 

### Tools and concepts

Services I used were EC2 and IAM. Key concepts I learnt include policy management and resource management.

### Project reflection

This project took me approximately an hour. 

---

## Tags

### What I did in this step

In this step, I will launch two EC2 instances to increase computing power.

### Understanding tags

Tags are like labels you can attach to AWS resources for organization. They help organize resources and can be used to filter resources when you need to find them.

### My tag configuration

The tag I’ve used on my EC2 instances is called Env. The values I’ve assigned for my instances are production and development.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy for other users to only have access to the development instance, to prevent accidental changes to the production instance.

### Understanding IAM policies

IAM Policies are rules for who can do what with AWS resources.

### The policy I set up

For this project, I’ve set up a policy using JSON.

### Policy effect

I’ve created a policy that allows starting, stopping, and describing EC2 instances with the development tag. And also denies the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource

In JSON, Effect gives the option to allow or deny an action, Action gives the option to list a number of actions, and Resource attributes of a JSON policy specify which resources the policy applies to.

---

## My JSON Policy

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will simplify user login by using an Account Alias.

### Understanding account aliases

An account alias is a user friendly name for AWS accounts that can be replaced for the account ID.

### Setting up my account alias

Creating an account alias took me a minute. Now, my new AWS console sign-in URL is https://nextwork-alias-eduardo.signin.aws.amazon.com/console 

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will set up a dedicated IAM group for other users so that I can manage everyone's permissions from one place. I will also set up a dedicated IAM user for a new user so they have a way to log in.

### Understanding user groups

IAM user groups are collections of users that allow you to easily manage policies.

### Attaching policies to user groups

I attached the policy I created to this user group, which means that all users inside the group will also have the policy.

### Understanding IAM users

IAM users are entities who can be granted tailored credentials to an AWS account.

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is to send them an email with instructions. The second way is to share with them an .csv file with the information.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that some of the dashboard panels were showing Access denied. 

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will log into the account using the new user's credentials because I want to test the new user's access to the production and development instance.

### Testing policy actions

I tested my JSON IAM policy by trying to delete both instances.

### Stopping the production instance

When I tried to stop the production instance, I received an error. This was because the user does not have permission to delete this instance.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

When I tried to stop the development instance, I received an error that did not allow me to stop the instance. This was because the policy set up earlier.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to use the Policy Simulator to validate policies without affecting the AWS resources. I'm doing this because stopping instances can be disruptive to other developers, and it takes extra time to complete.

### Understanding the IAM Policy Simulator

### How I used the simulator

---

---
