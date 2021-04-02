# Others:
## I. Set up Snowboy environment on Kali WSLII: 
```
sudo apt-get update &\
sudo apt-get install -y make swig g++ &\
sudo add-apt-repository universe &\
sudo add-apt-repository main &\
sudo apt-get install -y libatlas-base-dev liblapack-dev libblas-dev
```

# Computer network:

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

