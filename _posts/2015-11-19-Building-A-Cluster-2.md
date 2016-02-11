---
layout: post
title: Building a Cluster Part 2
---

Last time I discussed a bit about the needs we had identified and outlines for supporting
next-generation sequencing in a clinical setting from a bioinformatics perspective.
I focused a bit at the end on the solution for storage we are using from <www.45drives.com>
based off of their Storinator product. We have three of the 4U units in-house now with some
drives on the way. The 10 GbE switch is also now in the data centre and other than that
we are just waiting on our compute solution to be delivered. For our compute option
we went with the Dell FX2 platform. The FX2 is an example of the recent trend of moving towards converged
architectures to simplify operations and generally reduce costs. This platform comes in a variety of
configurations and densities, we opted for the 4 node compute option with I/O aggregators
to simplify our networking. The 4 compute nodes themselves actually communicate over the backplane of the FX2,
meaning that communication between nodes doesn't need to go to the switch and back,
that is definitely one of the main advantages of the aggregator over the ethernet pass-through module
they offer, and the cost difference is pretty minimal. With the 10GbE between the storage nodes and compute, overall
we should have a blazing fast cluster.

Each node fits our requirements for CPU and RAM, and has a few TBs of local storage for
fast scratch, temporary files, genomics resources, etc.

Now it is all about planning the OS and how to hook everything up together in an
awesome cluster.
