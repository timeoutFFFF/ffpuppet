FFPuppet
=======

[![Build Status](https://api.travis-ci.org/MozillaSecurity/ffpuppet.svg)](https://travis-ci.org/MozillaSecurity/ffpuppet)
[![Coverage Status](https://coveralls.io/repos/github/MozillaSecurity/ffpuppet/badge.svg)](https://coveralls.io/github/MozillaSecurity/ffpuppet)
[![Build status](https://ci.appveyor.com/api/projects/status/7r1sx0iad8wksfmw/branch/master?svg=true)](https://ci.appveyor.com/project/tysmith/ffpuppet/branch/master)

FFPuppet is a python module that automates browser process related tasks to aid in fuzzing.

Installation
------------

At this time no modules are required to run FFPuppet however some features may not be available.

##### Installing python modules
  
    pip install requirements.txt

Linux requires xvfb in order to run headless.

##### Ubuntu

    apt-get install xvfb


Usage
-----
```
usage: ffpuppet.py [-h] [-e] [-l LOG] [-m MEMORY] [-p PREFS] [-P PROFILE]
                   [--safe-mode] [-t TIMEOUT] [-u URL] [--valgrind] [--windbg]
                   [--xvfb]
                   binary

Firefox launcher/wrapper

positional arguments:
  binary                Firefox binary to execute

optional arguments:
  -h, --help            show this help message and exit
  -e, --extension       Install the fuzzPriv extension (specify path to
                        funfuzz/dom/extension)
  -l LOG, --log LOG     log file name
  -m MEMORY, --memory MEMORY
                        Process memory limit in MBs (Requires psutil)
  -p PREFS, --prefs PREFS
                        prefs.js file to use
  -P PROFILE, --profile PROFILE
                        Profile to use. A temporary profile is generated by
                        default.
  --safe-mode           Launch browser in 'safe-mode'. WARNING: Launching in
                        safe mode blocks with a dialog that must be dismissed
                        manually.
  -t TIMEOUT, --timeout TIMEOUT
                        Number of seconds to wait for the browser to become
                        responsive after launching. (default: 300)
  -u URL, --url URL     Server URL or local file to load.
  --valgrind            Use valgrind
  --windbg              Collect crash log with WinDBG (Windows only)
  --xvfb                Use xvfb (Linux only)
```
