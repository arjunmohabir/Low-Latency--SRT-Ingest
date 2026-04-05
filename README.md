# Low Latency Streaming Over SRT (Ingest Server)

## Overview
This project demonstrates how to stream live video from a mobile device to a home PC using the SRT (Secure Reliable Transport) protocol. The setup enables stable, low-latency streaming over mobile data by forwarding a port and configuring OBS (Open Broadcasting Software) as an ingest receiver.

## Objective
To create a reliable remote video ingest pipeline that performs well over unstable or bandwidth-limited networks, using SRT instead of traditional protocols like RTSP.

## Key Concepts
- SRT (Secure Reliable Transport)
- Port Forwarding (NAT)
- Low-latency video streaming
- Network reliability over mobile data
- OBS ingest configuration

## System Architecture

Mobile Device (Encoder) → Public IP → Router (Port Forwarding) → OBS (SRT Listener)

## Setup Summary

### 1. Mobile Encoder
- Used a mobile streaming app (e.g., Larix Broadcaster / IRL Pro)
- Configured SRT output with target IP and port

### 2. Router Configuration
- Forwarded a specific port from the public interface to the internal PC
- Ensured correct protocol and port mapping

### 3. OBS Configuration
- Set OBS to listen for incoming SRT stream
- Configured media source with SRT listener mode

## Testing & Results
- Successfully streamed video from a mobile device over cellular data
- Maintained stable connection under varying network conditions
- Observed improved reliability compared to RTSP-based streaming

## Why SRT?
SRT provides:
- Packet loss recovery
- Adaptive bitrate support
- Lower latency under unstable conditions

This makes it ideal for mobile or remote streaming scenarios over mobile data connections.

## Real-World Applications
- Remote live broadcasting
- Field video reporting
- IRL streaming setups
- Contribution feeds for production environments

## Files Included
- `/images` → OBS configuration screenshots
- `/configs` → Example SRT settings and port forwarding details

## Notes
Sensitive data such as public IP addresses has been omitted for security.
