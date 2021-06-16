---
title: "Cameron Bielstein | UbiPAL"
date: 2021-06-14T22:14:46-07:00
draft: false
weight: 0
project_title: "UbiPAL"
project_short_title: "UbiPAL"
project_subtitle: "Secure IoT platform"
project_description: "A decentralized IoT security platform with dynamic and human-readible access control language."
project_summary: "UbiPAL is the result of a master's thesis written at UT Austin. The project extended the SecPAL policy assertion language to support dynamic environmental conditions in access control statements. The requirement for centralized rule servers is also removed, allowing the ubiquitous network to stay online through single-point failures via direct negotiation of access rights between devices."
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

UbiPAL is a secure platform and access control policy language for ubiquitous computing, also known as the [Internet of Things](https://en.wikipedia.org/wiki/Internet_of_things) (IoT).

Based on the existing [SecPAL](https://en.wikipedia.org/wiki/SecPAL) language, UbiPAL introduced two key enhancements:

1. Addition of dynamic environmental conditions in security policies
1. Removed requirement for any authoritative access control server

For more details, read the summaries below or read the [full paper](https://repositories.lib.utexas.edu/handle/2152/31851).

The name "UbiPAL" comes from **Ubi**quitous **P**olicy **A**ssertion **L**anguage.

### Dynamic Environmental Conditions in Access Control

Often, digital access control policies are encoded in authoritative lists of who may access which resource.
Access is either granted to or withheld from groups or individuals at all times.
However, human "access control" is often much more subjective and dynamic.
For example, I may wish to allow my dog walker to open my front door only at times when they are scheduled to walk my dog and if I am not currently at home.
It would be insecure to allow them to open my door at all times and insufficient to disallow at all times.

UbiPAL expands upon the SecPAL assertion language to add such dynamic rules through two additions to the language:

1. Expand the language of conditions on assertions to include statements about the physical environment (e.g. "Cameron is not home")
1. Allow a definition of trusted IoT devices which may satisfy the condition (e.g. "Is Cameron not home?")

### Decentralized Access Control

In our era of cloud computing, applications are often run in centralized internet servers for convenience.
This is a simple and powerful model for many scenarios.
For ubiquitous computing (or IoT), a centralized access control server can become a single point of failure that brings the entire system to a standstill.
Even a decentralized system that is off-site can fall prey to an outage with an internet service provider.

UbiPAL aims to solve that problem by allowing individual devices to negotiate access control between themselves with a centralized server.
This is achieved through [public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) and securely signed and privately exchanged policy assertions.
Devices or applications may collect a chain of assertions to present as evidence of their access privileges when challenged.
In this way, access control can continue in the face of network or other failures.

## Paper Abstract

The ubiquitous computing environment and modern trends in personal computing, such as body sensor networks and smart houses, create unique challenges in privacy and access control. Lack of centralized computing and the dynamic nature of human environments and access rules render most access control systems insufficient for this new category of systems. UbiPAL is an object-oriented communication framework for ubiquitous systems which provides secure communication and decentralized access control. UbiPAL uses a modified SecPAL implementation to provide reliable, ad hoc access control. The UbiPAL system uses cryptographically signed, publicly held namespace certificates and access control lists in the style of TLS certificates. This approach allows message authentication and authorization in an ad hoc, completely decentralized method while maintaining human readability of policy language. UbiPAL was implemented as a C++ library, made freely available at (1), and evaluated to have minimized overhead. Even on the slowest device evaluated, a Raspberry Pi, UbiPAL authentication and authorization adds less than 20 milliseconds to the delivery a message with a message overhead of 153 bytes. The UbiPAL programming model separates access policy from application programming and results in small amounts of code required from the application programmer, creating an accessible paradigm for programming ubiquitous computing systems.
