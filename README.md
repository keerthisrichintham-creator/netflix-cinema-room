# Netflix Cinema Room — Synchronous Social Viewing

Zero-buffer co-watching via local DRM cache + WebSocket sync ≤150ms

Live Prototype:(https://www.figma.com/make/WSUuoXjgijua4d5BTHk8Wa/Netflix-Cinema-Room-Prototype?fullscreen=1&t=Tu8WGdOw4amxoUSu-1&code-node-id=0-6)

### Problem
Netflix party extensions have 30-40% buffering, no social feel, and audio echo.

### Solution
Native Netflix Cinema Room for 2-8 friends with:
- Pre-flight checks (Storage + License + Geo)
- Host controls vs Guest Raise Hand
- After-show Lounge with 40% PiP

### Guardrails Built (from my PRD)
- G-6 Storage Gate: File + 500MB buffer, block if <2GB
- G-1 Geo: ISO-3166 Same country check
- G-5 Sync: ≤150ms drift
- G-7 Audio Ducking: -12dB when guest speaks
- G-8 Auto-purge in 24h

### Screens
1. Lobby - Download Manager 88% → 100%
2. Pre-flight - All checks verified
3. Cinema Viewport - Synced 1080p
4. After-show Lounge - Ratings + Trivia

### Metrics
Zero-buffer >98%, Lounge engagement >60%

By Keerthisri Chintham | Product Manager  Project
