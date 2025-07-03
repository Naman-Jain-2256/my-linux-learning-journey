# 🐧 Installing Linux — Complete Beginner’s Guide

This guide walks you through installing Linux using:

- 🖥️ Native Installation (Bootable USB)
- 💻 Virtual Machines (VM)
- 🪟 Windows Subsystem for Linux (WSL)

---

## ✅ Option 1: Native Installation (Dual Boot or Full Install)

### 🔹 Step 1: Choose a Linux Distribution

Popular choices:

- **Ubuntu** – Most beginner-friendly
- **Fedora** – Great for developers
- **Debian** – Stable and reliable
- **Kali Linux** – For ethical hacking & cybersecurity
- **Arch Linux** – Highly customizable (advanced users)

👉 Visit [DistroWatch](https://distrowatch.com/) to explore more.

---

### 🔹 Step 2: Download the ISO File

1. Go to the official site of the chosen distro.
2. Download the 64-bit `.iso` file.
3. (Optional) Verify the checksum (SHA256/MD5) for security.

---

### 🔹 Step 3: Create a Bootable USB

#### 💡 Tools:

- **Windows**: [Rufus](https://rufus.ie/), [UNetbootin](https://unetbootin.github.io/)
- **macOS/Linux**: [balenaEtcher](https://balena.io/etcher), or the `dd` command

#### 📦 Example (`dd` command for Linux/macOS):

```bash
sudo dd if=/path/to/linux.iso of=/dev/sdX bs=4M status=progress && sync
```

> ⚠️ Replace `/dev/sdX` with your actual USB device (not a partition like `/dev/sdX1`).  
> Be very careful — this command is powerful and can **erase all data** on the selected drive.

---

### 🔹 Step 4: Boot & Install

1. Reboot your system.
2. Press the **boot menu key** (`F12`, `Esc`, `Del`, etc.).
3. Select your USB stick.
4. Choose **"Install"** or **"Try without installing"** (Live Mode).
5. Follow the on-screen Linux installation steps.

> 💡 Tip: Most distros offer a "Try without Installing" mode — perfect for testing before full install!

---

## 💻 Option 2: Virtual Machine (VM)

Run Linux inside your current OS — no USB needed.

### 🔹 Tools:

- [VirtualBox](https://www.virtualbox.org/)
- [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html)

### 🔹 Steps:

1. Install your preferred VM software.
2. Create a new virtual machine.
3. Mount the downloaded Linux ISO file.
4. Allocate:
   - **RAM**: 2–4 GB
   - **Storage**: 15–30 GB (dynamically allocated)
5. Boot and install Linux inside the VM.

---

## 🪟 Option 3: Windows Subsystem for Linux (WSL)

Run Linux directly within Windows — no dual boot or VM.

### 🔹 Install WSL (Windows 10/11)

1. Open **PowerShell as Administrator**, then run:

```powershell
wsl --install
```

2. Restart your PC.
3. Choose a distro (Ubuntu is default).
4. Set a Linux username and password.

> 🔧 Tip: For better performance, enable WSL2:
> 
> ```powershell
> wsl --set-default-version 2
> ```

---

### 🔹 Useful WSL Commands

- View available distros:

```powershell
wsl --list --online
```

- Install a specific distro:

```powershell
wsl --install -d Ubuntu
```

- Launch WSL:

```powershell
wsl
```

---

### 🔹 Accessing Files Between Windows & Linux

- From **Linux to Windows**:
  ```bash
  /mnt/c/Users/YourName/
  ```
- From **Windows to Linux**:
  ```
  \wsl$\Ubuntu\home\yourname\
  ```

---

## ✅ Summary Table

| Method        | Best For                     | Tools Used                    |
|---------------|------------------------------|-------------------------------|
| Native Boot   | Full Linux experience        | Rufus, Etcher, ISO, `dd`      |
| VirtualBox    | Safe testing & learning      | VirtualBox, VMware            |
| WSL (Windows) | Developers on Windows        | PowerShell, WSL2              |

---

## 🔚 Final Tips

- ✅ Always **backup important files** before installing Linux alongside Windows.
- ✅ Use **WSL or VM** first if you’re unsure about full installation.
- ✅ Tools like **balenaEtcher** and **Rufus** are highly recommended for ease of use.

---

### 🚀 Happy Linux-ing! 🐧✨

---

## 📝 Additional Resources

- 🌱 [Linux Journey](https://linuxjourney.com/) – Interactive learning
- 🧠 [LinuxCommand.org](https://linuxcommand.org/) – Command line tutorials