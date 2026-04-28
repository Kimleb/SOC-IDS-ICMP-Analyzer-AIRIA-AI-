Step-by-step guide

Step 1: Start tool
sudo python3 src/main.py

Step 2: Generate traffic

On attacker machine:

ping <target_ip> (eg ---> Ping 192.168.100.11)

Step 3: Review output

Check:

outputs/alert.json

Example Alert
{
  "alert_type": "Suspicious Network Activity",
  "indicator_value": "192.168.100.11",
  "packet_count": 77,
  "analyst_question": "Is this scanning activity or normal traffic?"
}
