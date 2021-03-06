# Project 7 - WordPress Pentesting

Time spent: *17** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: A stored XSS vulnerability in WordPress allows an user with the posting capability to compromise the website. 
    - Vulnerability types: Cross-Site Scripting XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  1. Logged in as admin create a Contributor or Author account
  2.Log in as the Contributor or Author that was created using a different browser
  3.Use created account to compose a POST and click the TEXT tab then insert <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>
  4.Go to admin login and go to POST, click the post from Contributor or Author and click "Preview"
  5.Go to click on the post and the XSS will be executed saying "test" but can be changed to anything you want.
  - [ ] )
2. (Required) Enumeration
  - [ ] Summary: A vulnerability that reveals the version of WP that is running 
    - Vulnerability types:Enumeration, Footprinting
    - Tested in version:4.2
    - Fixed in version:  
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: Type http://wpdistillery.vm/readme.html as a URL and click enter. Will reveal the version of WP that is being used.
  
3. (Required) Privilege Escalation
  - [ ] Summary: This is where a user is created, specifically a Contributor or Author. After an Admin approves a comment from the user, the rest of the comments don't need approval. 
    - Vulnerability types:Privilege Escalation
    - Tested in version:4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 1.Create a Contributor or Author as a new user.
                           2.In a separate browser log in to the new user account and create a comment then post it. There will be a notification that will say something about waiting for moderation (by the admin).
                           3.Go back to the Admin login and approve the comment that is awaiting approval.
                           4.Go back to the new user login and make create another comment and post it, there will not be a notification about awaiting moderation.
  
    
