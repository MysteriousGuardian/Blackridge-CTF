<p align="center">
  <img src="blackridge_logo.png" alt="Blackridge Oil Company" width="220"/>
</p>

<h1 align="center">Blackridge CTF</h1>
<p align="center"><i>A beginner-friendly Capture the Flag lab</i></p>

---

## The Story

Blackridge Oil Company looks fine from the outside. Website's up, servers are running, nothing seems wrong.

But Anna, the IT Manager, has been acting strange lately. The person who's supposed to keep everything locked down has been doing the opposite — same password on everything, folders left open, and whenever someone brings it up she deflects or points fingers.

Something's going on. Your job is to find out what.

You'll start from the website and work your way in. Every service you get through hands you something for the next one. It all leads back to Anna.

---

## Attack Chain

```
HTTP  →  FTP  →  SSH  →  SMB
```

Each chapter is a service. Each service has flags in them. Find them all.

| Chapter | Service | Description |
|---|---|---|
| 01 | HTTP | Blackridge Website |
| 02 | FTP | Blackridge File Server |
| 03 | SSH |  IT Department Access |
| 04 | SMB | Anna's share |

---

## Getting Started

Each chapter lives in `/chapters/` and shows you the construction of each service. No copyrights on this lab, if you want to try it out at home, you are more than welcome :) 


---

## Authors
David Tekin (MysteriousGuardian)
<br>
Melisia Younan




---
## Contributors
Oscar Lisnell
