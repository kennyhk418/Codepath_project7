# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) User Enumeration
  - [x] Summary: 
    - Vulnerability types:
	User Enumeration
    - Tested in version:
	4.1.2
    - Fixed in version: 
	Not yet fixed
  - [x] GIF Walkthrough: 

	<img src='http://i.imgur.com/R6peToL.gif' title='Video Walkthrough 1' width='400px' alt='Video Walkthrough 1' />
  - [x] Steps to recreate: 
	When I tried to login with the admin username and a false password, the screen will display "ERROR: The password you entered for the username admin is incorrect." However, 
	if I tried to login with some random username which does not exist, it will show "Error: Invalid username."
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/4.1.2/src/wp-login.php)

### 2. (Required) CVE-2015-5622
  - [x] Summary: 
    - Vulnerability types:
	XSS	
    - Tested in version:
	4.0
    - Fixed in version:
	4.1.6 
  - [x] GIF Walkthrough:

	<img src='http://i.imgur.com/ibSOBwc.gif' title='Video Walkthrough 2' width='400px' alt='Video Walkthrough 2' />
  - [x] Steps to recreate: 
	We would perform the XSS on the post, and put in `<a href="[caption code]=" onmouseover="alert('test')">link</a>`.
  - [x] Affected source code:
    - [Link 1](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622)

### 3. (Required) CVE-2015-5714
  - [x] Summary: 
    - Vulnerability types:
	XSS
    - Tested in version:
	4.0
    - Fixed in version: 
	4.1.8
  - [x] GIF Walkthrough: 

	<img src='http://i.imgur.com/M4fpc4o.gif' title='Video Walkthrough 3' width='400px' alt='Video Walkthrough 3' />
  - [x] Steps to recreate: 
	We would like to exploit XSS vulnerbility in the comment section, so we can put in `<script>alert('test')</script>`. A pop up window will appear in the comment page.
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

4. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [Ki Yin Kenny Lam]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.