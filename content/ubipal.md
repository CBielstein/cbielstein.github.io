---
title: "Ubipal"
date: 2021-06-14T22:14:46-07:00
draft: true
weight: 1
project_title: "UbiPAL"
project_short_title: "UbiPAL"
project_subtitle: "Secure IoT platform"
project_description: "A decentralized IoT security platform with dynamic and human-readible access control language."
project_summary: "UbiPAL is the result of a master's thesis written at UT Austin. The project extended the SecPAL policy assertion language to support dynamic, environmental conditions in policy assertions. The requirement for centralized rule servers is also removed, allowing the ubiquitous network to stay online through single-point failures through direct negotiation of access rights between devices."
collaborators:
    - name: "Robert F. Dickerson, PhD"
      link: "https://rfdickerson.github.io/"
technologies: ["C++", "Public Key Cryptography", "Internet of Things", "Raspberry Pi"]
button_links:
    - link: "https://repositories.lib.utexas.edu/handle/2152/31851"
      img: "book.svg"
      text: "Publication"
    - link: "https://github.com/cbielstein/ubipal"
      img: "github.svg"
      text: "GitHub Repository"
---

**Paper abstract**: The ubiquitous computing environment and modern trends in personal computing, such as body sensor networks and smart houses, create unique challenges in privacy and access control. Lack of centralized computing and the dynamic nature of human environments and access rules render most access control systems insufficient for this new category of systems. UbiPAL is an object-oriented communication framework for ubiquitous systems which provides secure communication and decentralized access control. UbiPAL uses a modified SecPAL implementation to provide reliable, ad hoc access control. The UbiPAL system uses cryptographically signed, publicly held namespace certificates and access control lists in the style of TLS certificates. This approach allows message authentication and authorization in an ad hoc, completely decentralized method while maintaining human readability of policy language. UbiPAL was implemented as a C++ library, made freely available at (1), and evaluated to have minimized overhead. Even on the slowest device evaluated, a Raspberry Pi, UbiPAL authentication and authorization adds less than 20 milliseconds to the delivery a message with a message overhead of 153 bytes. The UbiPAL programming model separates access policy from application programming and results in small amounts of code required from the application programmer, creating an accessible paradigm for programming ubiquitous computing systems.
