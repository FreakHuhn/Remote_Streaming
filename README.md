Remote_Streaming 

Browser-based remote access to your gaming laptopZero-install. Self-hosted. Firewall-friendly.

Project Goal

Remote_Streaming is intended to become a lightweight, fully browser-based solution for high-performance remote gaming and application streaming. The goal is to support restricted client systems like office PCs without requiring local installations.

Planned core features:

Real-time streaming of audio and video

Mouse, keyboard, and gamepad control

Use directly in a web browser

Firewall and NAT compatibility (WebRTC-based)

Full control via self-hosted infrastructure

Phase 1: Analysis & Architecture

Use Case:

Access your personal Windows gaming laptop

Remotely use graphics-intensive apps and games

Compatible with company/office PCs without admin rights

System Requirements:

Host: Windows, dedicated GPU, upload >10 Mbit/s

Client: Modern browser (Chromium-based recommended)

Network: WebRTC & NAT compatibility required

Technology Stack:

Backend: Sunshine (GameStream-compatible server)

Frontend: Moonlight Web (WebRTC client)

Alternative: Custom WebRTC + WebSocket solution possible

Phase 2: Preparing the Host System

Installation & Configuration:

Install Sunshine and add games/apps

Enable hardware encoding (e.g., NVENC)

Network & Security:

Open firewall for ports: 47984, 47989, 48010 (UDP)

Set up DynDNS (e.g., DuckDNS)

Optional: Reverse proxy for HTTPS (NGINX + Let's Encrypt or Cloudflare Tunnel)

Phase 3: Testing Remote Access

Establishing a Connection:

Use port forwarding or tunneling (Cloudflare / Tailscale)

Connect via Moonlight Web Client

Quality Assurance:

Test video, audio, and control

Adjust resolution, bitrate, FPS

Measure latency, optimize stability

Phase 4: Operation in Restricted Environments

Compatibility & Resilience:

Check WebRTC functionality (test.webrtc.org)

Simulate real-world conditions (office PCs, restrictive networks)

Test mouse & keyboard input

Fail-Safes:

Configure Sunshine auto-restart

Set up Wake-on-LAN or smartphone fallback access

Phase 5: Further Development

Usability:

Custom web GUI as launcher for games & apps

Monitoring & Security:

Monitor connections, implement latency alerts

Secure access: token, IP filtering, authentication

TLS via reverse proxy

Vision

At the end of this learning journey, the result should be a fully browser-based remote desktop stream from your private gaming laptop:

No client setup required

Secure and self-hosted

Ready to use at home, on the go, or in office environments

Remote_Streaming aims to become your digital window into your high-performance machine – no matter where you are.