# 🖧 University IT Center & Department Network Design

A comprehensive network design for the newly constructed IT Center and Department buildings of the university. This project involves creating a structured computer network with efficient use of IP addressing and VLANs, ensuring secure and seamless connectivity for all devices and users.

---

## 📄 Project Overview

The network design includes:
- **IT Center**: Offices, meeting rooms, computer labs, and a media center with a total of 164 data points.
- **Department Block**: Lecture halls, staff rooms, labs, and offices with a total of 203 data points.

---

## 🎯 Objectives

1. Design and implement an IP-based network with optimum subnetting and VLANs using the address range: `10.20.0.0/16`.
2. Configure routers, switches, and WiFi access points for connectivity.
3. Implement security measures to restrict access between specific nodes.
4. Ensure dedicated printer access for staff in specific areas.

---

## 🔧 Key Features

- **Network Segmentation**: Efficient VLAN configuration to segregate traffic between IT Center and Department.
- **Restricted Access**:
  - Printers and resources are accessible only to their respective staff.
  - Segregation of staff and lab networks to prevent unauthorized access.
- **Wireless Connectivity**: WiFi access with secure configurations and limited user capacity.
- **Optimized Subnetting**: Allocation of IP ranges based on device and room requirements.

---

## 🛠️ Technologies Used

- **Subnetting**: Custom IP range assignments for devices.
- **VLANs**: Layer 2 and Layer 3 VLAN configurations for network segmentation.
- **Network Devices**:
  - Routers
  - Switches
  - Wireless Access Points
- **Security Protocols**: Restriction of inter-VLAN access.

---

## 🚀 Implementation Steps

1. **Subnet Creation**:
   - Allocated IP ranges for each VLAN based on data point requirements (e.g., `10.20.0.0/26` for Computer Lab 1 in IT Center).
   
2. **Router and Switch Configuration**:
   - Configured routers with unique names and passwords for secure access.
   - Created VLANs for each room and associated them with specific subnets.
   - Multilayer switches used for inter-VLAN routing where needed.

3. **Wireless Access Points**:
   - Assigned SSIDs and secure passwords for meeting rooms, lobby areas, and departmental zones.
   - Limited maximum users based on seating capacity.

4. **Device and Printer Access Restrictions**:
   - Configured VLANs to prevent cross-room access.
   - Restricted printer access to designated staff groups.

---

## 📜 Subnet Details

| VLAN Name                                | Subnet            | CIDR | Devices | Range               |
|------------------------------------------|-------------------|------|---------|---------------------|
| Computer Lab 1 (IT Center)               | 10.20.0.0/26      | 64   | 60      | 10.20.0.0-10.20.0.63 |
| Computer Vision and Machine Learning Lab | 10.20.1.0/26      | 64   | 50      | 10.20.1.0-10.20.1.63 |
| Digital Learning Media Center            | 10.20.2.0/26      | 64   | 30      | 10.20.2.0-10.20.2.63 |
| Staff Room (Department Block)            | 10.20.2.128/29    | 8    | 5       | 10.20.2.128-10.20.2.135 |

*(Full VLAN details are available in the project documentation.)*

---

## ⚙️ Configuration Highlights

1. **Router**:
   - Example Configuration:
     ```bash
     Router(config)# hostname Main_Router
     Router(config)# enable secret <password>
     ```

2. **Switch VLANs**:
   - Example VLAN Creation:
     ```bash
     Switch(config)# vlan 10
     Switch(config-vlan)# name "Staff_Room"
     Switch(config-vlan)# exit
     Switch(config)# interface vlan 10
     Switch(config-if)# ip address 10.20.2.128 255.255.255.248
     ```

3. **WiFi Access Point**:
   - Configured SSID and security:
     ```bash
     SSID: University_WiFi
     Password: <secure_password>
     Max Users: 40
     ```

---

## 🖼️ Network Diagrams

- **IT Center**:
  Includes computer labs, staff offices, and meeting rooms.
- **Department Block**:
  Includes labs, lecture halls, and the department office.

*(Refer to the attached diagrams for detailed layouts.)*

---

## 🤝 Contribution

Contributions are welcome!  
Feel free to fork this repository, make improvements, and submit a pull request.

---


## 📚 Additional Resources

For detailed device configurations and VLAN setups, see the full documentation provided in this repository.
