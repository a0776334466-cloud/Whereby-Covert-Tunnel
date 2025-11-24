# Whereby-Covert-Tunnel 🎭 (TorKameleon-based)

**Project Lead:** [YOUR GITHUB USERNAME / NAME HERE]
**Status:** Seeking engineering talent for critical Transcoding/FEC integration.
**Based on the foundational research of Afonso Vilalonga.**

## 🎯 The Mission: Bypassing Application-Layer Whitelisting

Our censorship environment allows ONLY legitimate traffic to known services (e.g., Whereby, Zoom). Our goal is to tunnel full IP traffic through the **live Whereby servers**, not just mimic the WebRTC protocol.

### The Core Challenge: Transcoding Death
When we send our steganographic H.264 video through Whereby, the service's video processing (**Transcoding**) actively **destroys** the hidden Motion Vector (MV) data. The project's success hinges entirely on **data survival** during this process.

---

### 🛑 Important Note to Contributors: Current Code Status
Due to technical constraints with the web interface, the original TorKameleon PoC files have not yet been fully uploaded to this repository. Contributors are encouraged to examine the original research codebase (link available in **CREDITS.md**) while the Maintainer works on a complete synchronization. We are urgently seeking **Technical Lead** expertise to rebuild the structure collaboratively.

---

## 🏗️ We Are Recruiting Contributors for 3 Critical Modules

We have the core MV Steganography concept. We need experts to make it operational as a SOCKS5 tunnel.

### 1. Transcoding Survival & Robustness (FEC) 🛡️
* **Goal:** Integrate ultra-robust **Reed-Solomon (FEC)** directly within the C core. The FEC must be engineered to handle high data loss (up to 70%) caused by the Whereby server's video processing.
* **Deliverable:** A C library/wrapper ensuring hidden IP packets are recoverable on the server-side despite heavy corruption.
* **Skillset:** C/C++, Advanced Algorithms, Error Correction Coding.

### 2. Live Whereby/WebRTC Integration 📞
* **Goal:** Connect our SOCKS5 tunnel payload to the actual WebRTC stream established *through* the live Whereby service. This involves connecting to a meeting and injecting our MV-steganography stream as the user's video feed.
* **Deliverable:** Python/WebRTC code that manages the connection lifecycle with Whereby and handles the MV stream injection/extraction.
* **Skillset:** WebRTC Protocols (Signaling, ICE), Python (aiortc, or similar WebRTC libraries).

### 3. SOCKS5 Tunnelling (IP Management) 🚇
* **Goal:** Build the Python wrapper to manage all incoming and outgoing IP traffic for the steganography pipeline.
* **Deliverable:** A SOCKS5 proxy that segments IP packets into payloads for the FEC module and reassembles them on the other end.
* **Skillset:** Python (Networking), SOCKS/VPN Protocols.

## 🤝 Join the Effort
If you are passionate about building anti-censorship tools for the harshest environments, please open a GitHub Issue or contact the Project Lead.
