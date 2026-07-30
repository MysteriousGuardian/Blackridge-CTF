# Story Chapter 2: Plaintext and Pipelines
Well, it looks like the website needs a lot of maintenance and patching. Let's hope that the FTP server is doing better. It shouldn't be as bad as the websites, right?

# Construction of Blackridge FTP
FTP runs on it's own dedicated machine. It has it's own reasoning that is very similar to the HTTP part of this CTF. It makes the IT infrastructure more mature and realistic, which is what we try to aim. 

The service that was used on the FTP part is called vsftpd. Installation process was easy as well, since we only needed to write this on the terminal:
```sudo apt install vsftpd```

It didn't take long until we were ready to configure the service. By editing vsftpd.conf as a user with root permissions, we can see that there is a guide that lets us uncomment certain rows to activate the setting as shown below.
