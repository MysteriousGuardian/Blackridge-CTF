<p align="center">
  <img src="blackridge_logo.png" alt="Blackridge Oil Company" width="220"/>
</p>

<h1 align="center">Blackridge CTF</h1>
<p align="center"><i>A beginner-friendly Capture the Flag lab</i></p>

---

## The Story

Blackridge Oil Company is a mid-sized oil company with different types of services, such as a website and a file server. The company has hired an IT team that is controlled by the IT Manager "Anna Lindqvist".

Anna is pretty good at her job. But she has been acting quite odd recently. She leaves gaps of Blackridge open to the public without any precautions, using the same password EVERYWHERE and even blaming it on others. 

It's time to find out what causes Anna to be acting disrupted.

Your job is to work your way through Blackridge's internal systems — from the public-facing website all the way down to the file shares sitting quietly on the network. Every step teaches you something real. Every service hands you the key to the next one.

You're not here to cause even more havoc. You are here to solve a mystery.

---

## Attack Chain

```
HTTP  →  FTP  →  SSH  →  SMB
```

Each chapter is a service. Each service has a few flags in them. Find them all.

| Chapter | Service | Description |
|---|---|---|
| 01 | HTTP | Blackridge Website |
| 02 | FTP | Blackridge File Server |
| 03 | SSH | IT Departments Secure Shell Access |
| 04 | SMB | Anna's share |

---

## Getting Started

> You'll need a terminal and a bit of curiosity. That's it.

Each chapter lives in `/chapters/` and shows you the construction of each service. No copyrights on this lab, if you want to try it out at home, you are more than welcome :) 



---

## Authors

<!-- Your turn — say what you want here -->

---

<p align="center"><sub>Built for educational purposes · University of Borås · 2025</sub></p>
