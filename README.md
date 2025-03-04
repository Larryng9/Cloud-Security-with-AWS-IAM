![PSG (1) copy (67)](https://github.com/user-attachments/assets/67d6bfb2-eea5-449f-87dd-537e8c596609)

## Project Objective:
### Creating an IAM Users and User Groups, deployed EC2 Instances and IAM policies.

* EC2 instances

* IAM Policies

* IAM Users and User Groups

* AWS Account Alias

<img width="645" alt="architecture" src="https://github.com/user-attachments/assets/034bd3d1-7e14-415e-aa6e-be2594dc78aa" />

  # STEP 1
## Launch EC2 Instances

Welcome to the team! You've just joined our dynamic team as a DevOps engineer, and we're thrilled to have you on board.

As we gear up for the upcoming holiday season, we need to:

1. **Boost our computing power** to match increased traffic to the website. Lots of new students want to learn with NextWork over the break!
2. Onboard an intern working here - they should have the **right permission settings** to contribute while keeping the company's resources secure.

Let's start with the first task and **boost computing power** by launching some EC2 instances.

  **In this step, get ready to:**

  * Launch two Amazon EC2 instances.
  * Log in to your AWS Management Console.
  * Head to **EC2.**

![image](https://github.com/user-attachments/assets/46b35ba5-ad71-45c8-a312-ecf53fe327fe)

  * Switch your **Region** to the one closest to you!

![image](https://github.com/user-attachments/assets/882debb0-a7f8-4058-bd42-691e395c7095)

  * In your EC2 console, choose Launch instances.
  * Let's set up your EC2 instance!
  * In Name, enter the value nextwork-production-yourname. Yup, replace yourname with your name.
  * Choose **Add additional tags,** which is right next to your Name field.

![image](https://github.com/user-attachments/assets/4bdaf847-da61-4ae4-9bf9-902dd3de1f2a)

  * Choose Add new tag.
  * For the next tag, use this information:
    * Key: Environment
    * Value: production

![image](https://github.com/user-attachments/assets/ce01923a-bb66-4ae0-9c5d-3c95a8eb12dc)

  * Head on down to see your EC2 settings and make sure the Amazon Machine Image (AMI) is using a Free tier eligible option.

![image](https://github.com/user-attachments/assets/70e1c856-13dc-4bb5-8688-a73b9f502cc9)

  * For the instance type, also make sure you're using a Free tier eligible option!

![image](https://github.com/user-attachments/assets/68128ba1-067f-4473-87ed-98e626252255)

  * For Key pair (login), select Proceed without a key pair.

![image](https://github.com/user-attachments/assets/b6095911-e09b-4abc-a8ab-2cd112190f4a)

  * You're ready! Click Launch instance.

![image](https://github.com/user-attachments/assets/30b633a0-200d-4b49-a3dd-00f183a148ab)

![image](https://github.com/user-attachments/assets/e55a6246-7925-423f-abb4-cd783846a35e)

  *  Looks like a success!

![image](https://github.com/user-attachments/assets/2b35d233-217e-4efb-9e33-46c51e10239b)

  * Now let's create one more EC2 instance for the development environment.

  * Repeat the same flow, but this time using these tags:
    
* Name: Larry-Development
* Environment: Development

![Capture](https://github.com/user-attachments/assets/c7070705-cebf-4d5b-8ebf-5a5d258c22bb)

* Launch your second instance.
* Select Instances from your left hand navigation panel.
* If you only see one instance on your page, make sure to use that refresh button!

![image](https://github.com/user-attachments/assets/88e337ad-7d31-4939-8496-fb5ca28279ac)

* Let's have a look at your wonderful work.
* Select the checkbox next to one of your instances, and a popup window of information pops up!
* Select the Tags tab.

![image](https://github.com/user-attachments/assets/e9ae8b63-251f-4b77-baf3-2ad4c42ef1ee)

Voila - you'll see the tags you've defined right here.

![image](https://github.com/user-attachments/assets/d831620c-eb5e-4089-951c-5f96cec109e4)

  # STEP 2
## Create an IAM Policy

I've deployed two EC2 instances, one for your production environment and one for your development environment.

Now let's move into our second task as engineer - it's time to onboard the team's new intern and set up permission policies.
Our intern should have permission to the development EC2 instance but not the production instance. We don't want them to accidentally shut down the platform or push their changes to the production environment while they're just testing things!

To start this task, we'll use AWS IAM to give our intern access to the development instance first.

**In this step, get ready to:**
  * Create an IAM policy that gives access to the development instance.
  * Head to your **IAM** console.

![image](https://github.com/user-attachments/assets/1baaa13d-4447-4f73-97c9-79bd540f6b11)

  * Now on the left-hand navigation panel of your IAM console, choose Policies.
  * Choose Create policy.
  * Switch your Policy editor tab to JSON.

![image](https://github.com/user-attachments/assets/04b49108-2e77-4b27-8146-2f2b48e8e8ed)

  * Here's the policy I'll be using!

![Capture1](https://github.com/user-attachments/assets/86fea9d8-875d-4285-a7aa-988612382a10)

  * Select Next when you're ready.
  * Fill in your policy's details:
    * Name: LarryDevEnvironmentPolicy
    * Description: IAM Policy for NextWork's development environment.
  * Choose Create policy.
  * Oh no! Turns out there's a rule for the characters allowed in your Policy description. Edit this description to get rid of that error (can you tell which character is not valid? There's a hint given to you right underneath the Description's text box).
  * Choose Create policy again when you're done.

![image](https://github.com/user-attachments/assets/56d91aa5-ca74-408f-9ea5-66db1aac9472)

# STEP 3
## Create an AWS Account Alias

Alrighty, that was the permission policy all set up

Now that we can give our intern access to the development instance, the intern can't wait to start. They'd love to jump into the team's AWS account right away!

Sounds great... where should they go to log in?


**In this step, get ready to:**

  * Make it easier for users to log into your AWS account, using an Account Alias.
    
  * Head to your IAM dashboard.

  * In the right-hand side of the dashboard, choose Create under Account Alias.

![image](https://github.com/user-attachments/assets/9ff92fd5-89f1-4899-987f-de74ba0f89c9)

  * In the Preferred alias field, enter alias-larry. Yup, replace yourname with your name!
    
![Capture2](https://github.com/user-attachments/assets/0482dcb6-f9f5-4bd9-9c78-79e41bd6d7d8)

  * Choose Create alias.

# STEP 4
## Create IAM Users and User Groups










