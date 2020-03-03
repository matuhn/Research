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
# 02/17/2020: CVE-2020-9007

## Stored XSS
### Create a post with Tags : 1" onmouseover="alert(1)
### XSS will be fired if you put your mouse on tags

# REPORT TIMELINE
# 02/24/2020: Discovered the vulnerability
# 03/03/2020: Vendor confirmed

## Reflected XSS
### Go to : http://URL/codo/index.php?u=user/profile/11110%22%20accesskey=%22X%22%20onclick=%22alert(1)
### Use Alt+Shift+X , XSS will be fired

# REPORT TIMELINE
# 02/24/2020: Discovered the vulnerability
# 03/03/2020: Vendor confirmed
![](https://github.com/matuhn/Research/raw/master/codoforum/confirm.png)
