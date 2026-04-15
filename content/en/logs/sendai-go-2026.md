---
title: "I spoke at Go Conference mini in Sendai 2026"
date: 2026-02-21
tags: ["go", "conference", "sendai"]
categories: ["conference"]
draft: false
---

On February 21, 2026, [Go Conference mini in Sendai 2026](https://sendaigo.jp/) was held. I gave a talk titled "Who tests the Tests?" and also enjoyed the other sessions and the after-party as an attendee. It was a great experience, so I want to write down my thoughts on the overall atmosphere of the event, my own presentation, and the community interactions in Sendai.

## Sendai.go and Me

Sendai.go holds a special place in my heart. It was the very first offline conference I ever attended in person -- Go Conference mini 2022 Autumn IN SENDAI. I had been speaking at Go Conference since I was a student, but back then COVID was only just beginning to settle down, so all my talks had been online. Speaking offline added a sense of liveness that's hard to feel through a screen -- seeing people actually listening, reacting in real time. I remember how much fun that was.

The conversations I had and the connections people introduced me to at that event have continued through subsequent conferences and OSS activities to this day. Getting involved in organizing Go Conference, eventually becoming the main organizer, choosing "Ichigo Ichie" (once-in-a-lifetime encounter) as its theme, and starting my work as a maintainer of Kubernetes and Argo CD -- all of it traces back to that first step.

Coming back to that same origin point four years later in 2026, this time as a speaker, was a deeply meaningful experience for me.

## My Talk: Who tests the Tests?

In my session, I presented on Mutation Testing and [gomu](https://github.com/sivchari/gomu), an OSS tool I built to implement it for Go. The slides are available on [SpeakerDeck](https://speakerdeck.com/sivchari/who-tests-the-tests).

### What I Wanted to Convey

AI-driven code generation and test generation have been spreading rapidly in recent development workflows. Whether code is written by a human or by AI, the guardrail that ultimately ensures quality is CI, and at its core are tests. But "tests exist" and "tests perform meaningful verification" are two different things.

Code Coverage has long been used as the go-to metric for test quality. However, as Goodhart's Law states -- "when a measure becomes a target, it ceases to be a good measure" -- chasing coverage numbers leads to hollow tests that merely execute code paths without any assertions. When you delegate test generation to an AI agent, you can even end up with tests that call `t.Skip` and effectively verify nothing.

In my talk, I introduced Mutation Testing as an approach to "test the tests," explained how it works, walked through the implementation of gomu, and showed how to integrate it into CI.

After the talk, I received questions like "how do you start introducing this into an existing project?" and "at what granularity should it be applied?" -- it was clear that there is strong interest in putting Mutation Testing into practical use.

## A Talk That Stood Out: tobari

The talk that left the strongest impression on me at this conference was goccy's presentation on [tobari](https://github.com/goccy/tobari).

While my talk was about the quality of tests -- "are your tests performing meaningful verification?" -- tobari addresses coverage -- "which tests cover which parts of the code?" Both approach the same underlying question of "how do we trust CI and tests?" from different angles.

In an era where AI-generated tests are becoming the norm, we will need both test quality and coverage traceability. The fact that these two topics appeared side by side at the same conference felt symbolic of this transitional moment in the age of coding agents.

## Community Interactions in Sendai

As I mentioned at the beginning, Sendai.go is where I first attended an offline conference in 2022. Many of the people I met back then are still active in the community, and I was able to reconnect with them at the venue and the after-party at Sendai.go 2026.

In an era where online communication is the default, the value of moments where names, faces, and personalities come together in person has only grown. Local conferences like Sendai.go feel different from large-scale conferences in Tokyo -- the distance between people is shorter, the boundary between speakers and attendees is more relaxed, and there is a stronger sense of unity between the sessions and the after-party. I think it is wonderful that every attendee shares the common experience of having traveled all the way to Sendai simply because they love Go that much.

## Closing

I was able to return as a speaker in 2026 to the community I first attended in person in 2022. Being able to maintain these community relationships over the years, and continuing to meet so many people even after entering the workforce, is something I feel truly fortunate about.

Thank you to senoue, the organizing committee chair, and all the committee members, the sponsors, Cloudsmith Inc. for providing the venue, and everyone who came up to talk at the event. I truly appreciate it.

I look forward to seeing you all again in Sendai next time.
