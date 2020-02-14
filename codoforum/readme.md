# This is what I achived when research on [Codoforum](http://codologic.com/)
## Reflected XSS
### Firstly, login into a user account, and create a new topic with title <svg/onload=alert(document.domain)>
![](https://github.com/matuhn/Research/raw/master/codoforum/1.png)
### Secondly, do nothing and refresh the page 
![](https://github.com/matuhn/Research/raw/master/codoforum/2.png)
### It causes by this block of code 
![](https://github.com/matuhn/Research/raw/master/codoforum/3.png)
### Vendor confirmed
![](https://github.com/matuhn/Research/raw/master/codoforum/image.png)
![](https://github.com/matuhn/Research/raw/master/codoforum/20200214_072124.jpg)
# REPORT TIMELINE
# 02/13/2020: Discovered the vulnerability
# 02/13/2020: Vendor confirmed
