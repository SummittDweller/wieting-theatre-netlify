---
title: Network
draft: false
author: Mackenzie McFate
date: 2021-05-22T06:40:53-05:00
socialshare: false
weight: 80
---
<!--
menu:
  main:
    identifier: prices
    pre: dollar-sign
    weight: 200
-->

<hr/>

## Networks and Other Connections

The Wieting's systems are identified as follows:

{{<table "table table-striped table-bordered">}}
| System Name | Description | Addressing | Physical Locations |
| --- | --- | ---- | --- |
| THEATRE | This is the SSID of the Wieting's internet connection and house network. | 10.0.0.0 / 24 | Provides service to OPERATIONS and WEITING-WIFI/GUEST only. |
| OPERATIONS | Cinema system network for systems control. | 10.11.128.0 / 24 | Ethernet only in the Projection Booth |
| WEITING-WIFI | Wireless only via our EERO devices. | 192.168.4.x / 24 | Wireless in the auditorium and south addition. |
| WEITING-GUEST | Guest wireless only via our EERO devices. | 192.168.4.x / 24 | Wireless in the auditorium and south addition. |
| Others | All other names indicate connection types of limited length like `USB`, `OPTICAL-AUDIO`, `HDMI`, `SERIAL`, etc. | Not applicable | Wherever the connected devices are. |
| \*MEDIA | Cinema system gigabit network for transfer of media/content. | 10.0.0.0 / 23 | Ethernet only in the Projection Booth |
{{< /table >}}            

<!-- Notes from Andrew Peevler...

10.0.0.x = MEDIA Network
10.11.128.x = OPERATIONS network... everything cinema-related except MEDIA

Password for VNC to the GDC server is `gdcvnc`
VNC to the Christie projector should address 10.11.128.191 with a password of `cdsclub`

Problem:  When the iMac's ethernet connection is active, the iMac cannot access the internet!

-->

## Wieting Network Topology "Secret Decoder Ring"

{{<table "table table-striped table-bordered">}}
| Device Code | Description | Physical Location |
| --- | --- | --- |
| A | Thompson DCM476 Cable Modem from Mediacom | Projection Booth - Top of Audio Rack |
| B | NetGear 4-Port Wireless Router | Projection Booth - Top of Audio Rack |
| C | DGS-2208 8-Port Gigabit Switch | Projection Booth - Top of Audio Rack |
| D | NetGear ProSafe 8-Port Gigabit Switch | Projection Booth - Rear of Cinema Pedestal |
| E | JNIOR A-310 Programmable Logic Controller | Projection Booth - Rear of Cinema Pedestal |
| F | Simplex Grinnell Fire Alarm | Stage North |
{{< /table >}}            

### Cable Label Convention

Each end of a cable should be labeled following this convention:

  `DeviceCode.Port - Network or Cable Type - DeviceCode.Port`

Labels should be applied such that the `DeviceCode.Port` corresponding to a particular device is nearest that device.  This will require placing one of the labels "upside down". \*See the first example below for clarification.  

#### Examples

  - A `THEATRE` network cable running from device `B`, port 1, to an unidentified port on device `F` will have a pair of labels marked `B.1 - THEATRE - F.x`.  \*At device `B` the `B.1` end of the label should be nearest device `B`, while at device `F` the `F.x` end should be nearest the device.
  - A `USB` cable running from an unidentified port on device `G` to an `In` port on device `P` will carry a pair of lables marked `G.x - USB - P.In`.
  - An `HDMI` cable running from the `Out` port on device `T` to an `In` port on device `C` will be labeled `T.Out - HDMI - C.In`.
