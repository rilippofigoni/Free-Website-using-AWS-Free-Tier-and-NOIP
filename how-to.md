### Creating a Free Website using AWS Free Tier and NOIP

* **Create EC2 instance using AMI Linux - AMI Linux t2.micro**

* **update the package**
  
  ```bash
  sudo yum update -y
  ```

* **Install apache http server**
  
  ```bash
  sudo yum update -y
  ```

* **Start http server**

* ```bash
  sudo systemctl start httpd.service
  ```

* **Create html file**
  
  ```bash
  vi /var/www/html/mypage.html
  ```

* **view the page in browser**
  
  http://ec2-3-142-147-5.us-east-2.compute.amazonaws.com/mypage.html


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
  noip -C
  ```


* **Start the noip service**

  ```bash
  sudo system start noip
  ```

After a minute verify the IP change and check the page with the new domain url

http://xxxxxxxx.ddns.net/mypage.html
