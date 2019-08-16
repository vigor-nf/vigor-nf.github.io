---
layout: default
title: "Developing Formally Verified Middleboxes with Vigor"
---

# {{ page.title }}

We present the design and implementation of Vigor, a software stack and toolchain for building and running software middleboxes that are guaranteed to be correct, while providing competitive performance and preserving developer productivity. With Vigor, developers write the middlebox code (i.e., the software network function, or NF) in C atop a standard packet-processing framework, putting persistent state in data structures from a Vigor-provided library. Vigor then automatically verifies that the resulting software stack correctly implements a specification (written in Python).

Vigor has three points of novelty: NF developers need no verification expertise, and the verification process does not require their assistance (push-button verification); the entire software stack is verified, down to the hardware (full-stack verification); and verification can be done in a pay-as-you-go manner, i.e., instead of investing upfront a lot of time in writing and verifying a complete specification, one can specify one-off properties in a few lines of Python and verify them without concern for the rest.

We present five NFs written using Vigor---a NAT, a Maglev load balancer, a learning bridge, a firewall, and a traffic policer---that are guaranteed to satisfy standard RFC-derived specifications, be memory-safe, and not crash or hang. We show that they provide competitive performance.
