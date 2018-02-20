---
layout: post
title:  "What I'm working on - Feb 2018"
date:   2018-02-20 12:00:00 +0000
categories: work
summary: "What I'm doing at work and how I'm balancing two projects at once"
---
In a previous post I mentioned I'm going to be focusing on data stuff at work this quarter. This didn't go quite as smoothly as I hoped, and I'm now working across two teams. 60% of my time is spent with a team of developers building a data warehouse for GOV.UK content. The other 40% is working on a multidisciplinary team that is looking at how we measure GOV.UK as a whole.

# Job 1: Building a data warehouse
My 60% team is building a data warehouse - although I think we're using the term data warehouse a bit loosely. To me it brings to mind a single database that a team of analysts can use to answer business questions, but that's not quite what we're doing. We don't have a huge amount of capability in that area, and our immediate goal is to build tools to inform people who manage content about what's working well, what could be removed/archived, what's underperforming etc.

We're implementing a [STAR schema](https://en.wikipedia.org/wiki/Star_schema) to record multiple "facts" (data points) about individual pages on GOV.UK over time.

It looks like my role is going to be building an API layer that makes this data accessible. I think this will be quite interesting as GDS has recently put together some [API standards](https://www.gov.uk/guidance/gds-api-technical-and-data-standards), so there's an opportunity to do it well and make the data public.

I haven't thought about what this going to look like yet, but a couple of weeks ago I visited the Parliamentary Digital Service and saw some of what they're doing. All their new APIs are following the [odata standard](http://www.odata.org/), which makes them interoperable with business intelligence (BI) tools, so their analysts can mix and match their public data with user analytics to understand what users are looking for. This looked like magic to me and I really want to explore this further.

# Job 2: Establishing reproducible data pipelines
On my other team I'm looking at the whole data infrastructure more broadly and considering ways we can make it better. At the moment data is fragmented, difficult to use, and not widely accessible. A lot of things have been built piecemeal by different teams of developers, and there's also a machine learning pipeline in development, which I'm assuming will require a lot of domain knowledge to maintain and scale.

Realistically we can't solve all of the problems we have immediately. So the challenge for me has been to find technical problems I can work on that will move us in the right direction.

The thing I'm focusing on now is the way we extract, transform and load data across the platform (ETL). There are batch processing tasks that need to happen to keep things running, and there is a reporting function we need to be able to measure KPIs, which is mostly not automated at all.

[My plan](https://github.com/alphagov/app-performance-summary/blob/850b2fcb4023f3de26476c1ec2c499594753c78e/doc/adr/0002-use-luigi.md) is to explore [Luigi](https://github.com/spotify/luigi) as a way to standardise batch processing a bit, using some currently hard to extract KPIs as a proof of concept.

I've seen an excellent example of a data pipeline elsewhere in GDS that makes it possible to reuse processing steps, trace the provenance of figures through the pipeline, and test correctness at each step. I'm hoping to implement something similar to this, but I'm also worried about not being able to deliver something tangible that will stick around after the project ends in a few weeks.

# Dividing my attention between two teams
Working on two things has been really difficult, but it was my choice to work on both these things at once. At the beginning of the quarter I was only on the performance measurement team. I then changed teams because I wasn't confident that I could usefully contribute to this full time, as the only developer.

This traded one problem for another; more demands on my time and a lot of context switching. This really stressed me out to the point where I wasn't sleeping properly and I couldn't focus on things. Thankfully my managers have been flexible and supportive. My current plan for dealing with this is:

1. take a week off ⛱
2. split my time into two (consecutive) chunks and make sure everyone I work with knows my schedule
3. across both teams, focus on specific problem areas I can work on relatively independently (instead of rigidly sticking to a [Kanban process](http://kanbanblog.com/explained/))
