[ Attacker Machine ]
        ↓ ICMP traffic
[ Network Switch / LAN ]
        ↓
[ SOC Sensor (tshark) ]
        ↓
[ CSV Parser ]
        ↓
[ Analyzer (Python Counter) ]
        ↓
[ Alert Engine ]
        ↓
[ JSON / API Output ]


Security Logic :
Monitors ICMP traffic patterns
Identifies abnormal packet volume per IP
Generates structured alerts for SOC analysis


Detection Rule
IF packets_from_IP > THRESHOLD
THEN trigger alert
