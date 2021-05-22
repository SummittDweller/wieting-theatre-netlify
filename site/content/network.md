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
<<<<<<< HEAD
| THEATRE | This is the SSID of the Wieting's internet connection and house network. | ?.?.?.? / 24 | Ethernet and wireless throughout the theatre. |
| MEDIA | Cinema system gigabit network for transfer of media/content. | 10.11.128.0 / 23 | Ethernet only in the Projection Booth |
| CONTROL | Cinema system network for systems control. | 10.0.0.0 / 24 | Ethernet only in the Projection Booth |
| EERO | Wireless only (SSIDs: 'WietingWiFi' and 'WietingGuest') for admins and guests. | 192.168.4.x / 24 | Wireless in the auditorium and south addition. |
=======
| NETGEAR | This is the Wieting's internet connection and house network. | ?.?.?.? / 24 | Ethernet and wireless throughout the theatre. |
| MEDIA | Cinema system gigabit network for transfer of media/content. | 10.11.128.0 / 23 | Ethernet only in the Projection Booth |
| CONTROL | Cinema system network for systems control. | 10.0.0.0 / 24 | Ethernet only in the Projection Booth |
| EERO | Wireless only connections for guests. | 192.168.4.x / 24 | Wireless in the auditorium and south addition. |
>>>>>>> 8b2208adb2f53ba27586e18af65afeefe351e6d0
| USB | Wired USB connections of limited length | Not applicable | Wherever the connected devices are. |
{{< /table >}}            


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

#### Examples

<<<<<<< HEAD
  - A `THEATRE` network cable running from device `B`, port 1, to an unidentifed port on device `F` will have a pair of labels marked `B.1 - THEATRE - F.x`.  At device `B` the `B.1` end of the label will be nearest the device, while at device `F` the `F.x` end will be nearest that device.
  - A `USB` cable running from an unidentified port on device `G` to an `In` port on device `P` will carry a pair of lables marked `G.x - USB - P.In`. 
=======
  - A `HOUSE` network cable running from device `B`, port 1, to an unidentifed port on device `F` will have a pair of labels marked `B.1 - HOUSE - F.x`.  At device `B` the `B.1` end of the label will be nearest the device, while at device `F` the `F.x` end will be nearest that device.
  - A `USB` cable running from and unidentified port on device `G` to an `In` port on device `P` will carry a pair of lables marked `G.x - USB - P.In`. 
>>>>>>> 8b2208adb2f53ba27586e18af65afeefe351e6d0
