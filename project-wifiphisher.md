---
layout: default
title: The Wi-Fi is Gaslighting You: An MITM Project
permalink: /projects/wifiphisher
---

# The Wi-Fi is Gaslighting You: an MITM Project

For a Capstone assignment, I was tasked with a simple objective: successfully intercept wireless traffic. But instead of just writing a dry report, I decided to dive into why your devices are essentially too clingy for their own good.

Using a pair of adapters and a healthy dose of technical mischief, I set out to prove that the biggest vulnerability in your home network isn't a complex software bug—it’s the fact that humans are hard-wired to trust a 'Please Enter Password' box if it pops up at the right time. This project isn't just a story about packet injection and SSID cloning; it’s a deep dive into the 'Evil Twin' method and why your Wi-Fi might actually be gaslighting you.

## Why I Chose This (The "Work Smarter, Not Harder" Defense)

I chose the Evil Twin MITM approach because it targets the "human element" rather than trying to break complex encryption. While a traditional brute-force attack on a WPA2 handshake can take an eternity and depends entirely on the password's complexity, this method uses a Captive Portal to bypass the math entirely.

By combining a deauthentication attack to kick the victim off the legitimate network with a cloned SSID, I created a scenario where the user "volunteers" their credentials to regain internet access. This demonstration proves that even with strong WPA2 encryption, Social Engineering remains the most efficient path for an attacker because it exploits the user's trust rather than the network's software.

## The Methodology: A Step-by-Step Breakdown

### Step 1: The "I Hope This Installs" Phase

The first step was setting up the toolkit in Kali Linux. I cloned the wifiphisher repository from github and installed the dependencies.

git clone https://github.com/wifiphisher/wifiphisher.git

sudo python setup.py install

[INSERT SCREENSHOT 1: Showing the wifiphisher directory downloaded]

### Step 2: Fighting the Final Boss (Roguehostapd)

A major part of this assignment involved getting roguehostapd to function. I hit a massive skill check when the source code had an outdated ConfigParser module that was breaking everything. I had to manually patch hostapdconfig.py to use the **modern** configparser library.

[INSERT SCREENSHOT 2: Your code editor or terminal showing the roguehostapd files]

### Step 3: Manifesting the Evil Twin

With the tools patched, I was ready to launch wifiphisher. But first, I had to make sure my two USB Wi-Fi adapters were plugged in and recognized by the VM. Why two adapters? One needs to deauthenticate/jam the network so users are booted off. The other comes in to "save the day" by copying the SSID (Wi-Fi name) of the now jammed Wi-Fi. This took some time, but eventually they were both recognized and I was able to run wifiphisher.

I selected my target network, "704," and chose the Firmware Upgrade Page scenario. This is where the gaslighting begins... telling the user their router is needs to update.

[INSERT SCREENSHOT 3: Wifiphisher scanning and selecting network 704]

### Step 4: The "Kick Out" (Deauthentication)

One adapter began jamming the original network while the other broadcasted the cloned, unsecured SSID. My host PC got kicked off the real Wi-Fi and, being a stage-five clinger, immediately looked for anything with the same name.

[INSERT SCREENSHOT 4: Wifiphisher showing "Emitting Beacon frames" and jamming status]

### Step 5: Bypassing Windows

Modern Windows machines are suspicious. My PC tried to avoid my trap by redirecting to msn.com (default for Firefox) instead of the router update page. To force the issue, I manually navigated to the gateway IP, 10.0.0.1, which finally forced the fake "Firmware Upgrade" screen to load.

[INSERT SCREENSHOT 5: The fake "Firmware Upgrade" page on the victim's browser]

### Step 6: Gimme the Loot!

The victim (me) entered the [dummy] password TestPassword123! to "verify" the update. Instantly, my Kali terminal lit up with the credentials in cleartext. The "Firmware Upgrade In Progress" screen kept them distracted while I sat there with their keys.

[INSERT SCREENSHOT 6: Kali terminal showing the captured POST request and the password]

## What I Learned (The TL;DR)

The biggest hurdle was realizing that modern hardware and operating systems are much more resilient than I expected. Getting drivers to cooperate and bypassing Windows "connectivity checks" proved that the environment setup is often harder than the actual attack.

I learned that intercepting wireless traffic isn't just about technical skill—it's about understanding how devices "handshake" and how easily that trust can be manipulated. To prevent being exploited this way, victims should be wary of "Open" networks that share the same name as their home Wi-Fi and never enter a Pre-Shared Key into a browser-based pop-up.

## The Moral of the Story

Upgrade to WPA3, use a VPN, and if your Wi-Fi starts acting mid or asks for your password in a browser tab, do a double take.
