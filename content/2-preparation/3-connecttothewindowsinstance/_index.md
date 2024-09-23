+++
title = "Connect to the Windows Instance"
date = "`r Sys.Date()`"
weight = 3
chapter = false
pre = "<b>2.3. </b>"
+++

#### Connect to the Windows Instance
1. Go to [Amazon EC2 console](https://console.aws.amazon.com/ec2/).
On the left navigation bar, click **Intances**.
Select **DevAxWindowsHost**.
Click **Connect**.



2. In the **Connect to instance** page
- Click tab **RDP client**.
- Click **Download remote desktop file.** We will download file remote desktop to the folder contains the key pair.
- Click **Get password**.



3. In the **Get Windows password** page:
- Click **Browse**.
- Select file **KPforDevAxInstances.pem** we downloaded in the section 1.1.
- Click **Decrypt Password** to decrypt the password.



4. Copy decrypted password .


5. Open file **DevAxWindowsHost.rdp** we downloaded in the step 2.
- Click **Connect**.

6. Type the password we copied in the step 4
- Click **OK**.



7. Click **Don’t ask me again for connections to this computer.**
- Click **Yes**.

8. Connect successfully.

#### Configure AWS CLI
1. Assign the Administrator Access to user **awsstudent** was created by Cloud Formation template
- Go to [AWS IAM Console](https://console.aws.amazon.com/iamv2/).
- Click **Users**.
- Click user **awsstudent**

2. In the **Permissions policies** section
- Click **Add permissions**

3. In the **Add permissions to awsstudent** page
- Click **Attach existing policies directly**
- Type `AdministratorAccess` to the search bar.
- Select **AdministratorAccess**
- Click **Next:Review**



4. Click **Add Permission**



5. Click tab **Security credentials**
- Click **Create access key** to create the access key


6. Click **Download .csv file** to save **Access key** and **Secret access key** to use in the next steps

7. Execute the below command:
```
aws configure set profile.devaxacademy.region <your_region>
aws configure set profile.devaxacademy.aws_access_key_id <access_key_id>
aws configure set profile.devaxacademy.aws_secret_access_key <secret_access_key>
```
{{% notice note %}}
Change **<your_region>** by **Region code**
Change **<access_key_id>** by **Access Key Id** we saved in the step 6
Change **<secret_access_key>** by **Secret Access Key** we saved in the step 6
{{% /notice %}}
