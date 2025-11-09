---
layout: post
title:  "Automotive CAN - A brief History"
date:   2025-11-06 11:15:32 +1100
categories: autmotive background
author: Davie C
images:
- images/@stock/post-6.jpg
---

Overview of Automotive CAN (Controller Area Network)

## 🧠 What Is CAN?

**CAN (Controller Area Network)** is a communication protocol used in automotive and industrial systems that allows multiple electronic control units (**ECUs**) to exchange data efficiently without a central computer.

Developed by **Bosch in the 1980s**, CAN became the backbone of in-vehicle communication, enabling reliable real-time data transfer between systems such as the engine, transmission, brakes, airbags, and infotainment.

---

## ⚙️ How It Works

CAN is a **multi-master, message-based bus**.  
This means any node can transmit data, and all nodes listen to the same shared network (the **bus**).

Each CAN message:
- Has an **identifier** (which defines message priority)
- Carries up to **8 bytes of data** (in classic CAN; **64 bytes in CAN-FD**)
- Includes **error checking** and **acknowledgment bits** for reliability

Instead of sending messages to specific addresses, CAN uses a **broadcast model** — every ECU receives the same message and decides whether it’s relevant.

---

## 🔌 Key Technical Details

| Feature | Description |
|----------|-------------|
| **Speed** | Up to 1 Mbps (Classic CAN), 2–5 Mbps (CAN-FD) |
| **Bus Type** | Differential pair (CAN_H, CAN_L) for noise resistance |
| **Topology** | Linear bus with termination resistors (typically 120 Ω at each end) |
| **Message Arbitration** | Priority determined by lower message ID number |
| **Error Detection** | CRC checks, bit monitoring, automatic retransmission |
| **Physical Layer** | Uses ISO 11898-2 (high-speed) or ISO 11898-3 (low-speed/fault-tolerant) |

---

## 🚗 Typical CAN Networks in Vehicles

Modern vehicles use **multiple CAN buses**, often with gateways between them:

| Network | Typical Speed | Example Systems |
|----------|----------------|------------------|
| **Powertrain CAN** | 500 kbps – 1 Mbps | Engine, Transmission, ABS |
| **Body CAN** | 125 kbps – 250 kbps | Doors, Lights, HVAC |
| **Infotainment CAN** | 500 kbps | Radio, Display, Navigation |
| **Diagnostics (OBD-II)** | 500 kbps | Vehicle scanning and service tools |

---

## 🧩 CAN vs CAN-FD

**CAN-FD (Flexible Data Rate)** is an enhanced version of CAN that:
- Increases data length from **8 → 64 bytes**
- Allows **faster data phase speeds**
- Improves efficiency for high-bandwidth modules (ADAS, sensors, cameras)

---

## 🔍 Applications Beyond Automotive

While dominant in vehicles, CAN is also used in:
- Industrial automation (PLC networks)
- Medical equipment
- Robotics
- Marine and aerospace systems

---

## 🧱 Summary

- **CAN** is a robust, low-cost network for real-time communication between vehicle modules.  
- It eliminates point-to-point wiring, reducing weight and complexity.  
- Its reliability, built-in error handling, and scalability make it a cornerstone of **modern automotive electronics**.

---

*References:*
- Bosch CAN Specification v2.0
- ISO 11898-1/2 Standards
- Vector, NXP, and Microchip CAN documentation

