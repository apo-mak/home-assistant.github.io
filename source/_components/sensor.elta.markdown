---
layout: page
title: ELTA Sensor
description: "Instructions on how to set up Elta sensors within Home Assistant."
date: 2017-02-05 08:00
sidebar: true
comments: false
sharing: true
footer: true
logo: http://www.elta.gr/Portals/0/elta.jpg
ha_category: Sensor
ha_release: 0.39
---

The `elta` platform allows you to track deliveries by the [Hellenic Postal Service (ELTA)](https://www.elta.gr/en-us/home.aspx).
Track ELTA Hellenic Post Packages on your dashboard get Origin (limited)/destinations(full) tracking information

To enable this sensor, add the following lines to your `configuration.yaml`:

```yaml
# Example configuration.yaml entry
c_Elta:
    code: YOUR_TRACKING_CODE
```

Configuration options for the ELTA Sensor:

- **code** (*Required*): The tracking code of the pacage.

The ELTA platform will only accept tracking code in the below format.
Two letters followed by nine numbers and ending with two letters (total thirteen characters).

ELTA Hellenic Post number rules :  ( # Letter, * Digit, ! Letter Or Digit )
  ( R# *** *** *** GR )   ( V# *** *** *** GR )
  ( A# *** *** *** GR )   ( C# *** *** *** GR )
  ( E# *** *** *** GR )   ( L# *** *** *** GR )
  ( N# *** *** *** GR )   ( I# *** *** *** GR )

Troubleshooting:
The tracking number has to end in “GR” or have destination country Greece.

If the tracking code does not meet the above format, there will be log entry in this format.
Invalid key YOUR_TRACKING_CODE . Key must be 13 characters.


<p class='note warning'>
The ELTA sensor is in BETA and currently only show tracking from ELTA.
</p>
