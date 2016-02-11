---
layout: post
title: Bioinformatics Microservices Part I
---

Following on from my previous post about why I think moving towards microservices
type designs will be beneficial to bioinformatics I want to discuss a project I am
currently working on and how I envision the different microservices fitting together
and why I'm going that route.

Like many bioinformaticians, I develop and work with analysis pipelines more than
pretty much anything I do. I'm also always eager to test out new frameworks, pipeline software,
and anything anyone else is doing. Recently I moved on from my Post-Doc where I was working
primarily on exome sequencing data from rare Mendelian diseases and to a full time position
in clinical bioinformatics. Now I am working up pipelines for processing targeted NGS
sequencing results in oncology molecular diagnostics. Speed is a key issue in order to
reduce turn around time and of course every single run needs to happen through a validated
NGS pipeline. These pipelines need to be version controlled (so previous historical
runs can be re-run exactly if needed) and every new version needs to be validated. Pipelines
can change over time and be improved, but they need to be stable in the sense of version
control. And this isn't trivial, other than minor tweaks like the number of CPUs to use
and memory configurations, etc, it really means every single aspect and command-line parameter,
the version of the command/binary/program, etc all need to be controlled. This is something that most
bioinformatics pipelines, as good as they are, don't really handle very well.
