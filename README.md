# Nephthis-BP-VBO---Extended-General-Utility
VB actions to fill in gaps missing from OOB General Utility VBO

## DoEvents
Replacement for Sleep/Wait to not rely on system thread halts produced by long waits. Uses Now() differential to get around dilation skew provided by wait stage thread halts, which prevents usage of assumed ([total time waited]+=[wait time increment]) calculation.

May produce high CPU usage. If that's the case, change the wait interval.

Wait stage interval is essential, a high CPU usage issue will almost certainly be created without it.

### Inputs:
* Sleep Time (Seconds) - Number
* Wait interval - Number

## Convert Number to Binary Text
Converts a number to binary text

### Inputs:
* Number - Number
* Padding - Number

### Outputs:
* Binary Text - Text
