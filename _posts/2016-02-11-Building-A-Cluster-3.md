---
layout: post
title: Building a Cluster Part 3
---

It's been awhile and all of the cluster components are here and have been running
through burn-in at the datacentre for a few weeks. We had some minor hiccups
waiting on a power cable to come in for the CISCO 10G switch, because apparently
they had to use a power connection just different enough from all other computer equipment
that you need to buy theirs, and of course it was back-ordered.

I would also say that luckily the IT department has been handling things like networking,
I can administer a UNIX system just fine, but networking is not my forte at all. We
ran into a big of a snag as well to do with interoperability and configuration of the
CISCO switch for the cluster, and the Dell FX2 system. We are using the FN I/O Aggregators
on the Dell and all of the ports are configured as a single LAG, which created some issues
with dropout and collisions on our network traffic.

Hopefully everything will run smoothly now, and I just need to go to the data centre
and finish up basic OS installation and some other configuration issues. I have Ubuntu 14.04 LTS server
edition running on the FC630 nodes within the Dell FX2 chassis, and the 45 Drives
storage nodes came with Cent OS pre-installed, so I have left that on there for now.
I plan on experimenting with Rockstor on one of the 45 Drives nodes to test it out
and see how well it works. I'm also going to install Mesos on all of the nodes to test
that out as an alternative to more traditional HPC software.

Let's see how it goes.
