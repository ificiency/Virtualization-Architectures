DEPLOYMENT OF A 5G MOBILE NETWORK


Overview

This project provides a hands-on demonstration of deploying a 5G mobile network using Free5GC and Docker. The setup includes critical 5G core network functions (NFs) such as AMF, SMF, NRF, and UPF, as well as a simulated User Equipment (UE) and gNodeB (gNB). The project is designed for exploring and understanding the 5G architecture, network slicing, and security configurations.


Features

5G Core Deployment: Includes all core network functions required for a 5G setup using Free5GC.

Network Slicing: Demonstrates configuration and operation of multiple network slices with distinct SST and SD.

Security Parameters: Configures integrity and ciphering algorithms for secure communication.

Traffic Analysis: Enables attachment of a UE, traffic capture, and protocol analysis.

Dockerized Setup: Simplifies deployment with Docker and Docker Compose.



Prerequisites

Operating System: Linux or Windows with WSL2.




Tools and Dependencies:

Docker Engine

Docker Compose

Free5GC-compatible kernel module: gtp5g




Installation

Clone the Repository:


git clone https://github.com/yourusername/5g-mobile-network-deployment.git

cd 5g-mobile-network-deployment



Install Required Tools: Follow the official guides to install Docker Engine, Docker Compose, and the gtp5g kernel module.



Configure Free5GC:

1. Download and configure the free5gc-compose repository.
2. Modify configuration files (e.g., nssfcfg.yaml, amfcfg.yaml) as needed for PLMN ID, network slices, and security parameters.




Usage

Deploy 5G Core Network: Use the provided Docker Compose file to deploy all 5G core network functions:

docker-compose up -d




Verify Deployment: Access the WebUI to confirm the network functions are running:

URL: http://<server_ip>:<port>



Provision and Attach UE:

Use the WebUI to provision a UE with its SUPI and configuration details.

Initiate the attachment procedure for the UE to the core network.




Capture and Analyze Traffic:

Use tools like Wireshark to capture and analyze traffic during the UE attachment process.

Code Structure

docker-compose.yml: Configuration file for deploying the 5G core network.

config/: Contains configuration files for Free5GC components.

logs/: Stores application logs for analysis.




Example Output

Network Slice Configuration:

Slice 1: SST = 1, SD = 010203
Slice 2: SST = 2, SD = 000001



Traffic Logs:

UE Attached: SUPI = imsi-208930000000001
Integrity Algorithm: NIA2
Ciphering Algorithm: NEA0



Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: git checkout -b feature-branch.
3. Commit changes: git commit -m "Add new feature".
4. Push to the branch: git push origin feature-branch.
5. Open a Pull Request.




License

This project is licensed under the MIT License. See the LICENSE file for details.



Acknowledgments

Special thanks to the Free5GC community and the contributors of open-source tools and libraries used in this project.