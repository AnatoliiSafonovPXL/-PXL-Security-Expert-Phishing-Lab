# PXL-Security-Expert-Phishing-Lab
This lab is made for PXL Security Expert and describes different phishing technologies used at the time.

Main tool in all of this will be Gohpish: https://github.com/gophish/gophish

---
## Case 1: Malicious MS Word file
Here are doing the classic Word file with macros. For this lab, the macro opens an URL in default browser via PowerShell command, so in general, it could also be a malicious command instead.

### First draft
Firstly, let's try to just send this file as an attachment to a legit-looking email.
The obvious problem is that it's a `.dotm` file, which 1st look a bit strange, 2nd requires an user input to run the macros.
Let's just throw the email template into AI with prompt 'Add a step that user needs to press "Enable" on macros prompt, and reason it with some security things'. And we get an email that asks user to allow running macros, nice. The regular email reader will either ignore an email, or, follow the steps and he'll get pwned.
Only if Windows Defender doesn't block the download of this file. Which he does, but realistically, it is not a big deal to also give instructions on how to disable Windows Defender.
This kind of campaign is meant to be sent to a large ammount of victims, so some non-technical user just may fall for it.

### A .docx file with macros
Apparently, it's possible to use a 'legit' `.docx` file to run macros. How?
Since the `.docx` file is just an archive, we could re-name it into `.zip` file and gain access to files inside it. It contains some `.xml` files, which are not insteresting for us, but what is insteresting, is the file `settings.xml.rels` in `./word/_rels/` folder. 
In it there is a `Target` parameter which, funny enough, points to a file that should be opened when opening `.docx` file. And it accepts URLs. 
So we will host our `.dotm` file on github, place its link as Target and use as a payload.

And GMail blocks this file because of some 'security issues' and 'dangerous file' inside it. Placing it in archive also doesn't help, in still can't pass the scan. So it's not a viable option for our mass-phishing attack.

Source: https://blog.redxorblue.com/2018/07/executing-macros-from-docx-with-remote.html

---
## Case 2: Landing pages
When creating a phishing campaign it is required to make a landing page inside Gophish. What it does, is it creates a custom HTML page with your link, that then 'steals' all data in the fields. For this lab both Gophish and the landing pages will be hosted in a closed environment, so the phishing link will be localhosts, but it also can be easily set behind a legitimate domain name and open internet.
It was not covered in first case, but Gophish has very powerful email editing. It accepts not only plain text with a bit of formatting, but also HTML marking, which allows creating of pretty convincing-looking mails. 
The landing page creation is also pretty simple: you could either write a HTLM code OR just give an URL and it will just clone webpage and create a phishing landing page out of it.
The other useful function for it is redirection, which can redirect user to a legit website after stealing theirs data, so user won't even notice that something happend. 
