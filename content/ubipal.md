---
title: "Cameron Bielstein | UbiPAL"
date: 2021-06-14T22:14:46-07:00
draft: false
weight: 0
project_title: "UbiPAL"
project_short_title: "UbiPAL"
project_subtitle: "Secure IoT platform"
project_description: "A decentralized IoT security platform with dynamic and human-readible access control language."
project_summary: "UbiPAL is an access control language and distributed system which extends the SecPAL policy assertion language to support dynamic environmental conditions in access control statements. The requirement for centralized rule servers is also removed, allowing the ubiquitous network to stay online through single-point failures via direct negotiation of access rights between devices. The project is the result of a master's thesis written at UT Austin"
collaborators:
    - name: "Robert F. Dickerson, PhD"
      link: "https://rfdickerson.github.io/"
technologies: ["C++", "Public-Key Cryptography", "Internet of Things", "Raspberry Pi"]
button_links:
    - link: "https://repositories.lib.utexas.edu/handle/2152/31851"
      img: "book.svg"
      text: "Publication"
    - link: "https://github.com/cbielstein/ubipal"
      img: "github.svg"
      text: "GitHub Repository"
---

## Project Summary

UbiPAL is a system for describing and enforcing access control for ubiquitous systems, known in popular terminology as the [Internet of Things](https://en.wikipedia.org/wiki/Internet_of_things) (IoT).
It provides both a human readable language for access rules and the secure system by which those rules are enforced.

UbiPAL is based on the pre-existing [SecPAL](https://en.wikipedia.org/wiki/SecPAL) system, which introduced human-readable access control rules while remaining provably secure.
To this system, UbiPAL added two key enhancements:

1. The ability for rules to be specified in terms of observed conditions in the real world (i.e. dynamic environmental conditions)
1. The ability to function without a single server arbitrating requests (i.e. decentralized access control)

These concepts are summarized below.
For full details, read the [full thesis paper](https://repositories.lib.utexas.edu/handle/2152/31851).

The name "UbiPAL" comes from **Ubi**quitous **P**olicy **A**ssertion **L**anguage.

### Dynamic Environmental Conditions

Digital access control policies are often encoded in strict lists of who may access which resource.
Consider how documents are shared over the internet; a list of people are granted the ability to view, some may be able to edit.
This system, with the addition of groups of users, has worked well in computing systems for decades.

However, as technologies like smart home devices bring software access control in to the real world, we realize human rules are much more likely to change and adapt to circumstance.
For example, I may wish to allow my dog walker to open my door at times when I am not home and I have requested their services but at no other times.
It would be insecure to allow them to open my door at all times and insufficient to disallow at all times.

SecPAL began to address human access control by constructing access rules in simple "human language" and including the ability to delegate authority.
UbiPAL expands upon that in a few ways for the "smart device" world of IoT:

1. Expand the language of conditions on assertions to include statements about the physical environment (in this example, "Cameron is away from home")
1. Allow a definition of trusted IoT devices which may satisfy certain conditions (such as, "Cameron's phone is an authority on Cameron's location," and "Cameron's calendar app is an authority on his schedule")
1. Define and implement the framework for these conditions to be verified in real time for each request

These together can allow users to author access control policies which properly encode the complexities of human expectations.

### Decentralized Access Control

In our era of cloud computing, applications are often run on centralized internet servers and data centers.
This is a simple and powerful model for many scenarios.
For ubiquitous computing (or IoT), a centralized access control server can become a single point of failure that brings the entire system to a standstill.
We often read news stories of a cloud outage locking people out of cars or interrupting "smart home" devices.
Even the best decentralized cloud systems require an active internet connection to the smart devices, which may not always be possible.

UbiPAL aims to solve this problem by allowing devices to communicate directly to negotiate access control between themselves without an additional intermediary.
This is implemented with [public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) and chains of delegated trust and identity similar to [the way trust is established on the internet](https://en.wikipedia.org/wiki/X.509).
Devices may construct a chain of certificates to demonstrate access pivileges or identity during access negotiations and eliminate the need for a single all-knowing access control server.

## Paper Abstract

The ubiquitous computing environment and modern trends in personal computing, such as body sensor networks and smart houses, create unique challenges in privacy and access control. Lack of centralized computing and the dynamic nature of human environments and access rules render most access control systems insufficient for this new category of systems. UbiPAL is an object-oriented communication framework for ubiquitous systems which provides secure communication and decentralized access control. UbiPAL uses a modified SecPAL implementation to provide reliable, ad hoc access control. The UbiPAL system uses cryptographically signed, publicly held namespace certificates and access control lists in the style of TLS certificates. This approach allows message authentication and authorization in an ad hoc, completely decentralized method while maintaining human readability of policy language. UbiPAL was implemented as a C++ library, made freely available at (1), and evaluated to have minimized overhead. Even on the slowest device evaluated, a Raspberry Pi, UbiPAL authentication and authorization adds less than 20 milliseconds to the delivery a message with a message overhead of 153 bytes. The UbiPAL programming model separates access policy from application programming and results in small amounts of code required from the application programmer, creating an accessible paradigm for programming ubiquitous computing systems.

Read the full thesis: [UbiPAL : secure messaging and access control for ubiquitous computing](https://repositories.lib.utexas.edu/handle/2152/31851)
