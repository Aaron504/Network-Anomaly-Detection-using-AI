# Network Anomaly Detection using AI
<p align="center">

  ![Screenshot 2025-05-16 231938](https://github.com/user-attachments/assets/a2bb61a2-f910-48f7-862c-74770a2b186c)

</p>

<h1>AI-Based Network Intrusion Detection with Gaussian Anomaly Detection</h1>
This project leverages AI to detect network intrusions and anomalies in packet traffic by applying Gaussian Anomaly Detection. Using a Windows VM hosted in Microsoft Azure, I captured and analyzed network packets with Wireshark, exported the data to CSV, and used a Python-based detection script to identify unusual traffic behavior.

The script models normal packet behavior using univariate Gaussian distribution, calculates the probability of each packet, and flags low-probability events as anomalies. A live graph visualizes probability scores against an anomaly threshold. Final results are saved as a labeled CSV file for further analysis or integration into a broader IDS system.



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Protocol (RDP) 
- Wireshark
- Python 3.11+ 

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- PHASE 1: Download a PCAP File
- PHASE 2: Set Up Python Libraries
- PHASE 3: Create and run the Python script (AI Gaussian Anomaly Detection)
- PHASE 4: Run the Script and Analyze Results

<h2>Deployment and Configuration Steps</h2>

-  PHASE 1: Download a Practice PCAP File
![Screenshot 2025-05-16 214722](https://github.com/user-attachments/assets/d312549b-b501-45fb-bb80-bb69d9bc4905)


- Phase 2: Set up Python Libraries
- This installs everything needed for:
- Reading your sample.csv
- Preprocessing the data
- Running Gaussian Anomaly Detection
- Visualizing anomalies

![Screenshot 2025-05-16 214524](https://github.com/user-attachments/assets/5999e03e-79e1-4dab-8246-6127705e872f)
![Screenshot 2025-05-16 214551](https://github.com/user-attachments/assets/745d7274-ad46-4201-9fc0-8a2a6c34c497)

- PHASE 3: Create the Python AI Gaussian Anomaly Detection Script
![Screenshot 2025-05-16 224126](https://github.com/user-attachments/assets/d474de56-878d-4faf-af4f-49ede3c80d3c)
![Screenshot 2025-05-16 224309](https://github.com/user-attachments/assets/fe7a8d3d-35f9-42d6-b746-84e0fd423568)

- Phase 4: Run the Script and analyze results

This Python script applies Gaussian Anomaly Detection (a statistical method using probability distribution) to detect unusual or malicious network traffic by analyzing features extracted from packet capture logs (e.g., packet size).

It works as follows:

- Loads network data from a CSV file (converted from .pcap using Wireshark)
- Extracts a relevant feature (packet length or frame.len)
- Normalizes the data so it's on a uniform scale
- Estimates Gaussian distribution parameters (mean and variance)
- Calculates the probability of each packet being "normal"
- Flags packets below a threshold as anomalies (potential intrusions)
- Visualizes results in a graph
- Exports results to a CSV file

![Screenshot 2025-05-16 225652](https://github.com/user-attachments/assets/e4168d8d-246a-474e-871f-08e55d3c8643)

The output graph has two key components:

- Blue Line → This shows the probability score of each packet.

- Higher values = "normal" traffic

- Lower values = more unusual

- Red Dashed Line → This is the anomaly threshold.

Any point below this line is flagged as anomalous

This allows you to visually detect spikes or dips in traffic that may represent malicious activity.

![Screenshot 2025-05-16 225732](https://github.com/user-attachments/assets/dd024301-52e2-43c6-8d25-b6449ae16b32)











