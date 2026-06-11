---
title: "I wrote an article for Software Design June 2026"
author: sivchari
date: 2026-06-10
tags: ["go", "mutation-testing", "software-design"]
categories: ["writing"]
draft: false
---

I wrote an article titled "Catching the pitfalls of AI-generated test code with Mutation Testing" as the first chapter of the second feature "How do you test code written by AI?" in [Software Design June 2026](https://gihyo.jp/magazine/SD/archive/2026/202606).

## How it came about

I had already talked about Mutation Testing and [gomu](https://github.com/sivchari/gomu), the Go implementation I built, at [Go Conference mini in Sendai 2026](/en/logs/sendai-go-2026/). Someone reached out after that talk, and that led to the article.

Writing a talk and writing a magazine article are quite different. Slides work because the speaker fills in the context in real time. An article has to stand alone, which meant writing out every background detail and reasoning I would normally say out loud. That turned out to be a different kind of hard work from preparing a presentation.

## Seeing your name in a magazine

Software Design is a magazine I have been reading since I was a student. It felt a little surreal to see my own name where I used to read other people's work.

Throughout the writing process I kept asking myself whether what I was writing was actually useful to readers and clear enough to follow on its own. Every round of review feedback reminded me how difficult it is to communicate technical ideas precisely. Now that it is done, I am simply glad I did it.

## What the article covers

The article starts from the problem that code coverage alone cannot guarantee test quality in an era where AI generates both code and tests. From there it walks through Mutation Testing as a technique, how gomu works under the hood, and how to integrate it into CI.

I hope you get a chance to read it in the issue itself.

## Closing

Thank you to the Sendai.go organizers for giving me the opportunity to speak, and to the Software Design editorial team for the invitation to write. I hope you enjoy the article.
