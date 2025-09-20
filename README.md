
<p align="center">
<img src="https://discords.com/_next/image?url=https%3A%2F%2Fcdn.discordapp.com%2Femojis%2F758749699364094023.gif" alt="arobsite" height="200">
                                                                                                                                                                                                                                                                               </p>
<div align="center">
                                                                                                                                                                                                                                                                               <h1>
Fast-Flags Guide

Made by <a href="https://discord.com/users/1254472513199673347">Scroom</a>,<a href="https://discord.com/users/1104189426374033519">Onion</a>,<a href="https://discord.com/users/1344953953095258144">koain</a>,<a href="https://discord.com/users/1395141912339677186">arobsite</a>
                                                                                                                                                                                                                                                                               </h1>
                                                                                                                                                                                                                                                                              </div>

# What are Fast-Flags?
**FastFlags (also known has FFlags) are a simple method for testing new features in roblox. u can mess around with FastFlags to test new features. It’s also a great way of seeing if a new issue is caused by a newly released feature. This concept exists in many pieces of software. For example, Google Chrome has chrome://flags/, which works in a similar way. Toggling FFlags can be useful for testing highly technical features or enabling very specific settings.**

**In Roblox, Engine Settings use the FastFlag system. This lets engineers make changes to the game engine without pushing a full update. It’s mostly used for things like [A/B testing](https://wikipedia.org/wiki/A/B_testing) or slowly rolling out new features. All FastFlags are set up by Roblox engineers, and the client loads a list of them from the internet when it starts.**
> [!CAUTION]
> **Using FastFlags should be treated as operating in a kind of “superuser mode.” Superusers have the ability to break things: if you enable the wrong flag, you might cause Roblox Studio or the client to malfunction.**
---
# Will using this get me banned?
**Short answer: No, it won’t. We are 100% sure of it, and even [Roblox Staff have confirmed that fact.](https://devforum.roblox.com/t/welcoming-byfron-to-roblox/2018233/693?u=xtremeguy2256 ) Bootstrappers are not exploit software and have nothing to do with exploiting.**
> **But if you are still using abusive FFlags (such as Noclip, JumpBoost, or Visual Glitches), people can detect this and report you, which may result in a ban.**
---
# Roblox Client Debug Menu Keybinds
| **Action**             | **Windows**              | **Mac**                   | **Mobile**                                    |
|------------------------|--------------------------|---------------------------|-----------------------------------------------|
| *Game stats*           | `Shift + F1`             | `Fn + Shift + F1`         | None                                          |
| *Graphics stats*       | `Shift + F2`             | `Fn + Shift + F2`         | None                                          |
| *Network stats*        | `Shift + F3`             | `Fn + Shift + F3`         | None                                          |
| *Network diagnostics*  | `Ctrl + Shift + F3`      | `⌘ + Fn + Shift + F3`     | Double-tap *"Joining game"* while loading    |
| *Network debugging*    | `Shift + F3`, then `Shift + 1` | `Fn + Shift + F3`, then `Shift + 1` | None |
| *Physics stats*        | `Shift + F4`             | `Fn + Shift + F4`         | None                                          |
| *Summary stats*        | `Shift + F5`             | `Fn + Shift + F5`         | None                                          |
---

<details>
<summary><h2><strong>FastFlags Documentation</strong></h2></summary>
<h2>What sites/bot are available for finding Fast-Flags?</h2>

**[FVariables](https://raw.githubusercontent.com/MaximumADHD/Roblox-Client-Tracker/roblox/FVariables.txt) ~ A sorted list of fast variables, which are used by Roblox to toggle changes to the engine remotely on multiple platforms without having to redeploy the client**

**[Flemish FastFlags](https://discord.gg/UHfwyxjeya) ~ This bot brings together all the features in one place. Instead of using separate tools like FVariables, you can access and use every FastFlag-related function through simple commands**

---
<details>
<summary><h2>Fast-Flags Tips-Explanations</h2></summary>

> 1. Roblox is mainly a CPU based game.
> 2. You can find fastflags in the Roblox Dev Console Memory.
> 3. FLogDebugShowFlagState is 90% correct; it only turns 100% correct when you join a game.
> 4. Having overlays can actually harm FPS, so yes. `FFlagDebugDisplayFPS` can actually reduce FPS.
> 5. Disabling **all** `telemetry`, will not do anything in terms of performance. It will also cause visual and other bugs.
---
<details>
<summary><h2>Fast-Flags Bits</h2></summary>

**A "bit" is how much data can be processed. For example, 64 bit will process more data than a 32 bit.**

**There is only 3 types of bits in fastflags**

> **32 Bit - Maximum value is 2,147,483,647**
>
> **16 Bit - Maximum value is 32,767**
>
> **8 Bit - Maximum value is 255.**

**These maximum values all can be checked with flagstate. 8 bit fastflags are generally useless and have no use.**

---
<details>
<summary><h2>Fast-Flags Headers</h2></summary>

> 1. `_IXP` ~ Internet Exchange Point. Used in IP networking, allowing Internet Service Providers (ISPs) to exchange traffic between their networks.
> 2. `_Staged` ~ A replica of a production environment, often used for testing or staging purposes.
> 3. `_PlaceFilter` ~ A filter that restricts FastFlags to a specific experience (place). Useful for saving time when switching between different games.
> 4. `_DataCenterFilter` ~ Similar to _PlaceFilter, but applies to datacenter IDs. Mainly useful for RakNet-related FastFlags.
```
{ "DFFlagDebugPauseVoxelizer_PlaceFilter": "True;GameID",
"DFIntConnectionMTUSize_DataCenterFilter": "1472;DataCenterID" }
```
---
<details>
<summary><h2><strong>Fast-Flags Configuration Prefixes</strong></h2></summary>

---
### `DFFlag`
> **Dynamic Fast Flag**
> - **Type:** Boolean (`true/false`)
> - **Description:** A dynamic flag that can be modified during runtime. It automatically updates every 5 minutes, reflecting any changes made to it.

### `FFlag`
> **Fast Flag**
> - **Type:** Boolean (`true/false`)
> - **Description:** A static flag that is initialized once and does not change throughout the session. It remains constant until a new session begins.

### `FInt`
> **Fast Integer**
> - **Type:** Integer (`-2147483648` to `2147483647`)
> - **Description:** A static integer that is initialized once and remains unchanged throughout the session. It only updates when a new session starts.

### `DFInt`
> **Dynamic Fast Integer**
> - **Type:** Integer (`-2147483648` to `2147483647`)
> - **Description:** A dynamic integer that can be updated during runtime. It refreshes automatically every 5 minutes to reflect any changes.

### `FLog`
> **Fast Log**
> - **Type:** Boolean (`true/false`) or Integer (`-2147483648` to `2147483647`) or Byte (`Warning, Verbose, ect`)
> - **Description:** A static log variable that is initialized once and does not change until a new session. It remains constant until the session is reset.

### `DFLog`
> **Dynamic Fast Log**
> - **Type:** Boolean (`true/false`) or Integer (`-2147483648` to `2147483647`) or Byte (`Warning, Verbose, ect`)
> - **Description:** A dynamic log variable that can change during runtime. It automatically refreshes every 5 minutes to reflect any updates made.

### `FString`
> **Fast String**
> - **Type:** String (`text`)
> - **Description:** A static string variable that is initialized once and remains unchanged throughout the session. It does not update until a new session starts.

### `DFString`
> **Dynamic Fast String**
> - **Type:** String (`text`)
> - **Description:** A dynamic string that can be updated during runtime. It automatically updates every 5 minutes to reflect any changes made.

### `SFFlag`
> **Synchronized Fast Flag**
> **Type:** Boolean (`true/false`) or Integer (`-2147483648` to `2147483647`)
> **Description:** A synchronized flag variable that is loaded by the server and sent to the client. It ensures that the flag’s state is consistent across different clients. The flag's value is forced by the server and cannot be changed by the client (you).
---
<details>
<summary><h2><strong>Fast-Flags Acronyms</strong></h2></summary>

---
> # "A" Letter Acronym FastFlags
---
```
AR: Augmented Reality
AI: Artificial Intelligence

Avg: Average
Agg: Aggregate
ACK: Acknowledge
ABR: Adaptive Bitrate
ACS: Access Control System
AUM: Assets under management
ACE: Animation Curve-Clip Editor
ACR: Asset Content-Cache Resolver
AES: Advanced Encryption Standard
AMC: Automated Moderation Capture
ACP: Accelerated Collision Pipeline
API: Application Programming Interface
ATC: Asset Transaction Cache / Automatic TXT Capture

Auth: Authentication
ASAN: AddressSanitizer
ACCb: Access Control Callback
AABB: Axis-Aligned Bounding Box
APGS: Asynchronous Projected Gauss-Seidel
ASTC: Adaptive Scalable Texture Compression
AICO: Artificial Intelligence Code Completion-Assistant

Async: Asynchronous
Arg-Args: Argument(s)
Aniso: Anisotropic Filtering
```

---
> # "B" Letter Acronym FastFlags
---
```
BW: Bandwidth
BG: Backgroun
BC: Block Compression
BVH: Bounding Volume Hierarchy
BPS: Bytes-Bits Per Seconds
BFS: Breadth-First Search
BTID: Browser Tracking-Token ID
```
---
> # "C" Letter Acronym FastFlags
---
```
CN: China
CD: Compositor Debugger

CTA: Call to Action
CPP: C++ [C Plus Plus]
CFM: Custom Fonts Module
CLI: Client-Command Line Interface
CSG: Constructive Solid Geometry
CCD: Cyclic Coordinate Descent
CDN: Content Delivery Network
CJK: Chinese-Japanese-Korean
CPU: Central Processing Unit
CSV: Comma-Separated Values
CDC: Compressed Data Codec
CFL: Courant–Friedrichs–Lewy Condition

Cull: Culling
CFrame: Coordinate Frame
Calc: Calculation/Calculate
```
---
> # "D" Letter Acronym FastFlags
---
```
DB: Database
DC: Data Carrier
Diff: Difference
DPI: Dots per inch
DMP: DataModelPatch
DOF: Depth of Field
DNS: Domain Name System
DSP: Digital Signal Processing
DCR: Developer Console Rewrite
DRM: Digital Rights Management
DRS: Dynamic Resolution Scaling
DXT: DIrectX Texture Compression (S3TC)
Diq: Data Ingestion Quota / Delay-In-Queue
DCD: Data Carrier Detection-Decomposition / Dynamic CSG Decomposition
```
---
> # "E" Letter Acronym FastFlags
---
```
EXP: Experience
ELF: Event Logging Framework

Exec: Execute
Email: Electronic Mail
ESEI: Event Stream Edge Ingestion
```
---
> # "F" Letter Acronym FastFlags
---
```
FC: Fast Cluster
FV: FastVariables
FK: Forward Kinematics

FIB: Future Is Bright
FPS: Frames Per Second
FRM: Frame Rate Manager
FSM: Froxel-Forward Shading-Shadow Manager / Finite State Machine

Func: Function
Freq: Frequency
FTUX: First Time User Experience
```
---
> # "G" Letter Acronym FastFlags
---
```
GB: Gigabyte
GC: Garbage Collection / Game Content

GLC: Gui Layout Container
GPU: Graphics Processing Unit
Gma: Game Manager API / Google Mobile Ads
GJK: Gilbert–Johnson–Keerthi Distance Algorithm

glFT: GL Transmission Format
GUAC: Global User App Configuration
GUID: UUID - Globally / Universally Unique Identifier
```
---
> # "H" Letter Acronym FastFlags
---
```
HSR: Hidden Surface Removal
HDR: High Dynamic Range

HTTP: Hypertext Transfer Protocol
Hz/Hertz: Measurement For Frequency
HTTPS: Hypertext Transfer Protocol Secure
HACD: Hierarchical Approximate Convex Decomposition
```
---
> # "I" Letter Acronym FastFlags
---
```
IP: Internet Protocol
Iter(s): Iteration(s)
Ik: Inverse Kinematics
IG: Intel-Integrated-Immediate Graphics

IAP: In-App Purchase
Inc: Incoming / Income
IAS: Input Action System
ISA: Instance Class Name
IBL: Image-Based Lighting
IXP: Internet Exchange Point
iOS: iPhone Operating System
ISR: Interrupt Service Routine
IDE: Integrated Development Environment
```
---
> # "K" Letter Acronym FastFlags
---
```
KB: Kilobytes
KD: K-Dimensional
KBpS: Kilobytes Per Second

KFS: Key Frame Sequence
KTX: Khronos Texture
```
---
> # "L" Letter Acronym FastFlags
---
```
LT: Live Telemetry
LMKD: Low Memory Killer Daemon

LOD: Level of Detail
LSC: Lua Script Cache
LRU: Least Recently Used
LERP: Linear Interpolation
LSP: Language Server Protocol
LMS: Log-Latency Measurement Service
LDL: Lower Diagonal Transpose [L: lower triangular matrix | D: diagonal matrix | L: transpose of L]
```
---
> # "M" Letter Acronym FastFlags
---
```
MB: Megabyte
ML: Machine Learning

Max: Maximum
Msg: Message
MIB: Mebibyte
Min: Minutes-Minimum
MPS: Market Place Service
MRS: Message Routing Service
MTU: Maximum Transition Unit
MRF: Multiple Replication Foci
MFT: Metrics-Memory-Monitoring Fault Telemetry
MRD: Metrics-Monitoring Report Data / Mega Replicator Data-Dictionary

Mutex: Mutual Exclusion
MMAP: Memory-Mapped File I/O
MS/MSec/Millis: Milliseconds
MacOS: Macintosh Operating System
MSAA: Multisampling Antialiasing
```
---
> # "N" Letter Acronym FastFlags
---
```
NS: Native Service / N Seconds
NLSM: Network Layer Statistics-State Monitor
NCNN: Neural Network Inference Framework
NLERP - Normalized Linear Interpolation

Num: Number
NAT: Network Address Translation
NOU: Number of Units-Network Ownership
NII: Network Interpolation-Integration / Natural-Language Input Inspection-Inference
```
---
> # "O" Letter Acronym FastFlags
---
```
OTA: Over-the-Air
OOM: Out Of Memory
OS: Operating System
OOP: Object Oriented Programming
```
---
> # "P" Letter Acronym FastFlags
---
```
PC: Personal Computer
PD: Physics Data [Proportional-Derivative]

Pkt: Packet
Ptr: Pointer
Pct: Percent
Par: Particle
PPJ: Price Per Job (?)
POC: Proof of Concept
PDP: Product Detail Page
PPP: Per-Particle Physics
PGS: Projected Gauss-Seidel
PBR: Physically Based Rendering
PMD: Packet Metadata Decoder / Part-Mesh Data
PVS: Potentially Visible Sets / Position–Velocity Solver

Poly: Polygon
Prio: Priority
Param: Parameter
Perf: Performance
Prot: Protocol-Protection
PCGDK: PC Gaming Development Kit
```
---
> # "R" Letter Acronym FastFlags
---
```
Rx: Receive
RN: Rotation Number
Roact: Rodux-Roblox UI Frameworks

Rbx: Roblox
Rcv: Receive
Rep: Replicator
RTT: Round-Trip Time
RTC: Real-Time Communication
RTL: Right-to-Left (Arabic TXT)
RSPV: Roblox Experience Event Prompt
RSS: Resident Set Size / Rich Site Summary
RCC: Remote Chat Channel / Roblox Cloud Compute
```
---
> # "S" Letter Acronym FastFlags
---
```
SJ: Stream Job
SM: Static Mesh
SN: Scale Number
SK: Skeletal-Skeleton Mesh

Snd: Send
Sec: Seconds
Sim: Simulation
STT: Speech-to-Text
SJT: Stream Job Time
SSL: Secure Sockets Layer
SDF: Signed Distance Field
Sat: Separating Axis Theorem
SSR: Screen Space Reflections
SDK: Software Development Kit
SFU: Selective Forwarding Unit
STR: Scene Tree Renderer / String

Stat: Statistics
SSAA: Supersampling Antialiasing
Sync: Synchronized-Synchronization
SIMD: Single Instruction Multiple Data
SLERP - Spherical Linear Interpolation
```
---
> # "T" Letter Acronym FastFlags
---
```
Tx: Transmit
Thou: Thousand-Thousandths
TN: Translation (Pyhics) Number
TC: Texture Compression / Team Create / Terms Compliance

TTS: Text-to-Speech
TCS: Text Chat Service
TAA: Temporal Anti-Aliasing
TLS: Transport Layer Security
TCP: Transmission Control Protocol
```
---
> # "U" Letter Acronym FastFlags
---
```
UX: User Experience
US-USec: Microseconds
UI: Screen UI or User Interface
UWP: Universal Windows Program
URL: Uniform Resource Locator
URE: Unreliable Remote Event
UDP: User Datagram Protocol
UGC: User-Generated Content
```
---
> # "V/W" Letter Acronym FastFlags
---
```
VK: Vulkan
WK: Webkit
WS: Web Socket
V[Number]: Version
VR: Virtual Reality
VM: Virtual Machine
VRAM: Video Random-Access Memory

Win: Windows
Var: Variable/Variant
WMD: Vocaloid Motion Data
VAD: Voice Activity Detection
VNG: Vietnamese-VinaGames [Vietnamese Company]
```
---
> # "J/Q/X/Y/Z" Letter Acronym FastFlags
---
```
Xbox: DirectX Box
XHR: XMLHttpRequest
QSG: Qt Scene Graph
JIT: Just-in-Time (Compilation)
JDI: Json Delta Interchange
QoS: Quality of Service
YUV: Y-Luma U,V-Chroma
```
---
