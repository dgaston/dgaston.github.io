---
layout: post
title: Minor (And Not So Minor) Annoyances in Bioinformatics. An Ongoing Saga
---

So today started out as a pretty frustrating morning due to random (not really random)
failure in some analysis pipelines on some data I am trying to work on for a collaborator.
The analysis has already taken far longer than expected for various reasons, some of
which are my fault, and some of which aren't. But given some of the issues that crop
up I was inspired to post a little bit of a vent concerning things that end up just annoying
me as a researcher in bioinformatics. Some of these are specific to today, some arent
but I am putting them all here today anyway. In some cases I may call out specific
software. In all cases I appreciate the work put into the tool by its developers. Often
it is a tool I use a lot. Sometimes it is a specific case where it is symptomatic of
larger issues in Bioinformatics software design. After all, if I thought the tool was
complete garbage I wouldn't care enough to vent about it (unless it was really widely
used and terrible, but thats something for other posts). Ok, so in no particular
order:

## Inflexible and overly restrictive parsers

This particular complaint is something I just ran into when running the whole
tuxedo suite on some data where I am doing something non-standard with non-standard
references. Working on some viral transcriptomics where I have created synthetic
genome and transcriptome references for the virus + human data, as both will be
present in the RNA-Seq data and we want to capture the whole system. And this
particular complaint is most frustrating when it happens while using a tool
that is in the middle of a longer tool chain. Often it necessitates changing something
about the reference data, which may necessitate going back and re-doing previous
steps. In this case it doesn't, it has just put the brakes on the analysis until I fix
the reference and re-run this particular step.

In this case it is cuffmerge and the FASTA reference. Why, in 2016, does the parser for
a widely used tool, require that all sequence containing lines in a FASTA record have the
same length? That is ridiculous. We have had pretty flexible FASTA parsers for longer
than cuffmerge was even a tool. Parsing FASTA isn't THAT hard, even if the records end up
being a bit non-standard.


This is an ongoing Saga of Rants... Stay Tuned
