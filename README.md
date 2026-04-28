🛡 Mini SOC ICMP Intrusion Detection System

A lightweight Network Intrusion Detection System (NIDS) designed to capture, analyze, and detect anomalous ICMP traffic in real-time using tshark.

This project simulates a SOC monitoring pipeline, including traffic capture, anomaly detection, and alert generation.

🚀 Features

Live ICMP traffic capture using tshark

Source IP traffic analysis

Threshold-based anomaly detection

Automated alert generation (JSON)

SOC-style workflow pipeline

Modular Python architecture

Optional external API integration (Airia/Wazuh-ready)

🧠 Architecture
Network Traffic

      |
      
tshark Packet Capture

      |
CSV Conversion

      |
Traffic Analyzer (Counter Logic)

      |
Anomaly Detection Engine

      |
Alert Generator (JSON)

      |
SOC Output / API Integration


⚙️ Installation
1. Clone repository
git clone https://github.com/your-username/mini-soc-icmp-ids.git
cd mini-soc-icmp-ids

2. Install dependencies
pip install -r requirements.txt

3. Install system dependency
sudo apt install tshark -y

▶️ Usage

Run the full SOC pipeline:

sudo python3 src/main.py

📊 Output Files

After execution:

File	Purpose
traffic.pcap	Raw packet capture
traffic.csv	Structured packet data
alert.json	SOC alert output
🔍 Detection Logic

An alert is triggered when:

ICMP packets from a single IP > threshold


Example:

192.168.100.11: 77 packets → ALERT

🧪 Use Cases
SOC training environments
Cybersecurity labs
Network traffic analysis
Intrusion detection simulation
Blue team practice
