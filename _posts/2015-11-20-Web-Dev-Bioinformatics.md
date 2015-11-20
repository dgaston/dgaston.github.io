---
layout: post
title: Web Development Tools and Bioinformatics
---

Over the last few years I have been doing a lot of experimentation and development
work (mostly unpublished) surrounding things like genomic pipelines and ways of
managing and exploring genomic level data (focused on rare variant analysis in humans).
While there are plenty of exceptional programs and tools out there for this (particularly
pipelines), we bioinformaticians do like to tinker and re-invent the wheel a lot. Sometimes
this is bad (I've been guilty of this in the past), and sometimes it isn't. We all also tend to come
at how to execute and configure things (again, particularly pipelines) in our own particular ways
so sometimes even the best software can be a chore for us to use, because some early step
just doesn't seem right to us.

This is one reason why I think we should follow a trend that has become a bit of a trend
in web design, which is the concept of microservices. I am by no means an expert, and suffice it
to say that you can learn much more about microservices elsewhere, but the general idea
is that instead of building monolithic programs we should build loosely coupled microservices
that can work together to form your application. These microservives should speak to each other
through APIs, meaning that you reduce the risk of internal changes to the service
breaking other parts of the application. These services can also be re-used again and
again in different applications. Microservices also should generally be small and focused. Do
one thing, and do it well basically.

For me I think this is a worthwhile ideal in Bioinformatics, although I understand that it
can sometimes be counter-productive from the sense of publishing. Of course we can always
develop applications and frameworks as microservices and publish them together as a collection.
The upside is that other people may want to only use selected services from your application instead of the whole
application. Developing as microservices should make this easier and more straightforward.
