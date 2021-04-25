# Bugs: 
## I. Speech Recognition: 
### I.1. Snowboy: 

1. "/usr/bin/ld: cannot find -lcblas": 
* Reason: ATLAS has not installed.
* Solution:

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

### I.2. SpeechRecognition: 
1. "AttributeError: Could not find PyAudio; check installation": 
* Reason: Missing dependency **PyAudio**.
* Solution: 
```
sudo apt-get install portaudio19-dev python-all-dev python3-all-dev && pip install pyaudio
```

2. GCC: 
* Solution: 
```
sudo apt install build-essential && \ sudo apt-get install manpages-dev
```

3.  Unable to run speech_recognition script:
* Reason: 
- Inappropriate Python environment. PyAudio is only compatible with Python 2.7, 3.4, 3.5, and 3.6. [Reference](https://people.csail.mit.edu/hubert/pyaudio/#:%7E:text=Note%3A%20As%20of%20this%20update,4).
* Solution: Setup appropriate Python environment.

4. "OSError: libespeak.so.1: cannot open shared object file: No such file or directory": 
* Solution: 
```
sudo apt-get update && sudo apt-get install espeak
```
* [Reference](https://stackoverflow.com/questions/32499491/python-text-to-speech-using-pyttsx).

## II. Ubuntu: 
1. "E: Could not get lock /var/lib/dpkg/lock-frontend": 
* Reason: Another process is using the resource.
* Solution: 
- Solution 1: Terminate all WSLII processes or restart the Windows machine.
> **DBKG** (Debian Package) Low - level system tool to manage Debian - related files (.deb).

> **Ubuntu** vs. **Debian**: Ubuntu provides user a polished Linux distro, debian on the other hand, provide user a Linux distro based on free software. Ubuntu cares about user friendly, debian care about freedom.

 - Solution 2: Check & finish all install/download process.

- Solution 3: Restart terminal.

2. "Failed to install file: not supported": 
* Reason: Ubuntu Software is getting crazy:)
* Solution: Install using terminal
```
sudo dpkg -i <file name>.deb
```

3. "mpeg-4 aac decoder h.264 decoder are required to play the file": 
* Solution: 
```
sudo apt-get update &&\
sudo add-apt-repository multiverse &&\
sudo apt install ubuntu-restricted-extras
```

4. "Exclusivity flag on, cannot modify" - VLC: 
* Solution: Restart machine.

5. Can not stream video over network.
* Solution: [link]https://www.youtube.com/watch?v=g5yukRgfk5Y

### II.1. Netem: 
1. "Error: Qdisc not found. To create specify NLM_F_CREATE flag.": 
* Reason: There is no previous loss emulator to be changed.
* Solution: 
```
tc qdisc add dev [Network interface] root netem loss [Loss percentage]%
```

* Bonus: After using the above command, can use: 
```
tc qdisc change dev [Network interface] root netem loss [Loss percentage]%
```

## III. Kali Linux: 
1. "Failed to execute child process "dbus-lunch"": 
* Reason: Missing dependency **dbus-lunch**.
* Solution: 

Terminate Kali Linux process:
```
vncserver --kill :* &&\ 
kex kill &&\
kex stop
```

Install missing dependencies:
```
sudo apt-get update && sudo apt-get install -y dbus-x11
```

2. Can not connect to internet:
* Examples: ping google.com
* Solution: Restart machine.

## IV. Google Colab: 
1. "UnicodeDecodeError: 'utf-8' codec can't decode byte '0x...' in position ...: invalid start byte"
* Reason: Upload files from Windows environment (Host machine) to Google Drive (Cloud environment) might has some problems.
* Solution: Manually copy.

## V. Face recognition (face_recognition):
1. "CMake must be installed to build the following extensions: _dlib_pybind11": 
* Reason: Missing CMake.
* Solution: 
```
pip install cmake
```

2. Can not connect to host machine camera from VM: 
* Just connect, avoid error, & wait :) However, the performance is f*cking bad.

3. "ERROR: dlib-19.8.1-cp36-cp36m-win_amd64.whl is not a supported wheel on this platform": 
* Reason: Inappropriate Python version.
* Solution:
```
conda install python==3.6.12
```

4. Install "dlib" on Windows: 
```
python -m pip install https://files.pythonhosted.org/packages/0e/ce/f8a3cff33ac03a8219768f0...2d54bfcf
```

## VI. Java: 
1. "Could not find or load main class":
* Reason: Path name contains special characters.

## VII. Android Studio: 
1. Android Studio does not recognize physical device: 
* Solution: Run VM to "wake it up":)

2. Debug or application's behaviors does not make sence:
* Solution: Just rebuild the application.



