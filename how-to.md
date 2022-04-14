### Creating a Free Website using AWS Free Tier and NOIP

* Create EC2 instance using AMI Linux
  

* update the packages
  > yum update -y

* Install apache http server
 > yum install httpd

* Start http server
  > service start httpd
 
* Create html file
 > vi /var/www/html/mypage.html
 
* view the page in browser
> http://ec2-11-222-333-44.us-west-2.compute.amazonaws.com/mypage.html

* Register a new free sub domain (noip.com) : Create an account and subdomain in noip website

* (http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dynamic-dns.html)

    
* Install noip package
  
* Enable extra packages for enterprise linux(epel) repository and install noip
            # yum-config-manager –enable epel
            # yum install -y noip
    create noip configuration – enter noip username and password
        # noip2 -C
    enable noip service with the configuration created
        # chkconfig noip on
    verify the noip service
        # chkconfig –list noip
    Start the noip service
        # service noip start
    After a minute verify the IP change against the domain name (xxxxx.hopto.org) in  noip.com site
    Check the page with the new domain url
        http://xxxxx.hopto.org/mypage.html
