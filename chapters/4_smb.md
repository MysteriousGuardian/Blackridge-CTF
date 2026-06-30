# Story Chapter 4: The Finale
You've made it to the last stop: Anna's private share.

Her supervisor's got her in a room right now asking questions, and from what's on this share, it's looking worse for her by the minute. Somewhere in here is the evidence that actually pins this down — proof of what she's been hiding, not just careless mistakes.

Dig through what's here. If you find other stuff she's let slip — bad planning, exposed company info, anything that shouldn't be sitting out in the open — grab that too. It all goes toward building the case against her.

Find the evidence. Make it stick.

# Construction of Blackridge SMB (First Version)
Time to whip out the last Debian VM of the CTF. The plan is to recreate a desktop interface that has a lot of dummy files and a folder called Recycling Bin. These dummy files would contain mixed stuff, such as VLAN configuration on Blackridge, salaries for employees and even mails. This interface would be created in folder that would be shared using the SMB service Samba.

*Insert image*

First things first, basic configurations on the VM. After that, it was time to install the service:

`sudo apt install -y samba`

Then we added "anna" as a Linux user and changed her SMB password:

```
sudo adduser anna
sudo smbpasswd anna
```

After adding the user, it is time to design the "desktop". I started off by seperating the desktop to the VMs actual desktop. This is done to avoid any future issues and allow me to fully be creative. By creating a directory in /srv/samba/anna, I could link the path to the SMB config later on. 

`sudo mkdir -p /srv/samba/anna`

Before adding the dummy files and fixing the details, I wanted to fix the SMB config so that only the user anna has permission to see the share. With the help of smb.conf, I've added a new share block on the configuration file: 

```
[anna]
   path = /srv/samba/anna
   valid users = anna
   browseable = no
   read only = yes
   guest ok = no
```

Simply put, this block tells the service that the share known as "anna" will only be assessible through the path /srv/samba/anna by the user "anna" that we've created and it is a read only share. There is no permission, other than reading and opening text files. This will save me lots of trouble if for some reason a dummy file gets deleted by the player. No guest accounts are allowed on the share, not even root will work. Anna is the only allowed user. Oh yeah, the player can't browse anywhere else in the machine other than that specified path.

After adding the block, I've restarted samba: 

`sudo systemctl restart smbd`

Then it was time for testing. I tried to access it from my host machine and I did come across an error, however I instantly knew what the error were. During the SMB configuration, I've specified a user called "blr_anna" as in Blackridge Anna, but I've created a user called "anna". Names don't match and rejects my SMB connections. It was an easy fix, just change the SMB configuration to the correct user and I was all set.

By using this path:
\\(SMB's IP-Address)\anna

I was prompted to a login box:
*Insert image of login box*

B
