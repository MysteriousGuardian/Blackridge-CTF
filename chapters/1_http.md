# Story Chapter 1: Introduction
Introducing Blackridge Oil Company! A corporation with several years worth of experience in the oil industry. They have recently modernized their IT-infrastructure with fast and resilient servers. However, there are some gaps that the IT-department have left out. It is your job to find and report all the clumbsy mistakes that Blackridge left out. It shouldn't be that serious... right?

# Construction of Blackridge HTTP (Prototype)
HTTP is split across two separate machines:
 - One machine takes care of the main website.
 - One machine takes care of the staff portal.

My initial plan was to have a single machine that takes care of both the staff portal and the main website. But I thought to myself, why not split both of them and make the structure way bigger than anticipated.
Another thing is that I have prompted both the main website and the staff portal on Claude, since I could absolutely not be bothered to create websites for two machines from scratch. Besides, AI does my job way better anyways.

Another bonus about having two seperate machines, is that the HTTP part of the CTF will be able to handle more load. Compared to having one machine, the HTTP traffic will be split between both machines and allow a smoother experience.

The only thing that I did on the HTTP machines was a simple apache2 installation. It was easily done with this command:

```sudo apt install apache2```

No configuration was needed. I only needed to transfer the folder that contains the main & staff site to their corresponding machine at /var/www/html/. It was as simple as that.
<img src="/images/http1.png">
<img src="/images/http2.png">
<img src="/images/http3.png">
(Blackridge main site)

<br>

<img src="/images/http4.png">
<img src="/images/http5.png">
<img src="/images/http6.png">
(Blackridge staff site)

<br>
<br>

Some things that I wanted to teach the students are basic security measures, such as not pressing random links, keeping passwords secure & not exposed, as well as ways to mitigate these errors. 

Current version: Prototype
