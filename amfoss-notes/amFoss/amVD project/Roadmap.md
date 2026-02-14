PHASE 0 — Mental Model (Week 0)

Before touching code, you must understand the stack:

Kernel (DRM/KMS)  
Compositor (Hyprland)  
Capture (PipeWire)  
Encode (H.264)  
Transport (USB network)  
Decode (Android)  
Input (uinput)

If you can explain each layer without guessing, you’re ready.

---

PHASE 1 — Virtual Monitor Foundation (Week 1)

Goal: Make Linux believe a new monitor exists.

Tool:  
VKMS

Tasks:

1. Load vkms module.
    
2. Verify new DRM device appears:  
    /sys/class/drm/
    
3. Confirm Hyprland detects it.
    
4. Force enable the output.
    
5. Move a window onto it.
    

Milestone:  
You can extend your desktop onto a black virtual monitor.

No streaming yet.

---

PHASE 2 — Frame Capture (Week 2)

Goal: Capture only the VKMS monitor frames.

Tool:  
PipeWire

Tasks:

1. Use PipeWire to list available outputs.

2. Capture VKMS output.
    
3. Save frames or display locally in a window.
    

Milestone:  
You can see the virtual monitor content in a separate preview window.

This proves your capture pipeline works.

---

PHASE 3 — Encoding (Week 3)

Goal: Compress frames efficiently.

Tool:  
GStreamer

Tasks:

1. PipeWire → GStreamer pipeline.
    
2. Encode with H.264.
    
3. Save to file.
    
4. Tune for low latency (no B-frames, low buffering).
    

Milestone:  
You can record the VKMS display as video with low delay.

---

PHASE 4 — Streaming Over Network (Week 4)

Goal: Send encoded video to another machine.

Transport choice:  
WebRTC (recommended).

Tasks:

1. Build simple WebRTC sender on Linux.
    
2. Build simple WebRTC receiver on another Linux PC.
    
3. Display stream in real time.
    

Milestone:  
VKMS monitor appears live on another computer.

Now you’ve built a remote monitor.

---

PHASE 5 — USB Transport (Week 5)

Goal: Replace LAN with USB cable.

Method:  
USB tethering → creates usb0 network interface.

Tasks:

1. Enable USB tethering on Android.
    
2. Verify usb0 network interface appears.
    
3. Ping Android.
    
4. Run your streaming server bound to usb0 IP.
    

Milestone:  
VKMS monitor appears on Android over USB.

No Wi-Fi involved.

---

PHASE 6 — Android Client (Week 6)

Android responsibilities:

1. Connect via WebRTC.
    
2. Decode H.264.
    
3. Render fullscreen.
    
4. Lock orientation.
    

Milestone:  
Phone behaves visually like a monitor.

---

PHASE 7 — Input Feedback (Week 7)

Linux tool:  
uinput (kernel input injection)

Tasks:

1. Android captures touch coordinates.
    
2. Send via WebRTC data channel.
    
3. Linux daemon receives.
    
4. Inject mouse/touch events via uinput.
    

Milestone:  
Touching phone moves Linux cursor.

Now it’s interactive.

---

PHASE 8 — Hotplug Illusion (Week 8)

Goal: Make it feel native.

When USB connects:

1. Android app sends handshake.
    
2. Linux daemon enables VKMS output.
    
3. Compositor reconfigures display layout.
    
4. Streaming starts automatically.
    

When USB disconnects:

1. Stop stream.
    
2. Disable VKMS output.
    

Now it behaves like plugging HDMI.

---

PHASE 9 — Latency Optimization (Week 9)

Measure:

Capture delay  
Encode delay  
Network RTT  
Decode delay  
Input round-trip

Tune:

Encoder preset  
Buffer sizes  
Queue depth  
Thread priorities

Target:  
< 40 ms total latency