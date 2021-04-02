# Others:
## I. Set up Snowboy environment on Kali WSLII: 
```
sudo apt-get update &\
sudo apt-get install -y make swig g++ &\
sudo add-apt-repository universe &\
sudo add-apt-repository main &\
sudo apt-get install -y libatlas-base-dev liblapack-dev libblas-dev
```

## II. Libs/APIs definition:
### 1. CMake: 
* CMake is an open-source, cross-platform family of tools designed to build, test and package software.

### 2. Dlib: 
* Dlib is a modern C++ toolkit containing machine learning algorithms and tools for creating complex software in C++ to solve real world problems.

# Computer network:

## Day 1:

### I. Basic

* Network interface: A network interface is the point of interconnection between a computer and a private or public network.
* List all network interfaces.
```
ifconfig
```

* List all available TCP ports: 
- t: TCP.
- l: Listening.
- n: Use only numbers for ID.
```
netstat -tln
```

* Default gateway: IP address of the rounter in LAN.

### II. Virtual Private Server (VPS): 
#### II.1. Definition: 
* A physical server is seperated into several virtual machines (VPSs). 
#### II.2. Types:
1. Single-Server VPS: 
* A number of VPSs are hosted on one physical server. 
2. Cloud VPS:
* Many dedicated servers are pulled together to form a hardware cloud. The VPS can be stored across several physical servers. 
#### II.3. Advantages:
* Scalability(Only Cloud VPS).
* Increase securities.

## Day 2: 

### I. Network adapter: 
* Definition: Computer hardware + Network connection provider.
* Types: 
  - Wired network adapter.
  - Wireless network adapter.
E.g., NIC (Network Interface Card/Ethernet adapter).

### II. Commands: 
1. Check LAN IP address: 
* Solutions:
  - Solution 1: Check "Wireless LAN adapter Wi-Fi."
```
ipconfig
```

  - Solution 2: Wifi Settings.

2. Check default gateway IP address: 
* Definition: Default gateway, LAN DNS server or rounter are the same.
* Solution: Find "Network Connection Details"

# UNIX-like authentication/authorization: 
## I. Definitions:
* User environment: User variable environments

## II. Topics: 
1. su vs. su -:
* su - : Login shell + Switch user + Clean previous user's environment variables.
* su: Normal shell + Switch user.
