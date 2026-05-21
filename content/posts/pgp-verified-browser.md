---
title: "Pgp Verified Browser"
date: 2026-05-21T11:42:32+10:00
draft: false
---

# Why did I make a PGP verified browser?

Hello, World!

It's been a while since I've posted anything on my blog but well here we are.

I believe that the current web is sort broken. Or well I didn't really like the fact that domains are paid and we have a really centralised web. So I decided to go out on a whim and create PWSS (PGP Web Static Secure) as a transport agnostic protocol for the web.

## What even is this?

Well, its not really a protocol but more so a regulation for the web. It ensures that every file on the internet is signed with pgp and their fingerprint is tied to the "domain" that they own, and as such if the content is intercepted and modified in transit, the signature check will not complete at the end or the fingerprint will not match the "domain" owner's fingerprint. Basically, this allows you to detect MITMs and as such by default assumes all nodes involved in the network are compromised.

Currently, it supports transport over https and really the only site on it is my blog (hence `pwss://zai1208` and the subpages `zai1208/[page_name]` for my blog pages)

For more info on the spec you can visit <https://github.com/zai1208/pwss/blob/main/SPEC.md>

## Why did I make this?

Cause I was fed up with the web.

## How do I use it?

If you want to get started with a simple Qt6 browser, you can run

```bash
yay -S pwss-browser-qt6
gpg --recv-keys 1D621CE3F6D554DC3E6E2551B1437E7DFC87A9B4
pwss-browser-qt6
```

and you will land directly on this page.

Enjoy the new web I guess.

{{< pgp_banner >}}
