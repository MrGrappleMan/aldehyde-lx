<div align="center">

# 🧪 Aldehyde-LX 
**The Bleeding Edge Bootable Container for Power Users**

[![GitHub User](https://img.shields.io/badge/Developer-MrGrappleMan-blue?style=for-the-badge&logo=github)](https://github.com/MrGrappleMan)
[![Image Type](https://img.shields.io/badge/Type-bootc-orange?style=for-the-badge&logo=linux)](https://github.com/containers/bootc)
[![Base](https://img.shields.io/badge/Base-Fedora_Layered-darkblue?style=for-the-badge&logo=fedora)](https://fedoraproject.org/)

---

### *Refined Performance. Rust-Powered Desktop. Total Efficiency.*
**Aldehyde-LX** is a specialized `bootc` image designed for the Ryzen 4000 series (4800H) architecture. 
It bridges the gap between high-performance workstations and 24/7 "Idler" efficiency.

</div>

---

## 🚀 Key Features

| Feature | Description |
| :--- | :--- |
| **🌌 COSMIC DE** | The next-gen Rust-based desktop environment by System76. Pre-packaged with productivity layouts and 4K assets. |
| **🏎️ Dynamic Tuning** | Custom `sysctl` arguments and `auto-cpufreq` to maximize the efficiency of the 8-core 4800H APU. |
| **🌐 Web Dev Alpha** | Shipped with **Google Chrome Canary** and the **Zen Browser** for those who live on the bleeding edge of web standards. |
| **🛠️ Remote Ops** | `mosh` for resilient mobile-to-desktop SSH and `preload` for predictive binary loading. |
| **🧹 Self-Healing Filesystem** | Automated BTRFS trimming and block-level deduplication to maintain SSD longevity and storage space. |

---

## 🛠️ Included Components

### **1. Desktop & Productivity**
* **COSMIC Desktop:** Rust-powered, modular, and lightning-fast.
* **4K Wallpaper Pack:** Curated high-resolution landscapes pre-installed in `/usr/share/backgrounds/aldehyde/`.
* **Zen Browser:** Optimized for privacy and performance with a native vertical tab workflow.

### **2. Performance & Kernel**
The image comes with a pre-configured `tuned-adm` profile and specific kernel cmdlines:
* `preempt=full` - For ultra-low desktop latency.
* `nvme_core.default_ps_max_latency_us=0` - To prevent NVMe drive stalling during high I/O.
* `auto-cpufreq` - Managed by a systemd service to balance thermals in Mini PC form factors.

### **3. The "Idler" Kit**
Perfect for systems that stay on 24/7 (Tailscale exit nodes, Snowflake relays, etc.):
* **Mosh:** Essential for Mumbai's varied network conditions; stay connected through IP switches.
* **BTRFS Dedupe:** Runs a weekly `duperemove` to clean up duplicate files from dev builds.
* **Tailscale:** Integrated hooks for seamless tailnet integration.

---

## 💾 Installation & Switching

Since **Aldehyde-LX** is a `bootc` image, you can rebase your existing atomic system (like Bazzite-DX) directly without a full reinstall.

### **Phase 1: Preparation**
Ensure your current system is backed up. Check your current deployment status:
```bash
bootc status
