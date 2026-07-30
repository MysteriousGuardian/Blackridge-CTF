# Story Chapter 2: Plaintext and Pipelines
Well, it looks like the website needs a lot of maintenance and patching. Let's hope that the FTP server is doing better. It shouldn't be as bad as the websites, right?

# Construction of Blackridge FTP
FTP runs on it's own dedicated machine. It has it's own reasoning that is very similar to the HTTP part of this CTF. It makes the IT infrastructure more mature and realistic, which is what we try to aim. 

The service that was used on the FTP part is called vsftpd. Installation process was easy as well, since we only needed to write this on the terminal:
```sudo apt install vsftpd```

It didn't take long until we were ready to configure the service. By editing vsftpd.conf as a user with root permissions, we can see that there is a guide that lets us uncomment certain rows to activate the setting as shown below:
<img src=/images/ftp1.png>

The configuration that I've decided to use, is modified so that I can ensure that everything works as it should. Here it is: 
<img src=/images/ftp2.png>

It looks messy, I know. But I will quickly explain what it does;
I've allowed two different types of accounts to use this service, which is an anonymous user and a local user. The anonymous user will get directed to a seperate folder compared to the local users. The local users will be redirected to their "home" folder where lots of files will be up for grabbing. I've also fixed so that accounts will have no permission to delete or add any files, thus minimizing risks for sabotage. 

As we all know, the odds of stuff the first time is very low. I did go through one specific error that took some time and I still don't know how the error came up. I knew one thing though, the configuration setting called chroot was the cause of the problem. So I disabled chroot and everything worked as it should.

Something to note, I don't intend to make these machines with perfect craftmanship. As long as it works as I intend, I am more than happy to conclude the part.

After the configuration part, I decided to test out all the accounts to see if they work as I intended. It passed with flying colors. (oh yeah, I added a special banner too) :)

<img src=/images/ftp3.png>

Since it worked, it is time to add content to all account types. I will be treating the anonymous account as a public account, meaning that I will be adding public reports, FAQ and stuff that you can find on regular FTP servers. On the blr_admin account, I will be adding more confidential information that should not be disclosed. Contracts, personal information, financial reports and stuff like that will be hidden to the public. But don't worry, there are flags in both anonymous account and the blr_admin account, to allow the players to learn the difference between both account types. 

To obtain the login details for blr_admin account and proceed to Chapter 3, you will need to find the login details on the staff website. 

Anyways, this is how the anonymous folder looks like: <br>
<img src=/images/ftp4.png>

And this is how the blr_admin folder looks like (note: these are folders, the text files are inside the folders):
<img src=/images/ftp5.png>
