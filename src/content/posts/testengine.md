---
title: "testengine: strategy games for club recruitment"
date: 2026-02-25
project: testengine
summary: building trading games for traders@uga
tags: [typescript]
---


testengine is a repo where I've been building a hub for multiplayer strategy/trading games.

## Inspiration

So the inspiration for this project was essentially trying to find a way for the people at Traders at UGA to reliably test the thinking of the applicants to our club. We took a lot of inspiration from Roblox, who sort of creates these online games for online assessments, which are like the first step in their job and internship application process. That's kind of what we wanted to do here. We also wanted a way to sort of play games with our members, as well as potentially open up gaming to potential applicants and just people that want to come to the club and learn about Traders at UGA and what we do. 

## Implementation

So the multiplayer server is built completely in Typescript. There are definitely plans to implement the server in a more performant language later on, but for now it's built in TypeScript and just uses a server and client node to sort of distribute and maintain a game state. 

## What's next

I have plans to add some more games so that we can have some more options in terms of what kind of games we can serve to our players. Also, the aforementioned engine updates. I'm also pretty interested in writing low-level code like C or Rust to compile to WebAssembly, which is a path we could take although it might be overkill for our use case.
