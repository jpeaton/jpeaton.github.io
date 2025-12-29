---
layout: post
title: "ELIF #1 - Untangling .NET"
date: 2025-12-29
categories: [elif]
---

# Intro

In a vulnerability capacity, a common critical vulnerability you may come across involves a platform/runtime called .NET. I'm here to help you (and myself by writing this) understand its purpose and what it does so you understand why it's important to keep secure and updated. Specifically, I will use the CVE-2023-36049 vulnerability to explain how .NET can be insecure.

# What is .NET?

.NET is a **development platform** owned by Microsoft, and it's made up of three parts: a runtime (the thing that actually runs code), a framework/libraries (pre-built code developers rely on to build more things), and tools (for building and compiling apps).

**ELIF:**

Imagine your computer is a toy store. The applications on your computer are all toys. There's one problem: the toys can't work by themselves. They need things like batteries, instructions, and working/moving parts. 

.NET acts as the helpkit to make sure the toys work properly. It sits between your computer (the operating system) and the toys (applications), and it ensures that the toys work and behave as expected. Without it, the toy won't turn on or it has weird behavior.

Many toys in the store only know how to work if they have the helpkit. The nice part about it is that you don't really need to interact with the helpkit. The helpkit does its thing in the background, meaning the average user will never see or interact with it.

# .NET Runtime versus ASP.NET

The .NET runtime is the core execution engine, while ASP.NET is a web framework that runs on top of it. 

.NET runtime is used to run .NET applications. ASP.NET depends on it, and desktop apps that use .NET depend on it.

ASP.NET is simply the framework for web apps which is used to create Websites, Web APIs, and Microservices. It handles things like HTTP requests/responses, routing, authentication, and session handling.

**ELIF:**

.NET runtime is the brain, it makes sure the .NET programs run. Without it, no .NET programs really turn on.

ASP.NET is a website builder kit. It's used only to make websites and needs the brain (.NET runtime) to work.

# What happens if I uninstall .NET?

If .NET is uninstalled, any application (toy) that depends on .NET (helpkit) can no longer do so. This means the app either won't work, or will have irregular and unexpected behavior.

While Microsoft develops .NET and it comes included with Windows, most core Windows features don't depend on it. However, some built-in tools and many third-party programs do require .NET to function.

# .NET Security

.NET versions vary across organizations. Some may be on version 7, while the newest version is version 10. If an organization has a cadence for network scans on servers/machines, it may detect a vulnerable version of .NET. But what's vulnerable about it?

Well, it could be a slew of things. But for our purposes, we can look at a Privilege Escalation Vulnerability (CVE-2023-36049). According to Microsoft, an attacker could potentially inject arbitrary commands into a .NET app where the app then mishandles the input, allowing an attacker to write files, delete files, or overwrite files. This is due to the .NET runtime itself, not the apps.

**ELIF:**

Imagine a toy (application) in the toy store (computer) that writes notes to a notebook (input to a file). This toy follows instructions exactly as written. 

The toy expects instructions to follow such as:

> "Write this note in Notebook A"

The attacker may be able to sneak in hidden instructions inside this message, such as:

> "Write this note in Notebook A"
> "ALSO go rip pages out of Notebook B"

The toy doesn't realize those extra instructions snuck in, it just follows them blindly.

This is an attack that utilizes outdated versions of .NET to do things like:

1.) Create new files where they shouldn't exist
2.) Delete important files
3.) Overwrite configuration files (files that tell apps how to run)
4.) Break the app or make it behave dangerously
5.) Set up attacks for later

This vulnerability is in the .NET runtime itself, not just one app. Therefore, the best solution is to update the .NET runtime version to a newer one that has been patched by Microsoft.

I hope this helped!
