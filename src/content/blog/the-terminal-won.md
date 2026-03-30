---
title: 'The Terminal Won'
description: 'The same tool everyone thinks will replace computers is making me use mine more.'
pubDate: 'Mar 30 2026'
epistemicStatus: 'growing'
---

Let's start with an irony: for 40 years, the tech industry has spent millions to hide the terminal from people. Turns out the terminal is the right primitive when you add a "middle layer" automation between you and the raw machine. LLMs are great at text in, text out. LLMs are great at Unix tool calls. **LLMs hate inferring context from UIs.**

The biggest challenge when automating something with AI is to make something that can be **deterministic, debuggable and observable**. Tools like Claude Code or Codex solve this by grounding themselves in primitives that were time-hardened and are always reliable. They leverage the Unix philosophy instead of relying on an exotic interface: **boring commands that are stable, well-documented and composable.**

You will be *very* surprised at how many high-level tasks can be represented in those low-level building blocks. When you make this realization, it unlocks a lot of very interesting workflows that would have caused a huge overhead before.

An example of this is my relationship with launchd services. I had never used them prior to augmenting my workflow. They are very reliable scheduling services, they handle errors, they can retry, and they persist on restart when your laptop restarts.

Agents are very good at managing launchd. You don't need advanced knowledge of how the service works, you just need to know when it runs, when to cancel it, and its status. The fact that it uses typical primitives like exit statuses, observable right from the terminal, proves my earlier point.

Plumbing work in general has become such an easy part of these use cases. Setting up environments, installing dependencies, wiring services, this used to eat real hours, and my fellow developers can vouch for that. Now it's delegated. *Not* because I think the agent is smarter than me, but because **this work was always mechanical**. It used to be a niche that people specialized in and prided themselves on knowing. I don't remember everything I learned when setting up NGINX back in the day, although I do remember spending a lot of time debugging it. Now I can make an agent do it.

This work needs a text interface, but it doesn't need a UI representation of that text. That UI was meant to create a mental model for you, the user. LLMs don't need that.

There is a thick wall that is collapsing right now. On one side you had normal users who lived in user interfaces, their interaction with computers was mediated by apps that developers built. Things like Excel, Slack, Figma. On the other side you obviously have techies who use terminals and IDEs. Non-technical people can now interact with low-level systems using natural language, and developers don't need to care about low-level spec anymore. **Both sides are moving toward the middle.**

This can create interesting scenarios where:

- Joining a new team's toolchain can be fun instead of taking a full day following a stale README
- Doing market analysis and research using multiple data sources is faster and more efficient because you don't have to care about the UI, just the data
- Computers are more personal, workflows are more customizable and your machine actually adapts to how *you* work, not the other way around

All of this started because of a concept called product hacking. Non-technical people obviously don't want to use the terminal, but just like users were using Facebook groups to buy and sell things before Facebook made Facebook Marketplace, the same idea applies here. Non-technical people are using the terminal because they know it solves a real problem, especially in the automation scene.

This is a big opportunity for an AI-native product, a higher abstraction of the terminal. One that keeps the balance between an attractive UI and the agentic workflow underneath.

Computers are more fun to use now, *at least for me*. They are more approachable. I feel more encouraged to experiment with tools because I know I have this very smart companion as a fallback in case I mess up.

> It's quite ironic that the same technology everyone suspects will make us use computers less is the one that's making me use mine more.
