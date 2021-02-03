# Bugs: 
## I. Speech Recognition: 
### I.1. Snowboy: 

1. "/usr/bin/ld: cannot find -lcblas": 
* Reason: ATLAS has not installed.
* Solution:
```
sudo add-apt-repository universe &\
sudo add-apt-repository main &\
sudo apt-get update &\
sudo apt-get install -y libatlas-base-dev liblapack-dev libblas-dev
```

2. "ImportError: attempted relative import with no known parent package": 
* Reason: Import syntax on the file **snowboydecoder.py** is out-of-date.
* Solution: 

Legacy code: 
```
from . import snowboydetect
```

Latest code: 
```
import snowboydetect
```

3. Could not run make (MINGNU32) on Windows for Snowboy source code:
* Reason: Snowboy only supports for **Unix-like** OS.
> Make: Requires **Makefile** defines set of tasks to be executed. In Snowboy source code, the **Makefile** defines set of tasks to generate the **snowboydetect.py** file.

## II. Ubuntu: 
1. "E: Could not get lock /var/lib/dpkg/lock-frontend": 
* Reason: Another process is using the resource.
* Solution: Terminate all WSLII processes or restart the Windows machine.
> **DBKG** (Debian Package) Low - level system tool to manage Debian - related files (.deb).

> **Ubuntu** vs. **Debian**: Ubuntu provides user a polished Linux distro, debian on the other hand, provide user a Linux distro based on free software. Ubuntu cares about user friendly, debian care about freedom.
