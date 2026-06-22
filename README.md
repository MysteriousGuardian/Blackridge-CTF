<p align="center">
  <img src="blackridge_logo.png" alt="Blackridge Oil Company" width="220"/>
</p>

<h1 align="center">Blackridge CTF</h1>
<p align="center"><i>A beginner-friendly Capture the Flag lab — built at University of Borås</i></p>

---

## The Story

Blackridge Oil Company is a mid-sized energy firm with a decent website, a file server, and an IT department held together by one overworked IT chef named **Anna Lindqvist**.

Anna is good at her job. Mostly. But like a lot of people managing too many systems at once, she's cut a few corners — left a share open here, reused a password there, trusted that nobody would go looking.

Someone is going to go looking. That someone is you.

Your job is to work your way through Blackridge's internal systems — from the public-facing website all the way down to the file shares sitting quietly on the network. Every step teaches you something real. Every service hands you the key to the next one.

You're not here to break anything. You're here to find out what was already broken.

---

## Attack Chain

```
HTTP  →  FTP  →  SSH  →  SMB
```

Each chapter is a service. Each service has a flag. Find them all.

| Chapter | Service | Description |
|---|---|---|
| 01 | HTTP | The company website is hiding something in plain sight |
| 02 | FTP | The file server has folders that probably shouldn't be public |
| 03 | SSH | Getting a shell is one thing. Getting the *right* shell is another |
| 04 | SMB | Anna's share is open. Anna doesn't know you know that |
| Bonus | Wireshark | An old pcap file. An email thread. A name you've seen before |

---

## Getting Started

> You'll need a terminal and a bit of curiosity. That's it.

Each chapter lives in `/chapters/` and walks you through the challenge step by step — commands included, hints embedded, no prior experience required.

Start here → [`chapters/http.md`](chapters/http.md)

---

## Authors

<!-- Your turn — say what you want here -->

---

<p align="center"><sub>Built for educational purposes · University of Borås · 2025</sub></p>
