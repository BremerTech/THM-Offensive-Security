<h1>TryHackMe - Intro To Offensive Security Lab</h1>

<h2>Description</h2>
This lab consists of an easy break down into the world of an ethical hacker that looks for faults in websites that leads to vulnerable information or access to important systems. The following lab is TryHackMe's introduction into the world of hacking by simulating a loophole in a banking website, where money can be transferred to another account.
<br />


<h2>Languages and Utilities Used</h2>

- <b>GoBuster v2.0.1</b> 
- <b>Terminal</b>
- <b>Web Browser</b>

<h2>Environments Used </h2>

- <b>Ubuntu</b> 

<h2>Lab Walk-through:</h2>

<p align="center">
Launch Browser and Visit Targeted Site: <br/>
<br />
<img src="https://i.imgur.com/DOthw8z.png" height="80%" width="80%" alt="Intro To Offensive Security"/>
<br /> 
<br />

<p align="center">
Finding Hidden Website Pages :  <br/>
<img src="https://i.imgur.com/k0MPRjZ.png" height="80%" width="80%" alt="Intro To Offensive Security"/>

Open Terminal and use command to find potentially hidden and vulnerable pages.

gobuster -u http://fakebank.com -w wordlist.txt dir

In the command above, -u is used to state the website we're scanning, -w takes a list of words to iterate through to find hidden pages.

You will see that GoBuster scans the website with each word in the list, finding pages that exist on the site. GoBuster will have told you the pages it found in the list of page/directory names (indicated by Status: 200).

Gobuster is a tool used to brute-force: URIs (directories and files) in web sites, DNS subdomains (with wildcard support), Virtual Host names on target web servers, Open Amazon S3 buckets, Open Google Cloud buckets and TFTP servers.

<p align="center">
<img src="https://i.imgur.com/uydghT3.png" height="80%" width="80%" alt="Intro To Offensive Security"/>

A wordlist may contain thousands of words to search through in the .txt file.
<br />
<br />
<p align="center">
Finding Secret Pages: <br/>

<p align="center">
<img src="https://i.imgur.com/lVRqR5V.png" height="80%" width="80%" alt="Intro To Offensive Security"/>

At this point you will be shown what unprotected pages are vulnerable.

Using TryHackMe's example, with the use of GoBuster and terminal we found a secret bank transfer page that allows us to transfer money between accounts at the bank (/bank-transfer). 

Type the hidden page into the FakeBank website in the browser.

http://fakebank.com/bank-transfer

From here we were able to enter account details and transfer funds from one bank account to another.
<br />
<br />

<p align="center">
Mission Complete:  <br/>

 <p align="center">
<img src="https://i.imgur.com/1s7L8DD.png" height="80%" width="80%" alt="Intro To Offensive Security"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
