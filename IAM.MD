##  IAM - AWS

Introduces you to AWS Identity and Access Management, helps you set up users and groups, and shows you how to protect your resources with access control policies. Also shows how to connect to other identity services to grant external users access to your AWS resources.

## Creating IAM users (console)

1. Sign in to the AWS Management Console and open the IAM console at https://console.aws.amazon.com/iam/.

2. choose Users and then choose Add users

3. Type the user name for the new user. This is the sign-in name for AWS. If you want to add multiple users, choose Add another user for each additional user and type their user names. You can add upto 10 users at one time.

4. Select the type of access this set of users will have. You can select programmatic access, access to the AWS Management Console, or both.

• Select Programmatic access if the users require access to the API, AWS CLI, or Tools for WindowsPowerShell. This creates an access key for each new user. You can view or download the accesskeys when you get to the Final page.

• Select AWS Management Console access if the users require access to the AWS ManagementConsole. This creates a password for each new user Choose Next: Permissions.

5. On the Set permissions page, specify how you want to assign permissions to this set of new users.

6.Choose one of the following three options:

• Add user to group. Choose this option if you want to assign the users to one or more groups that already have permissions policies. IAM displays a list of the groups in your account, along with their attached policies. You can select one or more existing groups, or choose Create group tocreate a new group. 

• Copy permissions from existing user. Choose this option to copy all of the group memberships,attached managed policies, embedded inline policies, and any existing permissions boundaries  from an existing user to the new users. IAM displays a list of the users in your account. Select the one whose permissions most closely match the needs of your new users.

• Attach existing policies directly. Choose this option to see a list of the AWS managed andcustomer managed policies in your account. Select the policies that you want to attach to the new users or choose Create policy to open a new browser tab and create a new policy from scratch.

7. Choose Next: Tags.

8. (Optional) Set a permissions boundary.

9.(Optional) Add metadata to the user by attaching tags as key-value pairs. For more informationabout using tags in IAM, see Tagging IAM resources

10. Choose Next: Review to see all of the choices you made up to this point. When you are ready toproceed, choose Create user.

11. To view the users' access keys (access key IDs and secret access keys), choose Show next to each password and access key that you want to see. To save the access keys, choose Download .csv and then save the file to a safe location .After you create the policy, close that tab and return to your original tab to add the policy to the new user.

CREATING IAM Roles
 
 Step 1 Select trusted entity

 Step 2 Add permissions that are to be assinged for the particulars 

 Step 3 Name, review, and create

## What is an IAM Role?

An IAM role is an IAM identity that you can create in your AWS account and assign specific permissions.

An IAM role is similar to an IAM because it is an IAM identity that has specific permissions associated with it. These permissions determine what the identity can and cannot do.

However, one significant difference between an IAM role and an IAM user is that a role is assumable by anyone who needs it. A role does not have standard long-term credentials (like passwords) associated with it. AWS generates temporary security credentials when an IAM role is assumed.

## What is an IAM Policy?
An IAM policy is a document with a set of rules. Each IAM policy grants a specific set of permissions.

Policies are attached to IAM identities like Users, Groups, and Roles. Each IAM policy has a unique name.

There are two types of policies in your AWS account:

Managed policies: These policies can be reused and attached to multiple entities. AWS provides a lot of managed policies by default. Customers can also create their own managed policies.

Inline policies: These policies are applied directly to IAM entities. However, these policies are not reusable and cannot be attached to multiple entities.
