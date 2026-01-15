---
layout: post
title: "ELIF #2 - MITRE ATT&CK"
date: 2026-01-14
categories: [elif]
---

# Intro

Cybersecurity. Cyber warfare. Cyber attacks. Cyber defense. Advanced Persistent Threat. Reconnaissance. Infiltration. Exfiltration. All of these are terms used in the field of Information Security, but what else do they remind you of? If you said the military, congratulations because you're going to the fast money round.

Isn't that what militaries do? They attack, they defend, they track and eliminate threats, they do reconnaissance to scope out the enemy, they infiltrate enemy lines to accomplish secretive missions, they exfiltrate sensitive items and documents. What does that have to do with cybersecurity? Everything. Welcome to the MITRE ATT&CK framework, let's break this thing down.

# What's with the Miltary Terminology?

Much like military operations, cyber attacks *are* campaigns. We're not talking about a simple click and go, we're talking about a full on operation that requires several steps to accomplish a goal.

Think about it this way. Since the beginning of human history, war has been a constant. The greatest generals and minds of history all had something in common which helped them win and gain glory: they thought like their enemy. It is common knowledge that to win against someone, not only in war but in any player versus player type game, you have to think like the enemy. If I were in the enemies shoes here, what would I do? 

Chess: I have control of the center of the board and have the ability to begin an attack on the castled king with my setup. How will my opponent react if I move my queen/bishop/knight/etc?

League of Legends: The enemy team is ARAM mid, we have one player respawning in 30 seconds, they have their full team, Ocean Drake is up for grabs, and they have a strong healing team. What are they likely to do in this situation?

MITRE ATT&CK framework helps us understand the enemy's process.

Instead of asking

> How did we get hacked?

MITRE ATT&CK framework reframes it as

> Where were we vulnerable in the attack chain?

This allows us to pinpoint which stage failed, strengthen defenses at that point, and reduce the chance or impact of similar attacks in the future.

If you can:

> Detect recon → you stop the attack early.

> Block persistence → you kick them out faster.

> Break command & control → the attacker is blind.

MITRE ATT&CK isn’t about trying to seem tough with military words.

It’s about mapping digital warfare into something humans can understand and defend against.

# Okay, Can You Explain the Actual Framework?

Sure I can, reader. In fact, I'll explain it like you're five!

### Imagine...

Someone wants to break into your house and steal your iPad (no more Minecraft).

They don't just magically teleport inside your house and teleport out with your iPad. They follow steps and procedures.

What will this most likely look like?

1.) Bad guy looks for a way to get into your house.

2.) Bad guy finds a good way in.

3.) Bad guy goes through your house trying to find your iPad, being careful of alarms and making too much noise.

4.) Bad guy locates the iPad and grabs it.

5.) Bad guy sneaks away with minimal to no evidence.

You can ask:

> How did he steal my iPad?

But that's too general. He could've done a lot of things to steal it, and you don't have a camera or evidence.

The better question to ask:

> What step did we mess up?

Did we forget to lock a window? Did we fail to notice the bad guy was hiding? Did we fail to hear the bad guy moving around the house? All of the above?

If we fix that specific step, the bad guy will have a **much** harder time trying to steal from us again.

MITRE ATT&CK sets you up for success, so that you fix your weaknesses and stop guessing.

# TL;DR

Bad guys follow plans.

MITRE ATT&CK shows us the picture of the plan so we can find out where our weakness was in their plan.

