---
autogenerated: true
title: Spinnaker
redirect_from: /wiki/Spinnaker
layout: page
---

|                  |                                                                  |
|------------------|------------------------------------------------------------------|
| Summary:         | Device Adapter for FLIR cameras that use the Spinnaker interface |
| Available since: | 2019                                                             |

------------------------------------------------------------------------

The Spinnaker device adapter was created by
[CAIRN](https://www.cairn-research.co.uk).

## Installation

For Micro-Manager versions prior to 2021-03-08, download and install the
[Spinnaker driver from the CAIRN
website](https://www.cairn-research.co.uk/wp-content/uploads/2019/05/SpinnakerSDK_FULL_1.20.0.15_x64.exe).
For later Micro-Manager versions (both 1.4 and 2.0-gamma builds),
download and install a [Spinnaker V2
driver](https://meta.box.lenovo.com/v/link/view/a1995795ffba47dbbe45771477319cc3)
that supports VS2010 (currently, v2.0, 2.1, 2.2, and 2.3; 2.3 is
recommended). UPDATE: though it was expected that Micro-Manager would
work with all version 2 of Spinnaker, this does not appear to be the
case. Use version 2.3.0.77, which is available in the Spinnaker archive.

Follow the instructions in this [pdf on the CAIRN
website](https://www.cairn-research.co.uk/wp-content/uploads/2019/05/READ-ME-INSTALLATION.pdf).
Note that it is not needed to download 2.0-beta3-20181129, newer
versions of Micro-Manager (1.4 and 2.0) work as well, and already
include the file mmgr\_dal\_Spinnaker.dll.

RGB8 mode results in RGB images as of build 2021-03-08. BGRa8 mode
(preferred for RGB if your camera has it) is supported as of 2021-03-09.

