# 🖥️ Tiny11 in Docker Container

A Docker container solution for running Tiny11 with KVM acceleration, providing remote access via VNC and RDP.

# 🚀 Getting Started
Prerequisites
Docker installed
KVM enabled system
Administrative privileges
# 📦 Features
⚡ Run Tiny11 inside a Docker container
🔒 Secure with isolated environment
🖥️ Access via noVNC (web browser) or RDP
🚀 Fast virtualization using KVM (requires host support)
💾 Persistent storage using Docker volumes
# 🛠️ Requirements
Linux host with:
KVM enabled (/dev/kvm should exist)
Docker installed
Tiny11 ISO (for initial installation)
Modern web browser (for noVNC access)
# 🚀 Installation
### 1. Clone the Repository
```
git clone https://github.com/PixelPlayz69/windows10vm
```
### 2. Cd Into The File
```
cd windows10vm
```
### 3. Build The Docker
```
docker build -t windows10-vm .
```
### 4. Install ISO or Start Again
```
docker run -it --rm \
  --device /dev/kvm \
  -p 6080:6080 \
  -p 3389:3389 \
  -v windows_data:/data \
  -v windows_iso:/iso \
  windows10-vm
```
