============
 dzen-tools
============

A couple of useful scripts that either aids using dzen or use it as the output device.

systat2dzen
===========

Monitors machine resources (and other things) using dzen as the output device:

* cpu utilization
* memory usage
* swap usage
* load (uptime, load 1m 5m 15m)
* network usage
* disk usage
* hostname, date/time
* battery
* imap email

How to use
----------

::

  $ systat2dzen -d sda | run_dzen_top

Config files
------------

* imap (type=json)

::

  $HOME/.systat2dzen/imap
  { "GMAIL": { "proto"   : "imaps",
               "hostname": "imap.gmail.com",
               "port"    : 993,
               "user"    : "e@ma.il",
               "password": "...",
               "folders" : ["INBOX", ...]
             }
  }

run_dzen
========

Scripts that aids positioning dzen at the edges of the screen (top or bottom).

How to use
----------

::

  $ run_dzen_top ...
  $ run_dzen_bottom ...
