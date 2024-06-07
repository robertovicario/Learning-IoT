# Summary of IoT Communication Lectures

## Lecture 1: IoT Communication Principles

### Before the Internet: ARPANET
- **ARPA (Advanced Research Projects Agency)**: Established in 1958 by US President Eisenhower in response to the Soviet launch of Sputnik 1.
- **First Packet-Switched Network**: Allowed long-distance communication between computers through packets over a shared medium.

### The Internet Era
- **First Use of 'Internet'**: 1974 Internet Protocol Suite RFC introduced the term, indicating internetworking.
- **Internet Protocol Suite**: Evolved into TCP/IP.

### The OSI Model
- **OSI (Open Systems Interconnection)**: Concept by Charles Bachman based on ARPANET experience.
- **Layers**:
  - **Physical Layer (PHY)**: Bits exchange across a medium.
  - **Data Link Layer (DLL)**: Frames exchange within the local network.
  - **Medium Access Control (MAC)**: Nodes access shared medium.
  - **Network Layer**: Nodes find each other outside the local network.
  - **Transport Layer**: Data delivery.
  - **Applications**: User activities.
- **In Practice**: Application layer is on top of the transport layer.

### Wired vs. Wireless
- **Differences**: PHY and MAC differ; others are similar except in low-power wireless.
- **Wireless Challenges**:
  - Error-prone communication due to RF propagation.
  - Interference and regulation.
  - Mobility and resource constraints of end devices.

### PHY Layer Functions
- **Modulation**: Converts baseband signals into transmittable waveforms. Advanced schemes enhance spectral efficiency.
- **Error-Control Coding**: Adds redundancy to avoid errors. Effective in both wired and wireless communication.

### Shannon-Hartley Theorem
- **Channel Capacity**: \( C = B \log_2(1 + \frac{S}{N}) \).
- **Implications**: Larger bandwidth increases capacity, justifying the need for modulation.

### Modulation in Wireless Communication
- **Antenna Size and Frequency**: Higher frequencies allow smaller antennas, beneficial for IoT devices but pose challenges with obstacle penetration.

### Cellular Networks
- **Common System**: Base stations (BS) handle communications over GHz frequencies.
- **Multiple Access**:
  - **TDMA**: Time slots.
  - **FDMA**: Frequencies.
  - **CDMA**: Codes.

### WiFi (802.11): CSMA-CA
- **Carrier Sense Medium Access - Collision Avoidance**: Users listen before talking to avoid collisions.
- **Distributed Coordination Function (DCF)**: Includes CSMA/CA, ACKs, and optional RTS/CTS.

### IoT Design Space
- **Short Range & Unlicensed Spectrum**: Most IoT communication operates under these conditions.

### Power at TX/RX
- **Transmit Power Ranges**: Vary across technologies from -20 dBm to 30 dBm.
- **Sensitivity**: Typically below -100 dBm.

### Low-Power Wireless
- **Technologies**: Handle short-range, low data-rate communication at low power.
- **Challenges**: Susceptible to RF and non-RF phenomena.

### RF Propagation
- **Phenomena Affecting Communication**:
  - **Large-Scale Path Loss**.
  - **Shadowing**.
  - **Fading**: Including multipath, static, and induced fading.

### Wireless Research Evolution
- **2000s**: Simulation-driven with unrealistic models.
- **2004-2010**: Experimental work with Berkeley motes and TinyOS.
- **2010-today**: Shift to application-level focus.

### Practical Connectivity Insights
- **Non-Circular Radios**: Connectivity patterns are complex and not mathematically tractable.
- **Reliability**: Link-level ACKs and retransmissions are crucial.

## Lecture 2: IoT Communication Technologies

### The Importance of MAC in Low-Power Wireless
- **Energy Waste Sources**:
  - Collisions
  - Overhearing
  - Control Overhead
  - Idle Listening

### Key Ideas
- **MAC Protocols**:
  - **Channel-Based**: For resource-rich (e.g., cellular) - TDMA, FDMA, CDMA.
  - **Contention-Based**: For resource-poor (e.g., WiFi, IoT) - CSMA-CA.

### CSMA-CA
- **Principle**: Listen before transmitting.
- **Collision Avoidance in Wireless**: Collisions are hard to detect, necessitating collision avoidance.

### Collisions
- **Causes in Wireless**:
  - **Hidden Terminal**: Node C interferes with Node B while A is transmitting.
  - **Exposed Terminal**: Node C unnecessarily waits when it could transmit to D without interference.

### Spread Spectrum
- **Resistance to Interference**: By spreading signal energy over a wider frequency range.
- **Types**:
  - **Frequency Hopping Spread Spectrum (FHSS)**.
  - **Direct-Sequence Spread Spectrum (DSSS)**.

### Long-Range + Low-Power Communication
- **LoRa**: Proprietary technology for long-range, low-rate communication.
- **LoRaWAN**: MAC layer for wide-area network based on ALOHA.

### ALOHA
- **Pure ALOHA**: Transmit without listening.
- **Slotted ALOHA**: Transmit at the beginning of time slots.

### Throughput Comparison
- **Efficiency of Protocols**: Varied depending on specific use cases and network conditions.

This summary provides a comprehensive overview of the key concepts and technologies discussed in the IoT communication lectures.