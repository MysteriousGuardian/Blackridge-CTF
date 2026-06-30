# Story Chapter 4: The Finale
You've made it to the last stop: Anna's private share.

Her supervisor's got her in a room right now asking questions, and from what's on this share, it's looking worse for her by the minute. Somewhere in here is the evidence that actually pins this down — proof of what she's been hiding, not just careless mistakes.

Dig through what's here. If you find other stuff she's let slip — bad planning, exposed company info, anything that shouldn't be sitting out in the open — grab that too. It all goes toward building the case against her.

Find the evidence. Make it stick.

# Construction of Anna's SMB (First Version)
Time to whip out the last Debian VM of the CTF. The plan is to recreate a desktop interface that has a lot of dummy files and a folder called Recycling Bin. These dummy files would contain mixed stuff, such as VLAN configuration on Blackridge, salaries for employees and even mails. This interface would be created in folder that would be shared using the SMB service Samba.

*Insert image*

First things first, basic configurations on the VM. After that, it was time to install the service:

`sudo apt install -y samba`

Then we added "anna" as a Linux user:

`sudo adduser anna`

