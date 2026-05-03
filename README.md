# Review_lab_packet-_tracer1
# Basic Router Security Configuration (Cisco Packet Tracer)

## 📌 Overview

This project demonstrates basic router security configuration using Cisco Packet Tracer.
It focuses on securing router access by setting passwords and enabling/disabling password encryption.

## 🛠️ Lab Setup

* Two routers (R1 and R2)
* Connected via **GigabitEthernet0/0**
* Simple point-to-point topology

## 🎯 Objectives

* Connect two routers
* Configure hostnames
* Set enable passwords
* Understand password visibility in running configuration
* Enable and disable password encryption

## ⚙️ Configuration Steps

### 1. Connect Routers

Connect R1 and R2 using:

```
GigabitEthernet0/0
```

### 2. Set Hostnames

```
Router> enable
Router# configure terminal
Router(config)# hostname R1
```

### 3. Set Enable Password

```
R1(config)# enable password cisco
```

### 4. Check Password (Before Encryption)

```
R1# show running-config
```

👉 Password will appear in **plain text**

### 5. Enable Password Encryption

```
R1(config)# service password-encryption
```

### 6. Check Password Again

```
R1# show running-config
```

👉 Password will now appear **encrypted**

### 7. Disable Password Encryption

```
R1(config)# no service password-encryption
```

### 8. Verify Again

```
R1# show running-config
```

## 🔐 Key Concept

* `service password-encryption` encrypts passwords in the configuration file
* Without it, passwords are stored in plain text (not secure)

## 📷 Topology

* 2 Routers connected directly
* No switches or PCs used

## 📚 Tools Used

* Cisco Packet Tracer

## 💡 Notes

* This is a beginner-level lab for understanding basic security concepts
* Useful as a foundation for more advanced topics like SSH and AAA

---

## 👩‍💻 Author

Basmala salah

## ⭐ Don't forget

If you found this useful, give the repo a star ⭐
