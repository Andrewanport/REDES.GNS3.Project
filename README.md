# 📡 Computer Networks Project in GNS3

This project was developed for the **Computer Networks** course with the objective of creating and configuring a segmented network using the **GNS3** simulator. The network includes two subnets (LANs) connected by a router, simulating a practical environment for internal communication and routing.

---

## 📑 General Information

- **Program**: Internet Systems  
- **Course**: Computer Networks  
- **Semester**: 2024.2  

---

## 📋 Network Structure and Topology

### 🖧 Main Components
- **Router**: Connects and routes traffic between the two LANs.
- **Switches**: One switch per LAN, connecting the computers.
- **Computers**:
  - **LAN 1 (192.168.0.0/24)**: André, Keven, Breno
  - **LAN 2 (10.0.0.0/24)**: Lua, Pedro, Felipe

### 🌐 IP Addressing
- **LAN 1**:
  - IP Range: 192.168.0.x  
  - Subnet Mask: 255.255.255.0 (/24)  
  - Gateway: 192.168.0.254  
- **LAN 2**:
  - IP Range: 10.0.0.x  
  - Subnet Mask: 255.255.255.0 (/24)  
  - Gateway: 10.0.0.254  

---

## 🛠️ Configurations

### 📶 Router Configuration

bash
enable
configure terminal
# Interface connected to LAN 1
interface FastEthernet0/0
ip address 192.168.0.254 255.255.255.0
no shutdown
# Interface connected to LAN 2
interface FastEthernet1/0
ip address 10.0.0.254 255.255.255.0
no shutdown
# Enable routing
ip routing
end

### 🖥️ PC Configurations
  - LAN 1:
  - Andre
    ```bash
    set pcname ANDRE
    ip 192.168.0.2 255.255.255.0
    ip gateway 192.168.0.254

  - Keven
    ```bash
    set pcname KEVEN
    ip 192.168.0.3 255.255.255.0
    ip gateway 192.168.0.254

  - Breno
    ```bash
    set pcname BRENO
    ip 192.168.0.4 255.255.255.0
    ip gateway 192.168.0.254


- LAN 2:
  - Lua
    ```bash
    set pcname LUA
    ip 10.0.0.2 255.255.255.0
    ip gateway 10.0.0.254

  - Pedro
    ```bash
    set pcname PEDRO
    ip 10.0.0.3 255.255.255.0
    ip gateway 10.0.0.254

  - Felipe
    ```bash
    set pcname FELIPE
    ip 10.0.0.4 255.255.255.0
    ip gateway 10.0.0.254

## 🔗 For functionality tests and more information, access the link below:
[Click here! Complete Project.](https://www.canva.com/design/DAGX3s0q3LY/EZBiTtYRwA-u0GDSVbtDBg/view?utm_content=DAGX3s0q3LY&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h55a429acf4)
