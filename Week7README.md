# Project 7 - WordPress Pentesting

Time spent:  20 hours spent in total

> Objective: Find, analyze, and document three vulnerabilities affecting an old version of WordPress

## Pentesting Report

1. Authenticated Stored Cross-Site Scripting  (CVE-2015-5622)
  - [ ] Summary: 
    - Vulnerability types:  Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.2
    - [ ] Steps to recreate: 
 Allows remote authenticated users to inject arbitrary web script or HTML by leveraging the Author or Contributor role to place a crafted shortcode inside an HTML element, related to wp-includes/kses.php and wp-includes/shortcodes.php. 
  - [ ] Affected source code: 
    - [Link 1] (https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622)

2. Crytographically Weak Pseudo-Random Number Generator- PRNG (CVE-2017-05493)
  - [ ] Summary: 
    - Vulnerability types: Cryptographic Issues
    - Tested in version: 4.2
    - Fixed in version: 4.7.1
    - [ ] Steps to recreate: 
wp-includes/ms-functions.php in the Multisite WordPress API does not properly choose random numbers for keys, which makes it easier for remote attackers to bypass intended access restrictions via a crafted (1) site signup or (2) user signup.
  - [ ] Affected source code:
    - [Link 1] (https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5493)
3. Host Header Injection in Password Reset (CVE 2017-8295)
  - [ ] Summary: 
    - Vulnerability types: Weak Password Recovery Mechanism for Forgotten Password
    - Tested in version: 4.2
    - Fixed in version: 4.7.4
  - [ ] Steps to recreate: 
WordPress relies on the Host HTTP header for a password-reset e-mail message, which makes it easier for remote attackers to reset arbitrary passwords. By using ( wp-login.php?action=lostpassword request) and then arranging for this message to bounce or be resent, leading to transmission of the reset key to a mailbox on an attacker-controlled SMTP server. 
  - [ ] Affected source code:
    - [Link 1]( https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-8295)

4. Application Denial of Service (DoS) (CVE-2018-6389)
  
- [ ] Summary: 
    - Vulnerability types: Resource Management Errors
    - Tested in version: 4.2
    - Fixed in version: unpatched (through 4.9.2)
  - [ ] Steps to recreate: 
Unauthenticated attackers can cause a denial of service (resource consumption) by using the large list of registered .js files (from wp-includes/script-loader.php) to construct a series of requests to load every file many times.
  - [ ] Affected source code:
    - [Link 1]( https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-6389) 

## Assets
WPScan to ID vulnerabilities 
## Resources
- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
GIFs created with [LiceCap](http://www.cockos.com/licecap/).
## Notes
N/A
## License

    Copyright 2018 Courtney

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at (http://www.apache.org/licenses/LICENSE-2.0)
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
