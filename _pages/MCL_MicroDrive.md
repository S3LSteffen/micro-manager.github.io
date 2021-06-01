---
autogenerated: true
title: MCL MicroDrive
layout: page
---

<table>
<tr>
<td markdown="1">

**Summary:**

</td>
<td markdown="1">

Controls [Mad City Labs (MCL)](http://www.madcitylabs.com/) Micro-Drive™
XY stage

</td>
</tr>
<tr>
<td markdown="1">

**Author:**

</td>
<td markdown="1">

Mad City Labs

</td>
</tr>
<tr>
<td markdown="1">

**License:**

</td>
<td markdown="1">

BSD

</td>
</tr>
<tr>
<td markdown="1">

**Platforms:**

</td>
<td markdown="1">

Windows 7/8/10 (32 bit and 64 bit)

</td>
</tr>
<tr>
<td markdown="1">

**Devices:**

</td>
<td markdown="1">

XYStage

</td>
</tr>
<tr>
<td markdown="1" width=20%>

**Since version**

</td>
<td markdown="1">

1.2.36

</td>
</tr>
<tr>
<td markdown="1">

**Example Config File:**

</td>
<td markdown="1">

[Example Config File](Media:media/MMConfig_MCL_MicroDrive.cfg "wikilink")
(Sets up the Micro-Drive™ with the DemoCamera.)

</td>
</tr>
</table>

The MCL Micro-Drive™ controls the
[MicroStage](http://www.madcitylabs.com/microstage.html) series stage
devices.

The Micro-Drive™ is a USB enabled controller to be used with the
motorized MicroStage series offered by Mad City Labs. The Micro-Drive™
allows control and reading of encoder position with resolution of 20nm
and step-sizes down to 95nm. The MicroStage series can be used in
conjunction with [Mad City Labs](http://www.madcitylabs.com)
Nanopositioning systems for a complete positioning solution.

&lt;INCLUDE Note text="To correctly use the XY List feature, including
the "Calibrate" button, the positioning type must be set to "Absolute"
on the Device/Property Browser. However, "Calibrate" on the
Device/Property Browser (see below) calibrates correctly using either
absolute or relative positioning.😎"&gt;

The following properties are currently implemented in the Micro-Manager
MCL Micro-Drive&trade adapter:

<table>
<tr>
<th>

Property

</th>
<th>

Description

</th>
</tr>
<tr>
<td markdown="1">

<b>Position Type</b>

</td>
<td markdown="1">

Sets the positioning type as either absolute or relative positioning.
The default positioning type is relative.

</td>
</tr>
<tr>
<td markdown="1">

<b>Set Origin</b>

</td>
<td markdown="1">

Sets the current position as the origin by resetting the Micro-Drive™'s
encoders.

</td>
</tr>
<tr>
<td markdown="1">

<b>Return to Origin</b>

</td>
<td markdown="1">

Returns the MicroStage to the position defined as the origin.

</td>
</tr>
<tr>
<td markdown="1">

<b>Calibrate</b>

</td>
<td markdown="1">

Calibrates the Micro-Drive™ by moving the MicroStage to the X and Y
forward limits, setting this position as the origin, and returning the
MicroStage to the position it was when calibrate was selected. This
works exactly the same as the "Calibrate" button on the XY List but
allows for calibration when positioning type is selected as relative.

</td>
</tr>
</table>
