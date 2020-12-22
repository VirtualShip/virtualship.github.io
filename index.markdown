---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
nav_order: 1
---

# The package manager for Mac OS
{: .fs-9 }

VirtualShip offers a quick, easy, one-stop solution to all of your Mac OS package needs.
{: .fs-6 .fw-300 }

[Get started now](#quickstart){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [View it on GitHub](https://github.com/VirtualShip/Core){: .btn .fs-5 .mb-4 .mb-md-0 }

## Quickstart

### Dependencies

VirtualShip is designed to be very lightweight and uses the least number of dependencies as possible. The only things you need extra of a bash shell are:
* curl
* gh

```curl``` comes prepackaged with Mac OS, so you should disregard that as a dependency. Also, the binary of ```gh``` is installed with VirtualShip, so you can disregard that as well. What do we have here? No dependencies!

### Installation

With VirtualShip, installation is quick and easy. Copy the following code into your Mac Terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/VirtualShip/Core/main/.install)"
```
This command runs a script called ```.install``` in your terminal, which installs VirtualShip for you. Once the script is finished, try installing something with VirtualShip now!
