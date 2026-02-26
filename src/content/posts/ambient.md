title: "ambient: kill time in vscode"
date: 2026-02-25
project: ambient
summary: how I built ambient
tags: [vscode]

Ambient is a VS Code extension that is essentially a way for you to kill time and distract yourself, or sort of entertain yourself, while staying "in context" so that you aren't clicking off VS Code while waiting for the AI tool you're using to finish generating the code. 

## Inspiration

Ambient was basically derived from a problem that I would have where I would go and instruct Claude Code to do something and then click off of VS Code and go do something else. Then, while I was doing this other thing, Claude Code would finish and I would not realize, and I would continue to do this other thing. By the time I realized, "Oh, wait, I was waiting for Claude Code," you know, time has gone by and I am just being less efficient while vibe coding. 

Writing this out, it does just seem like all I need to do was turn on some sort of notification for Claude Code so I could always jump back to whatever I was doing. I was also just wanting to make a VS Code extension, I guess. I was also pretty interested in Bloomberg TV at the time, and I wanted a way to watch Bloomberg TV in my VS Code. 

## Challenges

Bloomberg TV was honestly incredibly hard to get working inside of VS Code because the video and audio codecs were just not working at all with the VS Code video and audio format. That was pretty annoying. That's why Ambient does not let you listen to audio or give you the audio of the Bloomberg TV stream.

Apart from that, it was quite an easy extension to make. I also added other things like RSS feeds, Minesweeper, and 2048 to expand the feature list a bit. It was basically just a funny thought that I had that I was able to whip up with Claude Code very quickly. 