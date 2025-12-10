
# Scapy Commands Documentation

This file lists all Scapy commands used during the practical lab exercises, including packet sniffing, crafting, and filtering.

---

# Launch Scapy

```bash
# Switch to root user
sudo su

# Start Scapy interactive shell
scapy
```
# Basic Packet Sniffing
```bash
# Start sniffing on all interfaces (unfiltered)
sniff()

# Save captured packets
paro = _
paro.summary()
```

Generate traffic in a separate terminal:
ping google.com
Stop sniffing with Ctrl + C

#Interface-Specific Sniffing
```python
# Sniff on the internal bridge interface
sniff(iface="br-internal")

# Save and summarize captured packets
paro2 = _
paro2.summary()
```

Generate network traffic:
ping 10.6.6.1
Then visit in browser:
http://10.6.6.23

# Filtered Capture – ICMP Packets
```python
# Capture only ICMP packets, count = 5
sniff(iface="br-internal", filter="icmp", count=5)

# Save captured packets
paro3 = _
paro3.summary()
paro3[3]
```

Notes
_ is used to reference the last output in Scapy.
Always run Scapy with root privileges to avoid permission issues.
Use Ctrl + C to stop sniffing manually if not using count
