# PXL-Security-Expert-Phishing-Lab
This lab was created for PXL Security Expert and demonstrates various phishing technologies currently in use.

The main tool used throughout this lab is Gophish: https://github.com/gophish/gophish

---
## Case 1: Malicious MS Word file
This case demonstrates the classic Word file with macros. For this lab, the macro opens a URL in the default browser via a PowerShell command; however, in practice, this could be replaced with any malicious command.

### First draft
First, let's try to just send this file as an attachment to a legit-looking email.
First, let's attempt to send this file as an attachment to a legitimate-looking email.
The obvious problem is that it's a .dotm file, which first, looks somewhat suspicious, and second, requires user input to run the macros.
We can improve this by feeding the email template into AI with the prompt: 'Add a step that requires the user to press "Enable" on the macros prompt, and justify it with security-related reasoning.' This generates an email that asks the user to allow macros, making it more convincing. The typical email recipient will either ignore the email or follow the steps and become compromised.
However, Windows Defender may block the download of this file. While this is a concern, it's not particularly difficult to include instructions on disabling Windows Defender.
This type of campaign is designed to be sent to a large number of victims, so some non-technical users may fall for it.

### A .docx file with macros
Apparently, it's possible to use a 'legit' `.docx` file to run macros. How?
Since the `.docx` file is just an archive, we could rename it into `.zip` and gain access to its content. It contains some `.xml` files, which are not insteresting for us. 
But what is insteresting is the file `settings.xml.rels` in `./word/_rels/` folder. 
This file contains a `Target` parameter which, funny enough, points to a file that should be opened when opening `.docx` file. And it accepts URLs. 
So we can host our `.dotm` file on GitHub, place its link as Target and use as a payload.

...And Gmail blocks this file because of some 'security issues' and 'detection of a dangerous file' inside it. Placing it in archive also doesn't help, in still can't pass the scan. So it's not a viable option for our mass-phishing attack.

Source: https://blog.redxorblue.com/2018/07/executing-macros-from-docx-with-remote.html

---
## Case 2: Landing pages
When creating a phishing campaign it is required to make a landing page inside Gophish. This creates a custom HTML page with your link, that then 'steals' all data entered in the fields. For this lab both Gophish and the landing pages will be hosted in a closed environment, so the phishing link will be localhosts, but it also can be easily set behind a legitimate domain name and open internet.
It was not covered in first case, but Gophish has very powerful email editing capabilities. It accepts not only plain text with basic formatting, but also HTML markup, which allows the creation of pretty convincing mails. 
The landing page creation is also pretty simple: you could either write a HTLM code OR just give an URL and it will just clone webpage and create a phishing landing page out of it.
Another useful function is redirection, which can redirect user to a legit website after capturing theirs data, so user won't even notice that something happend. 
