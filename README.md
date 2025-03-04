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

![image](https://github.com/user-attachments/assets/13becb6c-4d18-4fa5-949d-4da3e36efef7)

  * In your EC2 console, choose Launch instances.
  * Let's set up your EC2 instance!
  * In Name, enter the value **Larry-Production**. Yup, replace yourname with your name.
  * Choose **Add additional tags,** which is right next to your Name field.

![image](https://github.com/user-attachments/assets/a6ac337d-ab48-49c0-8fe3-cc41436ea74b)

  * Choose Add new tag.
  * For the next tag, use this information:
    * Key: Environment
    * Value: production

![image](https://github.com/user-attachments/assets/a1b2e124-fb7d-4666-be6b-afc6903cdc2c)

  * Head on down to see your EC2 settings and make sure the Amazon Machine Image (AMI) is using a Free tier eligible option.

![image](https://github.com/user-attachments/assets/70e1c856-13dc-4bb5-8688-a73b9f502cc9)

  * For the instance type, also make sure you're using a Free tier eligible option!

![image](https://github.com/user-attachments/assets/68128ba1-067f-4473-87ed-98e626252255)

  * For Key pair (login), select Proceed without a key pair.

![image](https://github.com/user-attachments/assets/b6095911-e09b-4abc-a8ab-2cd112190f4a)

  * You're ready! Click Launch instance.

![image](https://github.com/user-attachments/assets/6c03f067-a9bc-429a-9611-dbc50649b3e2)

![image](https://github.com/user-attachments/assets/a026561a-7308-4924-80b9-ae36f2e22db1)

  *  Looks like a success!

![image](https://github.com/user-attachments/assets/f83c6cc1-dbf9-43a5-9529-aad727dfd9eb)

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

Your account alias is looking slick! It should be a lot faster for users to find your account and log in now.

Our new intern doesn't actually have a way to log in to the team's AWS account yet... what should their username and password be?

You wouldn't want to just share your account details with them. After all, you have access to the production instance, which they shouldn't get access to.

Let's solve this problem using IAM again - this time we're using two other tools called groups and users.

**In this step, get ready to:**

Set up a dedicated IAM group for all NextWork interns, so you can manage all interns' permissions from one place.
Set up a dedicated IAM user for your new intern, so they have a way to log in.

  * Choose User groups in your left-hand navigation panel.
  * Choose Create group.
  * Let's create your first user group!

* To set up your user group:
  * Name: nextwork-dev-group
  * Attach permission policies: NextWorkDevEnvironmentPolicy

![image](https://github.com/user-attachments/assets/66294085-d427-4b10-b9ce-5cb83bb02f1f)

* Select Create user group. Success!

![image](https://github.com/user-attachments/assets/f3786a63-5bfa-4f94-bffb-a294e0c4ed7e)

* Choose Users from the left-hand navigation panel.
* Choose Create user.
* Let's set up this user! Under User name, enter nextwork-dev-yourname
* Tick the checkbox to Provide user access to the AWS Management Console.


* Uncheck the box for Users must create a new password at next sign-in - Recommended.

![image](https://github.com/user-attachments/assets/b89ccc91-0385-40e1-91e7-4183c6a7df06)

* Select Next when you're ready!
* To set permissions for your user, we'll simply add it to the user group you've created. Select the checkbox next to nextwork-dev-group.
* Select Next.
* Select Create user!
  
![Capture3](https://github.com/user-attachments/assets/1eec7862-dfac-4dcc-9ef9-ed32ca9bcaa5)

* It's a success - now you're seeing some specific sign-in details for your new user. Stay on this page.

![Capture4](https://github.com/user-attachments/assets/04c0d1cd-5fd4-4f09-a46b-20fd248bd807)

# STEP 5
## Test your intern's Access

The new intern is going to be stoked to receive their keys to the NextWork AWS account - well done 😎

Before we pass them their login details, let's test the interns' IAM User's access first. That way we can make sure that they have the right access to our development instance (and not the production instance).


In this step, get ready to:

*  Log into AWS using the intern's IAM user.
*  Test the intern's access to your production and development instance.



*  Copy the Console sign-in URL. Do not close this tab!
*  Open a new incognito window on your browser.
*  Open the new console sign-in URL in your incognito window.
*  aUsing the User name and Console password given in your IAM tab, let's log in!

![image](https://github.com/user-attachments/assets/bfe5da12-aea9-40c3-90f6-27f99f3bcb76)

*  As a new user, you'll notice that some of your dashboard panels are showing Access denied already.

![image](https://github.com/user-attachments/assets/8b4e46cb-d1f7-47b3-9f8a-ec88ccb5f699)

*  Head to your EC2 console, and make sure you're in the same Region as the one where you deployed your two production and development instances.
*  Head to Instances.
*  Select your production instance, and in the Actions dropdown, select Manage instance state.

![image](https://github.com/user-attachments/assets/ca93c72e-8a6a-4ab8-8b44-a61604fa947d)

*  Let's try to stop this instance. Select the Stop option, then Change state.

![image](https://github.com/user-attachments/assets/a6c69e35-8cc0-4dc3-87e1-21270a81b3d7)

*  Select Stop.

![Capture6](https://github.com/user-attachments/assets/9f0f735e-3629-4188-bf67-406a8aeaa605)

*  Now let's try to stop the development instance.
*  Head back to the Instances page, and select the checkbox next to nextwork-development-yourname.
*  Under the Actions drop-down, select Manage instance state.
*  Select Stop, then Change state. Select Stop.
*  Success!

![Capture7](https://github.com/user-attachments/assets/81d196f5-e1d6-4ac7-aae1-92d2a6e562c5)
