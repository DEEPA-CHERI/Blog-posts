---
title: "Managing Multiple AWS Accounts from the Command Line"
date: 2023-06-25T20:21:52+05:30 
draft: true
---

Introduction:
Handling multiple AWS accounts from the command line is essential for developers, people working on various projects. you might find it challenging to switch between them efficiently. Fortunately, AWS provides a simple and powerful way to manage different AWS profiles from the command line.

Step 1: AWS CLI Installation
Before you start, make sure you have the AWS Command Line Interface (CLI) installed. You can download and install it from the official AWS website.

Step 2: AWS Configuration
Now, let's configure AWS CLI for multiple profiles. Open your terminal and run the following command:

aws configure --profile profile_name
Replace "profile_name" with a name for your new profile. This command will prompt you to enter the Access Key ID, Secret Access Key, default region, and output format. You can repeat this step for each AWS account you want to manage.

Step 3: Switching Between Profiles
To switch between profiles when using the AWS CLI, you can use the --profile flag. For example, to use a specific profile, you can run a command like this:


aws s3 ls --profile profile_name
This command will execute the AWS S3 list command using the specified profile.

Step 4: Default Profile
If you want to set a default profile that the AWS CLI will use if you don't specify a profile explicitly, you can use the following command:


aws configure set default.profile profile_name
Step 5: Verifying Profiles
To verify the profiles you've configured, you can use the list-profiles command:


aws configure list-profiles
This will display a list of all the configured profiles.

Conclusion
Managing multiple AWS accounts from the command line is made easy by creating and switching between profiles. With this approach, you can work with different AWS accounts seamlessly, ensuring you're using the correct credentials and configurations for each specific account. It's a practical solution for developers and administrators who need to interact with multiple AWS environments.
