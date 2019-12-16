---
layout: default
title: Home
nav_order: 1
description: "The SDR Linux Distro for Raspberry Pi. Latest Software Defined Radio software pre-installed and ready to go."
permalink: /
---

# The SDR Linux Distro for Raspberry Pi
{: .fs-9 }

Modified Raspbian image with the latest SDR software pre-installed and ready to go. Compatible with every Raspberry Pi.
{: .fs-6 .fw-300 }

[Download Latest Version](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [View it on GitHub](https://github.com/luigifreitas/pisdr-image){: .btn .fs-5 .mb-4 .mb-md-0 }

---

The PiSDR is a Raspbian based operating system for the Raspberry Pi pre-loaded with multiple Software Defined Radio software. It was created to serve as a fast and reliable bootstrap for SDR projects.

---

## Support
This is a single person project with limited time and resources to acquire expensive SDRs. Only radios validated by tests are supported by this image. This is a limitation to maintain a certain level of quality. If you are a vendor and want your SDR supported by this image, consider donating one unit to the project.

### Software 
List of pre-installed software: SDR Angel, Soapy Remote, GQRX, GNURadio, LimeUtil, and LimeVNA.
#### Learn more [Pre-Installed Software](https://pisdr.luigifreitas.me/docs/software/software/index).

### Radios
We currently support the following SDRs: RTL-SDR, LimeSDR, PlutoSDR, Airspy, and Airspy HF.
#### Learn more [Supported Radios](https://pisdr.luigifreitas.me/docs/radios/radios/index).
 
### Computers
The latest version of the PiSDR (v3.0) supports every Raspberry Pi model (Zero, 1, 2, 3 and 4).

---

## Getting started

### Download
Since the download file is quite large, we created a poll of mirrors to ensure the fastest possible download. Click in the button below to be automatically redirected to the fastest mirror for you.

[Download Latest Version](https://rosetta.luigifreitas.me/public/pisdr/v2.1/pisdr_v2.1.tar.xz){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } 

#### Download Mirrors

| Status       | Server Location |Version  | TAR | ZIP |
|:-------------|:----------------|:--|:---|:----|
| Official | NYC | 2.1 | [Download](https://rosetta.luigifreitas.me/public/pisdr/v2.1/pisdr_v2.1.tar.xz) | [Download](https://rosetta.luigifreitas.me/public/pisdr/v2.1/pisdr_v2.1.zip) |
| [Collaborator](https://twitter.com/w4www_brian/status/1111335136929464320) | US-East | 2.1 | [Download](http://w4www.s3-us-east-2.amazonaws.com/pu4spy-pisdr/v2.1/pisdr_v2.1.tar.xz) | [Download](http://w4www.s3-us-east-2.amazonaws.com/pu4spy-pisdr/v2.1/pisdr_v2.1.zip) |
| [Collaborator](https://twitter.com/sam210723/status/1131846681916370945) | Singapore | 2.0 | [Download](https://vksdr.sgp1.digitaloceanspaces.com/PiSDR/pisdr_v2.tar.xz) | [Download](https://vksdr.sgp1.digitaloceanspaces.com/PiSDR/pisdr_v2.fixed.zip) | 

### Installation
The installation process is the same as the vanilla Raspbian. You will need a MicroSD card with at least 16GB of capacity. To transfer the image file to the memory card we recommend the open-source and multi-platform [balenaEtcher](https://www.balena.io/etcher/).

If you are feeling quite adventurous, you can copy the image to the memory card using `dd`. **Warning:** One should be extremely cautious using `dd`, as with any command of this kind it can destroy data irreversibly.
```bash
$ dd bs=4M if=pisdr_v3.0.img of=/dev/sdX conv=fsync
```
### Usage
This image can be used as a standard Raspbian desktop environment. The HDMI Output, SSH, and Remote VNC are enabled by default. For usage information about any pre-installed software, please refer to our [Software Page](https://pisdr.luigifreitas.me/docs/software/software/index).

**Warning: It is important to change the credentials after the first login to ensure your security.**

#### SSH
To access the system with this option, you will need an SSH client. This is built-in inside the Command-Line of most operating systems (Linux, macOS and Windows 10). As a GUI alternative,  we recommend using the PuTTY application available for Linux and Windows.

```bash
$ ssh pisdr@pisdr.local
Password: raspberry
```

#### VNC
The remote desktop can be accessed using any VNC client. The credentials are the same from the SSH. _Note: The Remmina Client is known to be incompatible with this VNC Server._

---

## About the project

PiSDR Project was created and maintained since 2019 by [Luigi F. Cruz](https://luigifreitas.me).

### Donation

Donations are welcome. Hit me up on [Twitter](https://twitter.com/luigifcruz) or [Email](mailto:luigifcruz@gmail.com) if you want to buy me a coffee.

### License

PiSDR is distributed by an [MIT license](https://raw.githubusercontent.com/luigifreitas/pisdr-image/master/LICENSE).

### Contributing

Everyone is very welcome to contribute to our project. Project icon made by [Smashicons](https://www.flaticon.com/authors/smashicons). 

#### Thank you to the contributors of PiSDR!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>