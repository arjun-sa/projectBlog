---
title: "WisprClaw: UGAHacks 11"
date: 2026-02-25
project: wisprclaw
summary: how wisprclaw came to be
tags: [SwiftUI, agentic-ai]
---

A couple weeks ago I participated in a hackathon at UGA called UGAHacks and won Best Solo Hack. I built WisprClaw, a voice layer for agentic AI that allows you to seamlessly interface with an AI agent while you work. 

## Origins

WisprClaw is sort of an amalgamation of my ideas with AI assistants and voice interfaces. In the past I've built a bunch of voice interfaces for different apps and I thought of WisprClaw while messing around with OpenClaw, trying to figure out how to actually interface with it. WisprClaw is essentially what Siri could've been.

## Building

Building WisprClaw was actually pretty simple. An OpenAI STT model listens to your speech after you hit a hotkey and sends the transcription to OpenClaw, which I paired with Anthropic's Sonnet 4.5. Later I added support for LLMLingua, which is a token compression model that allows you to preserve semantic meaning while also saving tokens, which is especially useful if you ramble or use a lot of filler words when you're prompting your agent. I built it all on a UI written in Swift, which I tried to make as close to the MacOS native UI as possible to make it as if you're just using another feature of MacOS.

## What's next

It is really interesting what agentic AI can do. I was honestly surprised by that when I was building Wisprclaw because of how useful it seemed to be. But at the same time I'm not very interested in agentic AI. I had an interest at one point, but to be honest, all of these sort of security vulnerabilities and how sort of non-deterministic they can be have really sort of turned me off from the space. I think I may try to make a foray again into this area soon, but right now I'm occupied with other ideas. 

I do want to venture more into voice layers. I've had quite the history with these voice layers and building voice interfaces for different products. I think I would really like to try to build a Wispr Flow, but open source. I think the biggest problem there is just trying to beat OpenAI's whisper model at voice detection and semantic retrieval. I think that's a really interesting problem, and I think that I would want to do that at some point. I think I just need to learn more about sort of AI for audio and deep learning before I can dive into that. 