# Quick CMS Stored XSS v6.7

## Author: (Sergio)

**Description:** A Cross-Site Scripting (XSS) vulnerabiliti in Quick CMS v6.7 allows a local attacker to execute arbitrary code via a crafted script to the to the SEO - Meta description in the Pages Menu.

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the Meta description of "Pages- SEO" allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "Pages - SEO ." section off General Menu. 

![XSS Payload SEO - Meta Description](https://github.com/sromanhu/-Quick-CMS-Stored-XSS---SEO-Meta-description/assets/87250597/edf7796f-4081-46b1-97f5-acfe6c2c067f)





We edit that SEO Settings and see that we can inject arbitrary Javascript code in the Meta Description field.


### XSS Payload:

```js
'"><svg/onload=alert('XSS')>
```


In the following image you can see the embedded code that executes the payload in the main web.
![XSS resultado SEO - Metadescription](https://github.com/sromanhu/-Quick-CMS-Stored-XSS---SEO-Meta-description/assets/87250597/f740d472-54ec-4ac2-a4f7-6e14d6b736d1)





</br>

### Additional Information:
https://opensolution.org/cms-system-quick-cms.html

https://owasp.org/Top10/es/A03_2021-Injection/
