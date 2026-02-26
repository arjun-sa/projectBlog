title: "EduMate: Claude Builder Hackathon at UGA"
date: 2026-02-25
project: EduMate
summary: how I built EduMate
tags: [SwiftUI]
---

EduMate is an interactive learning tool that allows students to talk to a tutor to explain concepts and be quizzed/lectured out loud.

## Inspiration

The concept for EduMate came to me when I was driving from Atlanta to Athens. I had a midterm coming up, and I really wish that there's some way for me to study in the car while speaking. There's this concept of being able to enhance your understanding of something by explaining it to someone else. That's the kind of method that I wanted to use to sort of verify my understanding of my midterm concepts.

## Implementation

EduMate is built on a Swift front end with a Python back end that processes the speech and sends it to an Ollama model. I wanted to make it a local model so that EduMate can be used without Wi-Fi. I also implemented a RAG system within this or with this Ollama model so that you can give EduMate your class material and it can pull directly from there to ask you questions and stuff like that.
There are two different modes in EduMate:
- A sort of quiz mode where EduMate can quiz you aloud and ask you to explain certain concepts.
- A lecture mode where EduMate can sort of just talk to you and explain the different concepts in your material to you in different ways so that you can understand it better.

## What's next

A little bit after I built EduMate, I was thinking about building a sort of AI classmate that would be able to sit in your lectures, listen to the lectures, and take notes, as well as talk to you about the lecture material. I guess maybe this would be more of an extension of EduMate, but it would just be able to have a more robust memory. With this mode, it would allow it to remember more relevant information from your lecture, and also you wouldn't necessarily need to give it lecture notes or anything. It would just be able to remember and pull things from the lecture, and even just remind you of different things, maybe the professor said X is on this test; then you can go and review this material. 