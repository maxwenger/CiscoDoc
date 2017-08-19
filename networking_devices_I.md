# Networking Devices I

## What you need to know

* Describe the purpose and functions of various network devices.

* Select the components required to meet a network specification

* Describe the components required for network and internet communication.

* Interpret network diagrams

* Differentiate between LAN/WAN operation and features

## All you need is a router! Right?

Okay, okay, when you go into Best Buy and ask the man in the blue polo shirt that you need a router, he will happily lead you to the networking section. But that Super Turbo Triple Band Home Office Router 2000, is a little more then just a router.

Its actually a router, a switch, an access point, and a firewall.

In a large organizations, they are usually separate devices and all do very specific things.

So whats in your home router?

### Router

![router](/resources/network_icons/router.jpg)

This is the standard icon for a router.

A router is a pretty simple device, it takes packets from one network, does some magic, and sends it to another.

**A router forwards packets between networks.**

### Switch

![switch](/resources/network_icons/switch.jpg)

This is the standard icon for a switch.

If you look on the back of your home "router", you might see a few ethernet ports, this is the switch part of your home router.

The switch is "less smart" than a router. It cannot connect networks, but it can connect many devices to a single ethernet port on a router or another device.

**A switch makes one ethernet port into many.**

### Wireless Access Point

![access point](/resources/network_icons/accesspoint.jpg)

This is the standard icon for an access point.

An access point is the antenna part of your home router. It sends out radio signals to wirelessly connect devices to your network. This is the "Wi-Fi" part.

**An access point connects devices wirelessly to the network.**

### Firewall

![firewall](/resources/network_icons/firewall.jpg)

This is the icon for a firewall.

**A firewall secures your network.**

---

So as I hinted earlier, in large organizations, these are broken up into separate parts.

*But why?*

Because home routers suck enough at all of them to use something else when it really matters. *Reliability matters when networks are big!*

## Cisco IOS

Everything has an operating system, on Cisco devices, the OS is called **Internetwork Operating System (IOS)**. Not to be confused by the IOS on an iPhone (Cisco did it first), the **Cisco IOS is a collection of operating systems for Cisco devices.**

### Layers of an OS

As with many things in computers, the OS is also defined as a layer of abstractions. Blow are these layers broken down into their most common definitions.

* Shell
  * User interface, can be a command line or a GUI. Anything that talks with a human.
* Kernel
  * Below the shell, the kernel takes input from the shell and tells the hardware what to do.
* Hardware
  * The physical device.

### Memory in Cisco device

You have two types of memory in a device.
**Flash memory** and **ram**.

Flash memory is **persistent**. It stores the operating system and the saved configuration files, and saves the data between reboots. Flash is *large* but *slow*.

RAM is **not persistent**. RAM stores anything that the computer is currently working on, but is wiped when you turn the device off. RAM is *small* but *fast*

On the startup of a Cisco device, the IOS and configurations are loaded into RAM to improve the devices performance over accessing everything from flash memory.

### Considerations before updating IOS*

1. What models of routers and switches require upgrades?

    * Upgrades most commonly are to **add features** or **improve security**

1. Do the routers and switches have enough RAM and flash memory for the proposed IOS versions?

    * Have enough flash to store IOS, enough RAM to load IOS into RAM.

1. What features are required for the devices?

    * More important to have a stable network than the "latest and greatest"

### Connecting to a Cisco device

Most common ways to access a Cisco device:

* Console
  * Does not require internet access
  * Connects the Cisco device to your computers serial port through an RJ45.
  * Only access method that works on first startup
  * **Method used to preform an initial configuration of a router or a switch***
  * Device can be compromised if someone has access to console port (lock up yo' routers and switches)
* Telnet
  * Virtual Teletype (VTY) access methods
  * Requires an IP address and network access
  * Content is sent in plain text
* Secure Shell (SSH)
  * Virtual Teletype (VTY) access methods
  * Requires an IP address and network access
  * Stronger password authentacation
  * Encrypts traffic
  * **Use to keep user ID, passwords and session content private.***
* AUX port
  * Out-of-band connection
  * Console port through a phone line
