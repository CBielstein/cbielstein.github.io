---
title: "Cameron Bielstein | APRS#"
date: 2021-06-14T23:09:52-07:00
draft: false
weight: 1
type: project
project_title: "APRS#"
project_short_title: "APRS#"
project_subtitle: "Digital packet radio encoder/decoder"
project_description: "A C# implementation of the APRS digital packet radio protocol used by amatuer radio operators."
project_summary: "APRS# is an encoder/decoder for the Automatic Packet Reporting System (APRS) digital packet radio protocol used by amateur radio operators around the world to exchange short messages, statuses, and locations."
collaborators:
    - name: "Edwin Mukhebi"
      url: "https://www.linkedin.com/in/edwin-mukhebi"
technologies: ["C#", ".NET Core", "GitHub Actions", "TCP Networking", "Packet Radio", "Amateur Radio"]
button_links:
    - link: "https://github.com/CBielstein/APRSsharp"
      img: "github.svg"
      text: "GitHub Repository"
---

## What is APRS?

The [Automatic Packet Reporting System](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System) (APRS) is both a digital packet radio protocol and the radio communication network used to transmit those messages.
Both the network and the protocol are used by [amateur (ham) radio](https://en.wikipedia.org/wiki/Amateur_radio) operators around the world to exchange messages, weather reports, locations, and more.

The APRS network is an ad-hoc, multihop, [mesh network](https://en.wikipedia.org/wiki/Mesh_networking) made up of radio transceivers ranging from repeating stations on mountain tops to personal handheld transmitters.
It is also backed by a network of "internet gateway" stations allowing internet-connected devices to send and receive messages from the radio waves.

APRS packets are encoded digital radio transmissions.
The packets carry an alphanumeric representation of information such as GPS location, weather readings, personal messages, identifying information, and more.
These packets are then [AX.25](https://en.wikipedia.org/wiki/AX.25) encoded, [frequency modulated](https://en.wikipedia.org/wiki/Frequency_modulation), and usually transmitted on [VHF](https://en.wikipedia.org/wiki/Very_high_frequency) amateur band radio frequencies.

## What is APRS#?

Currently under development, [APRS#](https://github.com/CBielstein/APRSsharp/) aims to create a modern set of tools for the APRS protocol. This includes a few primary objectives:

* Provide a modern encode/decode library for APRS packets for use in APRS software projects.
* Encode and decode packets from analog radios via hardware such as a [Terminal Node Controller](https://en.wikipedia.org/wiki/Terminal_node_controller), thus providing ham operators access to APRS communications without an expensive digital radio.
* Receive and decode packets supplied by the [Automatic Packet Reporting System-Internet Service](http://aprs-is.net/) (APRS-IS) to give hams and their software access to APRS communications without requiring a radio receiver.

Eventually, additional goals such as graphical user interfaces, web services, or more may be added to the project.

The project is cross-platform and runs on the open source [.NET Core](https://dotnet.microsoft.com/download/dotnet/3.1) framework.

## APRS# as a teaching tool

APRS# was submitted as a project for [InternLink 2020](http://web.archive.org/web/20210118044239/https://www.internlink.org/), a volunteer effort to replace internship and job opportunities for college students and recent graduates who lost opportunities due to the global COVID-19 pandemic.
Industry mentors with open source projects were paired with student or recent-graudate mentees to provide hands-on instruction in industry software engineering practices.

Through this program, [Edwin Mukhebi](https://www.linkedin.com/in/edwin-mukhebi) was matched with the APRS# project. Since he joined in 2020, he has contributed much of the initial code for the console application and interfacing with the APRS-IS backend.
