# html_basic_code_myprofile

🌟 Deploying a Static Website on AWS EC2: A Simple Guide 🌟

In this post, I demonstrate how to deploy a static website using an EC2 instance on Amazon Linux. 

<h1>Here's a quick and easy step-by-step guide:</h1>

Step 1: Launch EC2 Instance. Select Amazon Linux as the operating system.

Step 2: Configure Security Group
Allow HTTP (80), HTTPS (443), and SSH (22) ports.

Step 3: Connect to Your Instance
Use the public IP address in PuTTY or any SSH client.
Configure private keys for secure access.

Step 4: Install and Configure Apache
    
     I. Update the System: 
        "sudo yum update -y"

    II. Install Apache Server: 
        "sudo yum install httpd -y"

       Install Nginx Server: 
       "sudo yum install nginx -y"

    III. Start Apache Server: 
       "sudo systemctl start httpd"

        Start Nginx Server: 
       "sudo service start nginx"
 
    IV. Check Apache Status: 
       "sudo systemctl status httpd"

        Check Nginx Status: 
       "sudo systemctl status nginx"
 
V. Create HTML File: 
 "via index.html"

<br>
Step 5: Move HTML File or create file in that derectory.<br>
<br>
 Copy the file to the Apache/Nginx directory: <br>
 <br>
 "sudo cp index.html /var/www/html/"<br>
 "sudo cp index.html /usr/share/nginx/html/"<br>
<br>
Step 6: Create a Symlink<br>
<br>
  Point to the file directory.<br>
  <br>

     " sudo systemctl enable httpd "<br>
     " sudo systemctl enable nginx "<br>

Step 7: Access Your Website<br>
Open your browser, type http://localhost, and hit Enter.<br>
<br>
<br>
Your static website is now live! 🚀
