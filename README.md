# FortiGate Firewall on EVE-NG 🚀  

## 📌 Overview  
This repository provides a step-by-step guide for setting up **FortiGate Firewall on EVE-NG**, including **essential commands and useful links** to troubleshoot common issues.

---

## 🔹 EVE-NG Commands (Image Setup)  
```bash
mkdir /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
cd /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
mv fortios.qcow2 virtioa.qcow2
/opt/unetlab/wrappers/unl_wrapper -a fixpermissions
