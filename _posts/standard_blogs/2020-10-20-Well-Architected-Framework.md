---
layout: 	wAFPost
title:  	Well-Architected Framework
date:   	2020-10-20
categories: Posts
author: 	Jordan
permalink: 	/pineapple-octopus
---

## I know that I ended the last blog heavily suggesting that the next would be about the development of the blog and I know what you're thinking: it's all lies, they're not even square!!! But we were just notified yesterday by the Generation course I recently completed about an hour long 'Examples of a Well-Architected Framework' masterclass this morning from an AWS solutions architect so here's a lil' blog about it!

The main point that was echoed throughout this session was "just read the whitepapers" if you're going to be involved with the framework: from the people giving the requirements to the people building it and everyone in-between or who's involved in any of the meeting regarding it. They're (apparently) written to be nice to read and also contain links and things that will help you gain the knowledge required to make informed decisions about your framework that could be the difference that saves you a lot of time and money in the long run.

There are 5 pillars to the Well-Architected Framework which are the areas it will ensure your infrastructure is strong in if you follow the advice properly, and these are operational excellence, security, reliability, performance efficiency and cost optimisation. I'm not really going to talk anymore about these as concepts as it's all stuff I became familiar with for my AWS qualification, if you want to know more then click the description in the sidebar, but the main benefits are:

- It makes it easy to evolve and maintain the infrastructure in the future
- It's secure and will help you meet compliance requirements
  - use [AWS Artifact](https://aws.amazon.com/artifact/) for access and help regarding these
- It will allow you to robustly handle failure and continue providing for your customers
  - everything fails at some point, you may as well design it to bounce back quickly
- It will help you perform well and deliver a better experience to your customers
- It will help your infrastructure provide you the best value for your money

There's also a free Well-Architected tool available on AWS that makes it easy to go through and evaluate your existing framework, meaning that you don't need to be an expert or hire one to do it for you!

The bulk of this session was actually going over what actually happens in a business meeting to review the framework. This was broken down into the 3 steps as follows:

#### Prepare
The first step of anything that you want to do well is to plan how you're going to do it. To prepare for a Well-Architected Framework review, you first need to make sure that you've invited a mix of everyone involved, this includes everyone in the who's either giving requirements for, building or using the infrastructure as they'll all have different views on it as a whole and different priorities for what it should do well and ideally you want to satisfy as many of these as you can as early on as possible. It's also important to set the tone of the meeting as a safe space where negatives aren't bad things that everyone shouts at Kyle for, there will definitely be negatives in your framework and you should be open enough to discuss these productively to determine how to turn them into positives. The last point in the preparation stage is to do you homework, make sure you (and as many people in the meeting as possible) have read the white papers before hand and try to have an idea of what's going to be covered and what questions are going to come up so as much of this can be thought of and dealt with beforehand and not waste the precious little bit of concentration everyone has on thinking time.

#### Execute
You know those important people that were invited during your planning? Make sure they actually turn up and if for some reason a team doesn't show up/is late, you can always postpone the section of the meeting relating to them until they are available. Once the meeting is going, you need to be decisive and lead the meeting, not everyone is going to agree with every point so it's fine to compromise or just select the overall best option, you just need to move on at some point and don't want to spend the whole meeting on the first point. As well as moving it along, part of leading the review is also making sure everyone stays on track! You want to spend less time in meetings so everyone can spend more time doing their actual job.

#### Follow up
Once you've had the meeting, share the report with the stakeholders. There will be high risk issues in your existing infrastructure but that's ok, what isn't ok is pretending there aren't or playing them down and not actually dealing with them. No matter how much confidence you have in your infrastructure, it's only as strong as it actually is so you need to be honest about how strong that is and how you can use the Well-Architected Framework to develop an improvement plan with your stakeholders.

It is the AWS Well-Architected Framework, but it isn't just limited to AWS! It was written with AWS in mind though so while you're free to use it while using other systems, you may need to do some extra research into the tools and AWS specific things that it suggests.

