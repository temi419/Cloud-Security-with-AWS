<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** David Adeleye  
**Email:** davidadley58@gmail.com

---

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

In this project, I will demonstrate how AWS can be used to give an intern limited access to the dev teams systen. I'm doing this project to learn the basics of AWS and get comfortable with it 

### Tools and concepts

Services I used were verr helpful in learning the basics of AWS origin and its functions. The concepts I learnt include how IAM and EC2 operate for JSON policies, user/usergroups, and instances. 

### Project reflection

This project took me approximately 3 hours The most challenging part was trying to figure out why the StopInstance function kept saying denied for the intern. It was most rewarding to figure out what i did wrong which was a problem within the code. 

---

## Tags

 tags in AWS are basically just labels you attach to your resources (like EC2 instances, S3 buckets, IAM users, etc.) to help you organize and control them.



The tag I’ve used on my EC2 instances is called Env. The value I’ve assigned for my instances are development.










![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

 IAM (Identity and Access Management) Policies in AWS are used to control who can do what to which resources.

### The policy I set up

I set up the policy using JSON. It gave me more control over the exact permissions, conditions, and tags — especially for setting rules like only allowing actions on EC2 instances with a specific tag (Env=development).

The effect of my policy is to allow all EC2 actions, but only on instances that are tagged with Env=development. It also allows read-only access to all EC2 resources through ec2:Describe*. 

### When creating a JSON policy, you have to define its Effect, Action and Resource.

In a JSON IAM policy, Effect defines whether the action is allowed or denied. Action tells what operation is being requested, like starting an EC2 instance. Resource specifies which AWS resource the action applies to.










---

## My JSON Policy

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_1c864649)

---

## Account Alias

An account alias is a friendly name for your account login

Creating an account alias took me 30 seconfs Now, my new AWS console sign-in URL is nextwork-temi

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### Users

An IAM user is a single identity created in your AWS account that represents a real person (like you) or an application/service that needs to interact with AWS.

### User Groups

An IAM User Group is just a container for users that lets you assign permissions in bulk.

I attached the policy I created to this user group, which means attaching a policy to a user group gives all users in that group the permissions in the policy.

---

## Logging in as an IAM User

The first way is email credentials second is CSV file 

Once I logged in as my IAM user, I noticed access was denied This was because of the policies

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

I tested my JSON IAM policy by going int ingognito mode and logging into the interns account and testing out the functions 

### Stopping the production instance

When I tried to stop the production instance it denied me This was because of the policies 

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_0e7a9d6a)

---

## Testing IAM Policies

### Stopping the development instance

Next, when I tried to stop the development instance it stopped This was because I had the policy permissions to do so although it is a lot of power

![Image](http://learn.nextwork.org/eager_green_serene_nutmeg/uploads/aws-security-iam_1811801c)

---

## The IAM Policy Simulator

### How I used the simulator

---

---
