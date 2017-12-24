---
layout: post
title:  "Contributing to open source is hard"
date:   2017-12-24 17:19:00 +0000
categories: open-source
---
This year I attempted to do [24 pull requests](https://24pullrequests.com):

> The idea is basically "Send 24 pull requests between December 1st and December 24th", encouraging developers to give back to open source with little gifts of code throughout December.

I don't spend much time on open source outside of my day job, but over xmas I've got a lot of free time so I thought it'd be a good thing to try.

In the end I only submitted 5 PRs, but it was an interesting challenge.

# How I found stuff to contribute to

24 pull requests suggests some repositories itself, but they tend to be very
popular libraries or large projects that require a lot of context to get started.

My ideal project to contribute to is small in scope, and easy to hack on:

- I should be able to figure out what it does from reading the [README](https://robots.thoughtbot.com/how-to-write-a-great-readme)
- I should be able to check it out and run tests without much effort

A lot of the projects 24 pull requests recommended were also very dev focused. Stuff that works with a particular web framework for example.
These tools were pretty boring to me because I didn't care about the
problem they're trying to solve.

I found more relevant projects by looking at what I already work on:

- I contributed to some tools I was already using
- I looked at the [dependency graph](https://help.github.com/articles/listing-the-packages-that-a-repository-depends-on/) for the projects I work on in my day job
- I looked through the projects in github's [discover repositories tab](https://github.com/dashboard/discover)

When evaluating a project I looked for reported issues that I could easily reproduce.
I ignored any projects that had no recent commits on the master branch, as I didn't want to work on anything that was unmaintained.

# What I learned
My motivation for completing this challenge faded pretty quickly.

Contributing to open source takes a lot of effort. The experience of contributing to a project for the first time generally sucks. It's much more rewarding to get more involved with a single project than to contribute to 24 of them.

As a first time contributor it's hard to know how to get started and what is worth doing. I started out by looking for small bugs and missing documentation, as this is the easiest way to contribute when I don't know the project well.

For the most part I got positive feedback from the people who merged my PRs, but one of my pull requests was closed without explanation, along with an issue I commented on. This is pretty frustrating, as is the opposite case where PRs/issues [stay open for years](https://twitter.com/PR_birthday_bot).

I think open source works best when people respect the work others are putting in. Each contribution demands some of the maintainer's time, but offers some of the contributor's time in return. I really like that github now encourage ["help wanted" labels](https://help.github.com/articles/helping-new-contributors-find-your-project-with-labels/) to help new contributors. More projects should use these!
