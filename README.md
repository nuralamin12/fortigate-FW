# FortiGate Firewall on EVE-NG 🚀  

## 📌 Overview  
This repository provides a step-by-step guide for setting up **FortiGate Firewall on EVE-NG**, including **essential commands and useful links** to troubleshoot common issues.

---

## 🔹 EVE-NG Commands (Image Setup)  
```bash
mkdir /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
```
```bash
cd /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
```
```bash
mv fortios.qcow2 virtioa.qcow2
```
```bash
/opt/unetlab/wrappers/unl_wrapper -a fixpermissions
```
🔹 **FortiGate Initial Configuration**
**✅ Set Static IP on Port1**
```bash
config system interface
```
```bash
edit port1
```
```bash
set mode static
```
```bash
set ip <your-ip> <subnet-mask>
````
```
set allowaccess ping https ssh
```
```
end
```

**✅ Configure DNS**
```
config system DNS
```
```
set primary 8.8.8.8
```
```
end
```
**✅ Add a Default Route
**
```
config router static
```
```
edit 1
```
```
set device port1
```
```
set gateway <your-gateway-ip>
```
```
next
```
```
end
```
**🔹 Useful Links**

📌 FortiGate VM Download: https://lnkd.in/ev5k4rja
📌 EVE-NG Installation Guide: https://www.eve-ng.net/
📌 FortiGate Documentation: https://docs.fortinet.com/

