# Building-A-Basic-Home-Lab
💡 What's a Home Lab?: Think of it as your digital workshop, a safe haven to tinker, test, and refine your cybersecurity skills. A Home Lab is a personalized setup where you can build virtual environments, play with cutting-edge tools, and simulate real-world scenarios, all from the comfort of your home. 🏠💡

## Getting Started with Your Home Lab Setup
**1. Choosing the Right Virtualization Software**
Before you start building your lab, you'll need to select a virtualization platform. VirtualBox is a free and versatile option, perfect for beginners and professionals alike. It allows you to create multiple isolated VMs on a single physical machine.


**2. Downloading and Installing VirtualBox**
- Navigate to VirtualBox.org and download the version compatible with your operating system.
- Follow the installation prompts. If a dependency such as Microsoft Visual C++ 2019 is missing, the installer will guide you to download and install the necessary components.
- Download both the appropriate VirtualBox Platform Packages and Extension Pack.

<img width="955" alt="image" src="https://github.com/user-attachments/assets/961dbc50-0fee-4152-9b28-3dff3fc5f775" />


**3. Downloading and Installing Windows 10**
- Go to the Microsoft Website where there is a link for downloading Windows 10
<img width="956" alt="image" src="https://github.com/user-attachments/assets/730d637d-5943-4461-9841-031d6350d8e6" />


**4. Setting Up Your First Virtual Machine (VM)**
Once VirtualBox is installed, it's time to set up your first VM:

- Open VirtualBox and click 'New'.
- Name your VM and select the type of operating system you plan to install, such as Windows 10.
- Choose the downloaded Windows.iso for the "ISO Image" section.
- Allocate resources such as RAM and CPU cores according to your hardware capabilities.
<img width="512" alt="image" src="https://github.com/user-attachments/assets/02c0f3de-ec75-49ce-805a-dbbf93167f87" />
<img width="511" alt="image" src="https://github.com/user-attachments/assets/30caac94-02bf-4ee8-9fb9-88112a6cfca6" />

**5. Installing and Configuring Kali Linux**
- For offensive security practices, download and set up a Kali Linux VM.
- Use the pre-built Kali Linux VM available on their official site for ease of installation.
- After downloading, click the linux file ended with ".vbox" extension.
- This will automatically create a virtual machine in the virtualbox dashboard.
<img width="958" alt="image" src="https://github.com/user-attachments/assets/c6b8b7cd-6e82-4e8e-b2e1-e2ae37d49306" />
<img width="512" alt="image" src="https://github.com/user-attachments/assets/e4462b34-19c0-4923-8912-c13d0415ac1e" />


## Proper VM Network Configuration
To ensure safe testing environments, especially when handling malware or testing security tools, proper network configuration is crucial. Here’s how to set up your VM network settings to minimize risks:

**VirtualBox Network Settings**
- Open VirtualBox, select your VM, and go to 'Settings' -> 'Network'.
- You’ll see various network options. Here’s how to use them:
  - NAT: Use when internet access is needed without exposing your real network.
  - Internal Network: Best for malware analysis; VMs can communicate with each other but not with the outside world.
  - Host-only Network: Allows network communication between host and VMs, but not to the internet.
  - Not Attached: Disconnects the VM from all networks, providing maximum security during high-risk testing.

## Scenario-Based Network Configuration
- **Scenario 1: Testing Tools with Internet Access**
  - Use the NAT setting. It provides Internet access and isolates your VM from the host's main network.
- **Scenario 2: Analyzing Malware**
  - Set the network to 'Internal' or 'Not Attached' to prevent any external communications. This isolates your VMs entirely, providing a secure environment for analyzing harmful software.

 
**Implementing Network Changes**
- For malware analysis, change the network setting to 'Internal Network'. Create a network name (e.g., 'TestNet'), and configure all VMs to this network.
- Ensure that each VM has a static IP address if using the 'Internal Network' setting, so they can communicate within their isolated network without risk to your main system.

## Final Thoughts
Your Home Lab is more than just a learning tool; it's a platform to push your cybersecurity skills to new heights, offering endless possibilities for growth and experimentation. Whether you're a seasoned professional or just starting out, the insights and hands-on experience gained from a Home Lab are invaluable.

<img width="958" alt="image" src="https://github.com/user-attachments/assets/01dd9019-c9ce-4b69-80ae-09ff57d7050f" />


