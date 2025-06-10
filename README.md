# Vanessa Bakare | Lead Cloud Engineer| Cloud Engineering Project

**Author:** Vanessa Bakare   
**Project Title:** The Future of Accessible Cloud Infrastructure for Africa  
**Description:** This is a dynamic landing page designed to demonstrate my skills in cloud engineering, web development, and server deployment using AWS EC2 and Nginx. It features a personalized, responsive layout that highlights my expertise in setting up cloud infrastructure, configuring web servers, and deploying web applications.

## My IP Address
16.170.250.170

## Screenshots Of The Rendered Website


## Step-by-Step Documentation  
### AWS EC2 Instance
- I began by logging into and opening my AWS Management Console and navigated to the EC2 section
- I then launched an EC2 Instance in AWS using Ubuntu Server and also created a key pair to enable remote ssh

### WSL Terminal
- To SSH into my EC2 instance from WSL, I needed to use the .pem private key file that was downloaded to my Windows Downloads folder.
- To copy the key pair file in Windows Downloads folder into my WSL home directory, I used this command:
```
cp /mnt/c/Users/USER/Downloads/key.pem ~/.ssh/
```
- After copying, I changed the file permissions so SSH would accept the key using this command:
```
chmod 600 ~/key.pem
```
### Configuring Networking
- Next, I configured the Security Group of my instance by navigating to "Security Groups" to ensure Inbound Rules allow: - SSH (port 22) from my IP and HTTP (port 80) from anywhere (0.0.0.0/0) and to also allow HTTPS (Port 443)
- Then i 

### Installing Nginx
- Before installing Nginx, I first updated my package repositories using these commands: 
```bash
sudo apt update
sudo apt upgrade -y
```
- Next I used this command to install Nginx :
```
sudo apt install nginx -y
```
- Next I started and enabled the Nginx service :
```
sudo systemctl start nginx
sudo systemctl enable nginx
```

### Creating and Deploying the HTML Landing Page
- After navigating to the right directory, I used the command below to create my .html file for my landing page:
```
sudo nano /var/www/html/index.html
```
- Next, I added my simple HTML content and saved the file
- Then I created my CSS file for stylying the HTML using this command :
```
sudo nano /var/www/html/style.css
```
- I went back to my home directory and created a new folder which i called "altSchoolExam"
- Then i used the commands below to copy my index.html and style.css files into this new directory - "altSchoolExam" :
```
cp /var/www/html/index.html ~/altSchoolExam/
cp /var/www/html/style.css ~/altSchoolExam/
```
  
### GitHub 
- I initialized Git in my working directory using `git init`
- I staged the index.html and style.css files using `git add .`
- Then I commited the file and added a message using `git commit -m "My commit message"`
- Then opened my Github in my browser and created a new repo for this project.
- Then i navigated to Security/tokens, to create a PAT to use for pushing to my remote repo
- Then i used the following commands"
  ```
  git remote add origin https://github.com/Vanessabakare/RepoName.git
  git branch -M main
  git push -u origin main
  ```
- Then i entered the PAT i had created earlier.

### Creating My README Doc
- Then i went on to create my README doc and I included all the required info and docs



