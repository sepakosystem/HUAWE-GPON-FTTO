
# HUAWE-GPON-FTTO Project  
Comprehensive FTTO network configuration for a 100-unit building using Huawei Access and Cisco devices for Core.

This repository contains detailed configurations for a Fiber-to-the-Office (FTTO) and (FTTH) network deployed in a 100-unit commercial building. The setup integrates Huawei OLTs, MDUs, and ONTs with Cisco switches to deliver high-speed internet, VoIP, IPTV, CCTV, and server services. The project ensures secure, scalable, and efficient network management with isolated VLANs and optimized traffic profiles.

---

## Features  
- **High-Speed Internet**: Delivered via VLAN 200 with dynamic bandwidth allocation.  
- **Reliable VoIP**: Fixed bandwidth for quality VoIP services on VLAN 300.  
- **Secure CCTV**: Dedicated VLAN 400 with prioritized traffic for 120 cameras.  
- **IPTV Streaming**: Multicast-enabled VLAN 600 for seamless video delivery.  
- **Server Management**: Isolated VLAN 500 for internal servers.  
- **Scalable Internetwork**: VLAN 900 for flexible expansion and ISP connectivity.  
- **Robust Security**: SSH access, strong passwords, and VLAN isolation.  

---

## Repository Structure  
- **`OLT HUAWEI 5608T.txt`**: Configuration for Huawei MA5608T OLT.  
- **`SWICH CISCO 3750.txt`**: Configuration for four Cisco 3750-12SS switches.  
- **`MDU HUAWEI 5626.txt`**: Configuration for Huawei MA5626 MDU (sample for one of 41 units).  
- **`ONT HG8245H.txt`**: Template configuration for Huawei HG8245H ONT (one of 100 units).  
- **`README.md`**: Project documentation (you're reading it!).  

---

## Devices and Services  
- **OLT**: 1x Huawei MA5608T with 2x GPFD cards and 2x MCUD1.  
- **MDUs**: 41x Huawei MA5626 (24 FE ports each).  
- **ONTs**: 100x Huawei HG8245H for residential units.  
- **Switches**: 4x Cisco 3750-12SS for core switching.  
- **Servers**: 4x HPE G10 for internal services.  
- **NVRs**: 2x Dahua for CCTV management.  
- **CCTV**: 120x Dahua cameras.  
- **ISP Uplink**: Carrier Ethernet for FTTH and SIP accounts.  

---

## VLANs and IP Subnets  
| VLAN | Service       | IP Subnet          |  
|------|---------------|--------------------|  
| 100  | Management    | 10.10.100.0/24     |  
| 200  | Internet      | 10.10.200.0/24     |  
| 300  | VoIP          | 10.10.300.0/24     |  
| 400  | CCTV          | 10.10.400.0/24     |  
| 500  | Server        | 10.10.500.0/24     |  
| 600  | IPTV          | 10.10.600.0/24     |  
| 900  | Internetwork  | 10.10.900.0/24     |  

---

## Usage Guide  
1. **Clone the repository**:  
   ```bash  
   git clone https://github.com/sepakosystem/HUAWE-GPON-FTTO.git  
   ```  
2. **Apply configurations**:  
   - **OLT**: Upload `OLT HUAWEI 5608T.txt` via console or management interface.  
   - **Switches**: Copy `SWICH CISCO 3750.txt` sections to each Cisco 3750 switch.  
   - **MDUs**: Adapt `MDU HUAWEI 5626.txt` for each of the 41 MDUs (update `sysname` and IPs).  
   - **ONTs**: Use `ONT HG8245H.txt` as a template for each HG8245H unit.  
3. **Verify**:  
   - Use `display current-configuration` on Huawei devices.  
   - Use `show running-config` on Cisco switches.  

---

## Prerequisites  
- Huawei MA5608T OLT with H805GPFD and H801MCUD1 boards.  
- Huawei MA5626 MDUs and HG8245H ONTs.  
- Cisco 3750-12SS switches.  
- Console or SSH access to all devices.  
- Basic understanding of GPON, VLANs, and network configuration.  

---

## Contributing  
Feel free to fork this repository and submit pull requests with improvements. Suggestions for optimizing VLANs, traffic profiles, or adding new services are welcome!  

---

## Contact  
- **GitHub**: [sepakosystem](https://github.com/sepakosystem)  
- **Email**: [sepakosystem@gmail.com]

---

## License  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.  

   
