<h1>create-the-IAM-role-for-employee-directory-application</h1>

<h2>Description</h2>
we are going to create the IAM role for our employee directory application, and we will also look at how to create users and the different AWS access keys used for programmatic access to AWS APIs.

<br />

<h2>Program walk-through:</h2>

1. let's create the role by selecting Roles in the left-hand navigation of the IAM dashboard, then click Create role.
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741393074/Screenshot_2025-03-07_184411_vcbdhe.png"/>

<br />

2. Select AWS service, then we are going to select EC2 since our application will be running on EC2.
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741395214/Screenshot_2025-03-07_184531_jwvt6o.png"/>
<br />

3. On the page to Add permissions, we are going to use AWS-managed policies, select AmazonS3FullAccess and DynamoDB because we going to use it as the database for the application. (Give it a name)
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741395824/Screenshot_2025-03-07_184813_mxeitf.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741395854/Screenshot_2025-03-07_184826_crizxi.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741396080/Screenshot_2025-03-07_184958_jrsvh2.png"/>
<br />

4. Now let's create a user, click Add user and give a user name, In addition,  click the checkbox for Enabling console access. (what that means is I want to allow this user
to be able to sign in to the AWS management console, So note, by default, this was unchecked, meaning that just because you create a user doesn't mean they have access to the console).
 I'm going to allow an auto-generated password to be created, and then I want to leave the checkbox checked for users to create a password at the next sign-in.
Next step add the user to a group 
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741396472/Screenshot_2025-03-07_185322_g5pvuh.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741396939/Screenshot_2025-03-07_185350_hahd1q.png"/>
<br />

5.  I'm gonna go ahead and click Create group, and then what I wanna do is add a group name,  I'm gonna select the AmazonEC2FullAccess policy, then I'm gonna scroll down and click Create user group, We can see the permissions that this one user currently has. It will inherit the permissions from the EC2Admins group, and then it also has directly attached to itthe IAMUserChangePassword permission, which will allow these user to change their password. and now I can select this user group to add this user into,
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741397382/Screenshot_2025-03-07_185322_sy1mo2.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741397408/Screenshot_2025-03-07_185442_f6auzl.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741397435/Screenshot_2025-03-07_185509_jw6lcb.png"/>

6. We can see the permissions that this one user currently has. It will inherit the permissions from the EC2Admins group, and then it also has direct attached to it the IAMUserChangePassword permission,
which will allow this user to change their password, what I wanna do next is click on the Security Credentials tab, and if we scroll down, you can see that we have this panel here called Access keys.
Access keys are going to allow your user.
 I'm gonna go ahead and create an access key here, and then I wanna use this for the command line, and then I'm gonna go ahead and click the checkbox for "I understand the above recommendation." we have our access key here, and then we have our secret access key, which is not shown currently on this page, but you could click show and then copy it, and you would use this access key and secret access key
to be able to configure your command line locally.
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741397565/Screenshot_2025-03-07_185526_yo7bjr.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741397698/Screenshot_2025-03-07_185548_wlxge3.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741398175/Screenshot_2025-03-07_185743_nxrb0n.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741398201/Screenshot_2025-03-07_185747_sht9ug.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1741398223/Screenshot_2025-03-07_190016_sgsmm2.png"/>



