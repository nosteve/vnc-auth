Nmap VNC Authentication Scanner
Steve Ocepek
socepek@trustwave.com

INTRODUCTION
============

Use this Nmap script to quickly determine the types of authentication supported
by each targeted VNC server. Particularly useful when probing large environments
for servers that do not require authentication.

Features include:

- Exceptional speed, thanks to the Nmap Scripting Engine.
- Support for all official authentication types 
- Support for both 3.3 and 3.8+ protocol versions
- Runs wherever Nmap can run (Windows, Mac, Linux, BSD, etc)

INSTALLATION
============

Simply copy the file to your local Nmap scripts directory, or the local
directory from which Nmap is being executed. An example, though this path
will vary between operating systems and distributions:

/usr/local/share/nmap/scripts/

USAGE
=====

Call the script using the --script Nmap argument.

Example: 

nmap -P0 --script=vnc-auth.nse -p 5900 192.168.2.166

Each discovered VNC server will be listed with its supported security type(s):

Starting Nmap 5.00 ( http://nmap.org ) at 2009-10-28 13:32 EDT
Interesting ports on 192.168.2.166:
PORT     STATE SERVICE
5900/tcp open  vnc
|_ vnc-auth: RFB 003.008, Security Types: 02(VNC Authentication)

Nmap done: 1 IP address (1 host up) scanned in 0.14 seconds

COPYRIGHT
=========

vnc-auth.nse - A VNC authentication scanner for Nmap
Created by Steve Ocepek
Copyright (C) 2009, 2010 Trustwave Holdings, Inc.
 
This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA  02111-1307, USA.
