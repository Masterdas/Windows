 # Windows 10 Pro
<a href="https://youtu.be/_LZpwUM91UU" target="_blank">
  <img src="https://github.com/Masterdas/Windows/blob/main/windows.jpg?raw=true" alt="Android Windows Image">
</a>

# [VNC App Download link](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)
---
 
 
 ▶️ [Demo Server Setup video](https)
✅ Termux uses its own package manager (`pkg`), and it has its own repositories.
✅ The **`qemu-system-x86-64-headless`** package does not exist in Termux.
✅ Instead, Termux provides the **`qemu-system-x86_64`** package, which can be used in headless mode as well.

---

### How to install QEMU in Termux

###  **Update Termux**
📥[ Windows 10](https://drive.google.com/uc?export=download&id=1FbymOjzMGydmeZ7K5dZxBK6efA3iakNn)
```
pkg update && pkg upgrade
```

### Install QEMU

```
apt install qemu-system-x86-64-headless 
```
###  Open Download path
```
cd /storage/emulated/0/Download/
```

### Win10pro Run 

```
qemu-system-x86_64 -hda Win10pro.qcow2 -m 4096
```

 **(Optional) Install qemu-img**

```
pkg install qemu-img
```

---

### Running Windows 10 VM (example command)

Since Termux does **not** support KVM, and GUI is tricky, you’ll typically run it headless or via VNC:

**Headless mode (no GUI, just console output)**:

```
qemu-system-x86_64 \
  -hda Win10pro.qcow2 \
  -m 2048 \
  -smp 2 \
  -cpu max \
  -net nic -net user \
  -nographic
```

**With GUI via VNC**:

```
qemu-system-x86_64 \
  -hda Win10pro.qcow2 \
  -m 2048 \
  -smp 2 \
  -cpu max \
  -net nic -net user \
  -vnc :1
```

Then, use a VNC Viewer app on your phone to connect to **127.0.0.1:5901**.

---

