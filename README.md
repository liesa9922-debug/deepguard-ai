# DeepGuard AI — Multimodal Deepfake Detection & Media Verification System

DeepGuard AI is a client-side cybersecurity web application that analyzes videos, voice recordings, images, text documents, and URLs for synthetic generation, manipulation, and cryptographic provenance.

## Core Modules

- **Video & Lip-Sync Detector**: Samples keyframes across uploaded videos, evaluates facial-zone luminance and boundary sharpness shifts, correlates lower-face motion against speech intervals, and provides clickable suspicious timestamps.
- **AI Voice & Live Microphone Detector**: Uses the Web Audio API and a Radix-2 Cooley-Tukey FFT to measure high-frequency neural vocoder cutoffs (`>7.5 kHz`) and Wiener spectral flatness.
- **Image Manipulation (ELA) Detector**: Performs `90%` JPEG recompression Error Level Analysis to render an interactive thermal heatmap overlay and scans binary headers for EXIF/XMP/C2PA/AI-generator markers.
- **Document Stylometry & Link Verifier**: Evaluates sentence-length burstiness and Type-Token lexical diversity in text documents, and inspects URLs for HTTPS transport, punycode spoofing, and suspicious TLDs.
- **Forensic PDF & QR Reporting**: Generates SHA-256 integrity hashes, structured Explainable AI (XAI) evidence breakdowns, downloadable PDF certificates, and scannable verification QR codes.

## Privacy & Architecture

All media processing executes locally in browser memory using HTML5 Canvas, Web Audio API, and Web Crypto API—user files are never uploaded to external public servers.
