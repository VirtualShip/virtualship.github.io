---
layout: default
title: Commands
nav_order: 4
---

# Commands Guide
{: .fs-9 }

Learn and see how simple it is to issue commands in VirtualShip.
{: .fs-6 .fw-300 }

_Please note that all of the below commands work on any package, except when exceptions are listed_. 

# Order

As you learned (or will learn) in the Terminology Guide, an order is basically a command used to install a package. For example, if you wanted to install ```a52dec``` on your device, you would run:
```
ship order a52dec
```
This works for any package. There are no exceptions: the only thing that I need to mention is, that the following will not work:
```
ship order ship
```
For obvious reasons. Do not get this confused with refurbishing!

# Refurbish

This has no restrictions or exceptions whatsoever. Period. A refurbish is basically an update. For example, if you wanted to update ```a52dec``` to the newest version, you would run:
```
ship refurbish a52dec
```
Or, if you wanted to refurbish VirtualShip itself, you could run:
```
ship refurbish ship
```
And it will work! 

# Return

Another command available in VirtualShip is the return command. It is used to return a product: to uninstall a package. For example, if you wanted to uninstall ```a52dec```, you would run:
```
ship return a52dec
```
As with the order command, you cannot do the following:
```
ship return ship
```
Which also has obvious reasons why.

# Backorder

The backorder command in VirtualShip is similar to a request. It is used to request for a product that is _not in stock_ but you would like for it _to be in stock_. The backorder command creates an issue describing what product you want in stock. Note: before you issue a backorder command, be sure that:
* It is a product
* The product is not in stock
* The product is working
* The product has a stable release
* The product is not currently being worked on

When you have made sure of the above, you can then issue the command. For example, if you wanted ```ffmpeg``` to be in stock, you would type:
```
ship backorder ffmpeg
```
It will then ask for a description, in which case you might add:
```
Play, record, convert, and stream audio and video
```
