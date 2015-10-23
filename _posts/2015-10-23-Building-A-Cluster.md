---
layout: post
title: Building a Cluster
---

As part of my job as a Clinical Bioinformatician getting a Next-Generation
Sequencing-based Diagnostics test up and running I am designing and building the
small-scale computing cluster that we need to support this. Now we don't need a
tremendous amount of computing power since we are engaging in targeted sequencing
coming from Illumina MiSeq benchtop sequencers. Of course while the primary purpose
of this computing resource is to support clinical diagnostic needs, by purchasing
these sequencers in the hospital we will also be supporting research using the
equipment and research by other Faculty members who are new to NGS. As the sole
Bioinformatician in the hospital, and one of the few working on human genomics at
the University I tend to collaborate on a lot of diverse projects. So the cluster
needs to support that as well, with all clinical work receiving priority tasking.

_We had a few key things we needed out of our cluster:_

1. Small and cost-effective: We don't have a huge budget and we don't need a lot
2. Fast: Turn-around time is important so we need to maximize performance
3. Flexible: Lots of different workflows may be necessary
4. Lots of storage
5. Easy to support

Points 1 and 2 are a trade-off. The easiest way to get speed is to massively ramp
up the number of cores and nodes, but that can get expensive quickly. So we looked
for the CPUs that seemed to give us the best performance to cost ratio. Based on
that we selected the Intel Xeon E5-2620 processors. The clock speed of 2.40 GHz
is sufficient for all of our bioinformatics workflows. They have 6 logical cores
per processor (12 with hyperthreading) which is very good parallelization for the
price. Higher clockspeeds tend to get quite a bit more expensive, especially with
the same number of cores and vice-versa. We went with the new version 3 of these
chips as there are some significant speed-ups we can make use of from Intel
compiled versions of tools like BWA which should get us some speed-ups as well.

For RAM we went with 128GB per node. With full hyper-threading in play this gives
us 10GB of RAM per thread. While this is a lot more than what we need for most
amplicon-sequencing based workflows (2-4GB is generally sufficient depending on
the tool) but we will be supporting RNA-Seq data, exome sequencing data, and
whole genome data as well generated on sequencers from other locations, particularly
on a research basis.

These were the firm requirements we had. We also decided that for speed we really
wanted to be using 10 GbE within the cluster.

For storage we wanted to be able to get as many TBs as possible but at
economical prices while still having good performance. Enterprise storage can be
extremely expensive, especially if you are getting a solution that purports to
be scalable. Since this a health care setting, and we are in Canada, cloud computing
for the moment isn't on the table at all. Data needs to be local and our institution
wants to keep it in house. We don't know how long we will be required to retain
NGS data for, but worst-case scenario is the same length of time we need to keep
pathology reports and FFPE tissue-blocks which is roughly 20-25 years. Of course
we will turn over compute equipment several times over that time frame, but we wanted
lots of room to grow. Luckily for us a local company offers a really great storage
solution that fit our needs perfectly. <www.45drives.com> with their Storinator
product is absolutely fantastic, and they are only a few hours away by car. They started
out making this product for <www.backblaze.com> but are now doing their
own thing and selling it as a fully supported product. The Storinator is seeing increasing
usage in genomics centers and is hands down the most cost-effective and performant
device I've seen in this space. We went with the S45-Turbo solution. This means
fully populated with disks we can have 180TB, 270TB, or 360TB of storage per pod
depending on if we use 4TB, 6TB, or 8TB drives.

I'll talk a little bit more next time about the compute solution we selected and
some of my thoughts about rigging all of this up in a flexible way. We may go with
fairly standard HPC software or, I'm hoping, will move towards some newer solutions
like Apache Mesos.

Until next time.
