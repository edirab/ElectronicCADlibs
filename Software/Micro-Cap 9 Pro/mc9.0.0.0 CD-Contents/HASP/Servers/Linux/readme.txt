List of HASP License Manager Versions since 8.08 (November 2002)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This list includes improvements, bug fixes, and other 
relevant information. It is arranged in descending 
chronological order.


HASP LM Linux Version 8.30 (November 2004)
==========================

Requirements
------------

To run HASP License Manager 8.30, aksusbd Version 1.8 (or newer) is 
required. Ensure that the appropriate daemon is 
installed and running before launching the HASP LM.

New features
------------

HASP HL support. Can be used to monitor concurrent usage of 
HASP HL protected applications. 

Previously accessed HASP keys are displayed in the Aladdin Monitor. 
In earlier versions, keys were only displayed during an open
login session.

Supports network packets used by new client APIs 
(version 8.01 and up).

Supports new Aladdin Monitor requests (Version 1.4.1 and up) to speed up 
Aladdin Monitor performance.

Note
----

NHS_IP_LIMIT = <IPAddr>, <IPAddr>...

Specifies the range of stations which are allowed to access the currently 
activated HASP License Manager. The last byte entry may be specified as a 
range. Multiple entries should be separated by commas. The list may be 
split through several lines. The following wildcard (asterisk) byte combinations 
are valid: 4th only, 4th, 3rd or 4th, 3rd, 2nd. A netmask can be specified 
as the number of set bits from left to right (e.g. 10.0.0.0/8).

Example:
NHS_IP_LIMIT = 10.242.18-99,10.1.1.9/16  10.25.0.0/24,
               192.0.0.*,194.0.*.*,11.*.*.*,
               10.24.7.8-12/30, 10.24.2.17




V8.08 (HASP CD Rel 11.0)
========================

HASP LM Linux V8.08
====================

New features
------------

This is the first release of the HASP LM for Linux


Note
----

In the nhsrv.ini file the "10.1.1.1-3" (range) and "!10.1.1.1" (deny)
notations are not supported by LM 8.08.
A new notation is supported which allows specifying arbitrary subnet
masks: "10.1.1.1/24".
The "/24" specifies the number of one-bits (starting at the left) of
the subnet mask. E.g. "/24" defines a subnet mask of 255.255.255.0,
"/27" defines a subnet mask of 255.255.255.224.

For example:
To allow the LM to serve stations with the following range of
IP addresses: 10.24.3.8  - 10.24.3.15

   10    .    24    .     3    .     8
00001010   00011000   00000011   00001000  ==  10.24.3.8

00001010   00011000   00000011   00001111  ==  10.24.3.15
\                                    /
 \------------ 29 Bits -------------/

29 Bits are the same, meaning 10.24.3.8/29


Trademarks
----------
Aladdin Knowledge Systems Ltd. (c) 1985 - 2004. All rights reserved.
