# fortigate-FW
 📌 Helpful Links  📌 FortiGate VM Download: https://support.fortinet.com/   📌 EVE-NG Installation Guide: https://www.eve-ng.net/   📌 FortiGate Documentation: https://docs.fortinet.com/  🚀 If you’re working with FortiGate + EVE-NG and need help, feel free to reach out! Let’s build a strong tech community together. 


I recently set up FortiGate Firewall on EVE-NG and wanted to share the steps, essential commands, and resources to help others who might be facing challenges during installation.
Here’s a quick guide to get FortiGate running in EVE-NG smoothly! 💡
🔹 📌 EVE-NG Commands (Image Setup)
1️⃣ Create a directory for FortiGate VM:
mkdir /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
cd /opt/unetlab/addons/qemu/fortinet-FGT-v7-build1262/
2️⃣ Rename the FortiGate image:
mv fortios.qcow2 virtioa.qcow2
3️⃣ Fix permissions:
/opt/unetlab/wrappers/unl_wrapper -a fixpermissions


🔹 📌 FortiGate Initial Configuration
✅ Set Static IP on Port1
config system interface
edit port1
set mode static
set ip <your-desired-ip> <subnet-mask>
set allowaccess ping https ssh
end
✅ Configure DNS
config system dns
set primary 8.8.8.8
end
✅ Add a Default Route
config router static
edit 1
set device port1
set gateway <your-gateway-ip>
next
end
🔹
