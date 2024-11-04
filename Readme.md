# Hosting a Website on AWS with EC2, Apache2, and PuTTY

**Step 1: Launch a Linux EC2 Instance (Ubuntu)**
Login to AWS Console:

Go to AWS Console and log in.
Launch EC2 Instance:

Navigate to EC2 and click Launch Instance.
Choose an AMI (Amazon Machine Image):

Select Ubuntu Server
Choose Instance Type:

Pick t2.micro
Configure Security Group:

Create a security group with the following inbound rules:
SSH (port 22)
HTTP (port 80)
Key Pair:

Create a new key pair and download the .ppk file.
Launch the Instance.
<br>
**Step 2:** Connect to EC2 Using PuTTY
Open PuTTY.

Enter the Public IP of EC2:

In Host Name (or IP address), enter your instance's public IP.
Example: eg. (13.45.589.25)
Load PPK File:

In the left sidebar, navigate to Connection > SSH > Auth.
Click Browse and select the .ppk file.
Open the Connection:

Click Open and use ubuntu as the username when prompted.
**Step 3: Install Apache2 on the EC2 Instance**
Update the package list and install Apache2:

sudo apt update
sudo apt install apache2 -y
**Step 4: Delete Default index.html and Create a New One**
Navigate to the Apache directory: cd /var/www/html
Delete the default index.html: sudo rm index.html
Create a new HTML file: sudo vi index.html
Add your HTML code:
Example:
  <html>
    Hi, I am Himanshu.
  </html>
Save and exit.
Step 5: Access Your Website
Open a Browser.

1.Visit Your Website:

2.Enter your EC2 Public IP in the browser: eg. (13.45.589.25)

3.You should see your custom HTML page! 🎉
