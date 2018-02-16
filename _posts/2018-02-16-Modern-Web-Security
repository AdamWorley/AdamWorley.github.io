---
layout: post
category : Security
tagline: "| Overview for handy browser security"
tags : [Linux, Windows, OsX, Firefox, Chrome, IE, Content Security Policy, CSP, HTTPS, Public Key Pinning, HPKP, Subresource Integrity, SRI]
---

{% include JB/setup %}

The following are covered in [this video](https://www.youtube.com/watch?v=j-0Bj40juMI) by Scott Helme and this is a textual overview of what he covers, just for future reference.


#### Content Security Policy (CSP)

The [CSP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) allows for resource control of a webpage. It is possible to set policies that provide a white-list of the domains/loactions where content for the page can be loaded from, this is useful in mitigating the use of cross server scripting attacks and other malicious external content from being loaded. 


#### Public Key Pinning (HPKP)

[Public Key Pinning](https://developer.mozilla.org/en-US/docs/Web/HTTP/Public_Key_Pinning) is a very simple way to decrease the risk of man in the middle attacks (MITM) performed with forged certificates.

It's possible that a certificate authority could produce a valid certifcate to a malicious user that can be used to present a *secure* and authorised connection, while be controlled by an attacker.

HPKP stores a hash of the *real* certifcate on the website, if the hash doesn't match the one being presented when the page loads, the webpage will fail to load and inform the user there's a security issue with the website.

Through the way in which HPKP works, it's possible that if a browser were to load the malicious site first, then the legitimate website will no longer function as the HPKP is stored in the browser from first use. It is also very easy to lock yourself out of a website through incorrect set-up, and as such it is very important to test and set up the HPKP carefully before deployment.


##### Usage

```
Public-Key-Pins: pin-sha256="base64=="; max-age=expireTime [; includeSubDomains][; report-uri="reportURI"]
```

Example from mozilla:
```
Public-Key-Pins: 
  pin-sha256="cUPcTAZWKaASuYWhhneDttWpY3oBAkE3h2+soZS7sWs="; 
  pin-sha256="M8HztCzM3elUxkcjR2S5P4hhyBNf6lHkmjAHKhpGPWE="; 
  max-age=5184000; includeSubDomains; 
  report-uri="https://www.example.org/hpkp-report"
  ```


#### Subresource Integrity (SRI) 

[Subresource Integrity](https://developer.mozilla.org/en-US/docs/Glossary/SRI) is described below;

> SRI is a security feature that enables browsers to verify that files they fetch (for example, from a CDN) are delivered without unexpected manipulation. It works by allowing you to provide a cryptographic hash that a fetched file must match.

In modern web development the use of content delivery networks (CDN) opens up a very appealing vector of attack for hackers and can open up a vulnerbailtiy to any website using them. To midigate this risk using SRI to ensure that the content provided by the CDN has not been altered or tampered with. Using this [SRI hash tool](https://report-uri.com/home/sri_hash) it's possible to generate a hash (of known safe content), now anytime a browser attempts to load content from the CDN the hash of the content will be compared to the hash stored on the webpage.

##### Usage

To use SRI two more parameters are used in the script tag, they are the following;

```
integrity="sha256-5i/mQ300M779N2OVDrl16lbohwXNUdzL/R2aVUXyXWA="
crossorigin="anonymous"
```

`crossorigin` should almost always be anonymous.

`integrity` is the hash of the content.

If the CSP is set to `require-sri-for script style` then any script or style tags that do not include the above will no longer load.
