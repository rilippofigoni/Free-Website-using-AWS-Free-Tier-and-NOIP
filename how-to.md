### Creating a Free Website using AWS Free Tier and NOIP

* **Create EC2 instance using AMI Linux - AMI Linux t2.micro**

* **update the package**
  
  ```bash
  sudo yum update -y
  ```

* **Install apache http server**
  
  ```bash
  sudo yum install httpd
  ```

* **Start http server**

* ```bash
  sudo systemctl start httpd.service
  ```

* **Create html file**
  
  ```bash
  vi /var/www/html/mypage.html
  ```

* for example page you can use this code
  
  ```html
  <html>
  
  <head>
  
  <title>My example page</title>
  
  </head>
  
  <body>
  
  This is my personal website!
  
  </body>
  
  </html>
  ```

* Verify your web page on browser

* http://ec2-3-142-147-5.us-east-2.compute.amazonaws.com/mypage.html

* **Register free sub domain at http://noip.com and configure your DDNS router server**

* **Enable extra packages for enterprise linux(epel) repository and install noip**
  
  ```bash
  sudo amazon-linux-estras install epel -y
  ```

* **Install noip package**
  
  ```bash
  sudo yum install noip
  ```

* **create noip configuration – enter noip username and password**
  
  ```bash
  noip2 -C
  ```

* **Start the noip service**
  
  ```bash
  sudo systemctl start noip
  ```

After a minute verify the IP change and check the page with the new domain url

http://xxxxxxxx.ddns.net/mypage.html
