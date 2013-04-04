Ruby getoptions Class
=====================

This is a ruby class used to process options provided in the command line

Introduction
------------

This simple class uses **optparse** module in conjuction with **json**
to process command line options.

**optparse** are specified in a `json` file 

Examples
--------

How to use this module:
```ruby

$: File.expand_path('path/to/getoptions/dir')

require 'getoptions'

args = GetOpts(ARGV, 'path/to/opts.json')

p args
```

En example of a `opts.json` file:
```json
{
	"domain": {
		"short": "-d",
		"long":  "--domain MANDATORY",
		"desc":  "Fully Qualified Domain Name",
		"value": null
		},

	"dns": {
		"short": "-n",
		"long":  "--nameservers MANDATORY",
		"desc":  "comma separated list of nameservers",
		"value": null
		},

	"verbose": {
		"short": "-v",
		"long":  "--verbose",
		"desc":  "Be verbose",
		"value": false
		}
}
```

Requires
--------

 * json
 * optparse

CopyLeft
---------

Copyleft (C) 2012 Emiliano Castagnari <ecastag@gmail.com> (a.k.a. Torian)
