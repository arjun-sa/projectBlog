---
title: "cyprus: my first linux server"
date: 2026-03-03
project: cyprus
summary: a whole new world of linux fun
tags: [linux]
---

Today I finally got all the tools and parts together to get my very first Linux server up and running. I'm calling it cyprus. I have a ton of plans and ideas for this server, and I cannot wait to get started with them. 

## How did I get a server?

So many years ago, my dad got a server. When he first got it, I was pretty interested in it and what it could do, but he never really let me play with it because I was probably 10 years old, so the server kind of sat for a while and eventually I lost interest in it. 

Recently I came across this server while looking through the basement, where my parents have a bunch of stuff. I was able to pull this server out, dust it off, and get all the parts for it to get it running again. That meant getting a new power cable and a new SSD to boot an operating system onto, to make it a bit faster and stuff like that. Over the last month or two, I've been slowly procuring these parts, and recently I finally got the last thing I needed, which was a Wi-Fi adapter, because the Ethernet wiring in this apartment kind of sucks.

The Wi-Fi adapter was actually a pain to get running because I had to download an open source driver from GitHub because Linux isn't supported by the manufacturer. That was pretty interesting, and honestly it turned out to be pretty easy, but it definitely brought me back to my childhood, back when debugging an open source thing running on your computer, you had to dig through GitHub issues and random forums and all sorts of stuff to figure out how to fix your issue or get something working. It really makes you glad, I guess, that AI is a thing now, but also, in a way, I sort of miss it. I read this somewhere, but there is something about going on the quest for knowledge and putting in the effort to procure knowledge that makes it all so much more fulfilling and so much more meaningful.

These days, when you can just ask ChatGPT to do anything for you, it kind of takes that away from you. It takes that sort of effort, that quest, away from you. While it's definitely convenient to have this sort of unlimited access to information, I think newer generations, people who didn't have to fight and struggle in the pursuit of knowledge, have a different idea of what seeking knowledge actually means.

## What's next?

The main project right now is to spin up a Kafka cluster on the server. This is mainly for my own understanding of how Kafka works in sort of production-grade systems. I want to have a Kafka cluster and then run something like Cruise Control on it, which is a repo created by LinkedIn. It's an open-source automation tool for Kafka.

Once I've got both of those running, I want to create a test environment for it and maybe stress test Kafka + Cruise control. I'm thinking about setting up a data pipeline that automatically backs up any files from my MacBook when I'm at home. How this might work is that the files get sent to the Kafka cluster, which obviously isn't exactly a real world use case of kafka but I just want to set up the data pipeline anyway and see how this would work with real-world data. I guess I'll send the files through the Kafka cluster, and then they would be downloaded onto the server as a backup.

So far, that's my idea, but I've got lots of different stuff. I think eventually I would want to do the whole port forwarding thing and get my server actually up on the internet and maybe host some things or do stuff like that. Right now I don't really want to touch all that stuff because I am just not that well versed in networking, and I do not want to add my server to a botnet. 
