---
title: "simulacra: Hacklytics: Golden Byte"
date: 2026-02-25
project: simulacra
summary: how I built simulacra and my thoughts on distributed system testing and simulation
tags: [typescript]
---

last weekend I participated in Hacklytics: Golden Byte where I built simulacra, a web based distributed systems simulator.

## Inspiration

I had been interested in distributed systems for some time and realized that there weren't many interactive ways to learn about them. I wanted to mess around with these systems and sort of be able to watch as they broke in real time and learned with hands-on experience what good and bad designs were. There wasn't really anything in the market that let me do that. Simulacra was my attempt at fixing that problem.

## Implementation

Simulacra is built entirely in TypeScript. I have been interested in engines and simulation engines for a little bit now. I decided to try to build something that was really responsive yet also pretty lightweight so that anyone could run it in their browser. Basically, most of the processing is done in the browser. You have a React UI that communicates with the TypeScript engine that sort of generates this data. Then it's all sent to a Node.js backend that sends your data immediately to a Databricks SQL database. From there, your data can be queried. There's a startup at this hackathon called Sphinx, and Sphinx creates these AI models that can understand, format, and reason from data. I sort of decided to tack on Sphinx there to allow Sphinx to learn about this data and try to get some insights from this data.

As an example, for my demo, the distributed system in the simulation had a big error, like an architectural error. Sphinx was able to detect that there was bad throughput in this one from these nodes and understand why that might be occurring. Sphinx was one of the ways that you could get insights into the data, but I also made a Prometheus integration because I really wanted this tool to be useful to industry people. I kind of envisioned it as a way for people to whiteboard and design these distributed systems and test on them very quickly without actually having to implement anything. Having the Prometheus integration was so that these people would be able to connect this with Prometheus and then look through Prometheus and watch as the system is under load and see what it would be like to actually have the system in production. 

## Challenges

I think a sort of interesting challenge I ran into here was that Simulacra sort of sits in this weird space between learning tool and industry useful tool. I was trying to, I think, when I was building, sort of ran into this problem where I wanted Simulacra to be very useful to people in the industry, and you can sort of see this in my implementation of Prometheus and stuff like that, where I sort of lost sight of what Simulacra actually was. I was really intending it to be, or, well, since I wanted it to be useful for people in the industry and stuff like that, I think I missed out on really capitalizing on the learning part, because I think the learning angle is the most optimal angle there. A TypeScript engine that is sort of simulating a distributed system is not going to be nearly as high fidelity as the alternatives from AWS or whatever, so I sort of realized this towards the tail end of when I was building this. Look, this simulator is not that accurate, so there is really not that much of a point in trying to make this as useful and as industry oriented as possible. At the end of the day, this is just a TypeScript engine. It will never be as good as a real simulator that is actually spinning up instances of these micro services and actually pumping structured data through them to watch as they fail. This will never be that, so by trying to make it that, I am actually narrowing my scope and worsening my piece of the pie that I could be taking.

I think for next time I really want to be thinking about what my product actually is and what users can benefit the most from it. By the time that I had sort of realized what this was or how I could frame Simulacra within the wider array of all these different simulators and different ways to test your distributed system, it was quite late in the process for building. I tried to twist my story a little bit and make it work for both, when really, if I had just hammered down on education, I think it would have been better. Maybe not necessarily winning a prize, but it would have been a more coherent project. 

## What's next

I'm still very interested in this sort of distributed system simulation space. I think a lot of this inspiration has come from this company named Antithesis, which is a startup that recently had a round that was led by Jane Street. I think this sort of testing area and validation of these systems is a really interesting area.

I want to try to expand, maybe not this project, but expand or build another project in this space. I'm thinking of building a very robust testing suite for the market exchange that we have at Traders@UGA. I'm also thinking about other things. I just recently got a Linux server set up in my apartment. I'm wondering what it would be like to spin up a Kafka instance on there and simulate that, and maybe I'm pretty interested in cruise control, which was a tool developed by LinkedIn to automate Kafka clusters. I want to mess around with that and see if I can make some contributions to that Github eventually, or even just gain a better understanding of Kafka and what this can do. Lots of ideas. Not sure where we will go as of yet. 