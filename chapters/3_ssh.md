# Story Chapter 3: "Secure" Shell
Well, the FTP looked just as bad. Very basic security measures, which is odd. It's like Blackridge is being sabotaged, but there is only one way to find out. There is a login on one of the files to Blackridge SSH. Let's see what is behind the scenes. 

# Construction of Blackridge SSH (Prototype)
For this part, I decided to use OpenSSH as the service. To install OpenSSH, I ran this command: 
<br>
```sudo apt-get install openssh-server```

After installing the service, I needed to edit the configuration file a bit to adapt it for approximately 80-90 students at the same time. By editing the file ```/etc/sshd_config```, I would need to change the configuration file for it's purpose.
<img src="images/ssh1.png">

To be honest, I have no idea what everything does, but I know one thing for sure. It works splendid, as I've tested it like 5 times. 

Then the last thing to add, was some dummy files. I wanted the SSH part of this CTF to be a mini privilege escalation stage, where a user climbs up the hierarchy with techniques. While this does not represent an actual privilege escalation, it is enough to show how important securing systems is. 

The login details for the higher tier account is in a script which the user will have to nano, cat or something similar to it.

Anyways, here are the dummy files in anna's account:
<img src="images/ssh2.png">
<img src="images/ssh3.png">

And here is temp_ssh's home folder:
<img src="images/ssh4.png">
