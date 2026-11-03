# Hi there, I'm 0xKnowles 👋

> **A full portfolio site (same content as this README, in a browsable format) lives in
> [`docs/`](docs/) — enable GitHub Pages on this repo (Settings → Pages → Deploy from branch →
> `/docs`) to serve it at `https://0xknowles.github.io/0xKnowles/`.**

I love Plants, Tech and AI

- 🚀 **Core Stack:** TypeScript, React, Next.js, Angular, Node.js, C/C++, Kotlin, Python, and KiCad for hardware design.
- 🛠️ **Current Focus:** Custom embedded firmware for e-ink devices, self-hosted media tooling, AI agents and MCP, and automated cultivation monitors.
- 🌱 **Domain Expertise:** A strong background in IT infrastructure paired with deep experience in Integrated Pest Management (IPM) and greenhouse automation.

---

### 📂 Featured Projects

#### 📡🔒 [Ruby Firmware](https://github.com/0xKnowles/Ruby)
Custom firmware for the **XTEink X3 and X4** e-ink readers that turns the hardware into a stealthy, long-battery-life passive RF signal analyzer — with a small digital companion living in the corner of the screen.

<p align="center">
<img height="250" alt="Handshake" src="https://github.com/user-attachments/assets/a6e14307-bd01-49e7-aea4-693c88bfaf39" />
<img height="250" alt="Settings" src="https://github.com/user-attachments/assets/c150fb60-7484-4df4-8232-365d0ffd381e" />  
</p>


* **Passive RF Capture:** 802.11 monitor-mode WiFi sniffing (beacons, probe requests, WPA 4-way-handshake detection) plus passive BLE advertisement scanning — receive-only by default, nothing associates, pairs, or transmits.
* **Encrypted On-Device Logging:** Every observation is deduplicated and independently written to an AES-256-GCM encrypted daily log, decryptable right on the device with no PC required.
* **Ruby, the Companion:** A small creature reacts with a changing mood as a live front-end for what it's hearing, plus a Level 1-5 badge and header EXP bar tracking lifetime progress from unique devices seen and handshakes captured.
* **Opt-in Auditing Tools:** Raw `.pcap` handshake export for offline password auditing with hashcat, plus an active-deauth capability gated behind an explicit, off-by-default whitelist/blacklist targeting system.

<p align="center">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/excited.bmp" width="90" alt="Ruby, EXCITED">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/curious.bmp" width="90" alt="Ruby, CURIOUS">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/content.bmp" width="90" alt="Ruby, CONTENT">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/bored.bmp" width="90" alt="Ruby, BORED">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/lonely.bmp" width="90" alt="Ruby, LONELY">
</p>

#### 🌿🐣 [CrossPlant Firmware](https://github.com/0xKnowles/CrossPlant)
An open-source custom firmware fork for the **XTEink X3 and X4 mini e-ink readers**. It merges the advanced typography and performance optimizations of *CrossInk* with a re-engineered virtual plant companion mechanics system (*CrossPet*).

* **The Virtual Plant System:** Features a reading-driven ecosystem where plant stats (Moisture, Happiness, Health, Discipline) decay in real time while awake, evolving through branches (**Scholar 🎓**, **Balanced ⚖️**, or **Wild 🌲**) based on actual reading habits and streaks.
* **Premium Features:** 
  * A space-efficient **Two-Column UI** separating plant vitals from detailed reading partner statistics.
  * **Dew Drops (DD) Economy:** Real-time reading reward synchronization (+1 DD per page, +100 DD per book, time-based accumulation) to spend in an interactive item & cosmetic accessory shop.
  * **Dynamic Canvas Rendering:** Pixel-art accessories (Glasses, Wizard Hats, Crowns) scale and render directly on top of the plant's sprite.
  * **Plant Diary Sleep Screen:** A dual-pane standby screen displaying your sleeping plant alongside an RTC-synced daily achievement summary.
  * **Hardware Optimizations:** High-fidelity SD card `.bmp` asset probing, custom bezel key long-press shortcuts, and a research-backed typography engine featuring *Lexend Deca* and *Bitter*.

#### 📖🎌 [KomaOS Firmware](https://github.com/0xKnowles/KomaOS)
Manga-first e-reader firmware for the **XTEink X3 and X4**, built as a fork of CrossPoint Reader. The ESP32-C3 can't decode a full-resolution JPEG per page turn inside its ~380 KB of RAM, so KomaOS doesn't try: pages are pre-rendered off-device into 1-bit/2-bit XTC, and a page turn becomes a decode-free blit.

<p align="center">
<img height="250" alt="KomaOS boot screen" src="https://raw.githubusercontent.com/0xKnowles/KomaOS/claude/komaos-branding-manga-95dbjf/docs/images/boot-screen.png" />
<img height="250" alt="KomaOS home screen" src="https://raw.githubusercontent.com/0xKnowles/KomaOS/claude/komaos-branding-manga-95dbjf/docs/images/screens/Home.png" />
</p>

* **Two Reading Views:** Tall pages are split into overlapping landscape strips shown 1:1, or reassembled on-device into a full page for finding your place on a spread.
* **Manga-Aware Library:** Per-volume reading position, bookmarks and slice offset, LTR/RTL reading direction, chapter selection and quick page jump.
* **KomaUI Theme:** A home screen laid out as manga panels, with covers, reading stats and inked menu rows.
* **Full Reader Engine:** Keeps EPUB 2/3, hyphenation, dictionary lookups, KOReader sync, Wi-Fi transfer, OPDS, Calibre wireless and OTA updates.

#### 🧠🛰️ F.R.A.M.E. &nbsp;<img src="https://img.shields.io/badge/Private-555555?style=flat-square&logo=github&logoColor=white" alt="Private" />
**File Retrieval & Advanced Media Engine** — a self-hosted "second brain" for a seedbox media stack. Every app on the box holds one slice of the same story (requested, grabbed, downloaded, imported, playable, watched); F.R.A.M.E. polls them all, stitches the slices into one graph, and tells you exactly where any title is stuck and why.

* **One Graph, Six Apps:** Normalized adapters merge Ombi, Sonarr, Radarr, SABnzbd, Plex/Tautulli and LazyLibrarian into a single graph where every node carries a health state (healthy, stalled, failed, orphaned, cold).
* **Live 3D Visualization:** An interactive force-directed graph that updates in place over SSE as the poll loop runs.
* **Ask It Anything:** Twelve read-only tools over the graph, including lifecycle tracing, reclaim ranking and read-only SQL, with a voice "ask orb" powered by an ElevenLabs Agent.
* **Safe by Default:** Observes and explains only; optional actions are off unless enabled and need explicit approval.
* **Stack:** TypeScript, Fastify, SQLite, React, Three.js, ElevenLabs.

#### 🎮🧊 Stop 'n' Swop Restoration &nbsp;<img src="https://img.shields.io/badge/Private-555555?style=flat-square&logo=github&logoColor=white" alt="Private" />
ROM patches that restore Rare's cut **Stop 'n' Swop** feature across the N64 chain **Banjo-Kazooie → Donkey Kong 64 → Banjo-Tooie → Ocarina of Time**. The original relied on RDRAM fading slowly while you swapped cartridges; this project rebuilds the missing senders and receivers from the decomp research up.

* **Hand-Written MIPS Hooks:** Code tucked into unused ROM padding that finds the swap message, validates it with Rare's own checksum, and runs before each game clears RAM.
* **Restored Content:** DK64's Big Icy Door, fridge and Gold DK Bust, Banjo-Tooie's Ice Key handoff and Super Jiggy, and a Mega Jiggy that reaches Ocarina of Time.
* **Cart-Swap Emulator:** A patched Mupen64Plus core that dumps, reloads and decays RDRAM to simulate a real cartridge swap.
* **Desktop Launcher:** A Qt app that verifies your own ROMs, applies the `.bps` patches and lets you "Hot Swap" between games. No ROMs or game assets are ever distributed.

#### 🎙️🧪 Synapse Lab &nbsp;<img src="https://img.shields.io/badge/Private-555555?style=flat-square&logo=github&logoColor=white" alt="Private" />
An expert workbench for learning LLMs and AI coding agents — **Claude Code, OpenAI Codex and Google Antigravity** — with a voice coach that briefs you, works the screen and verifies your work.

* **Live Verification over MCP:** A zero-dependency MCP connector lets the lab see your coding agent and workspace, so lab steps turn green on their own when the work is actually done on disk.
* **Synapse, the Voice Coach:** Hold Space and talk; an ElevenLabs agent can read the current step, spotlight controls, copy commands and run checks.
* **Knowledge Base, Not a Syllabus:** A 20-question calibration, 33 briefing entries and 15 hands-on labs rewritten for each agent.
* **Living Visuals:** Synapse is rendered as a raw WebGL2 neural network of light that reacts to listening, thinking and speaking.
* **Stack:** Next.js, React, TypeScript, Tailwind, Claude API, MCP, ElevenLabs, Supabase.

#### 📚⚡ FlipNzb &nbsp;<img src="https://img.shields.io/badge/Private-555555?style=flat-square&logo=github&logoColor=white" alt="Private" />
Usenet and torrent automation for **ebooks, audiobooks and manga**, built the way Sonarr and Radarr work — because LazyLibrarian is largely unmaintained, Readarr is retired and the Goodreads API is gone.

* **Monitors Authors & Manga by Volume:** Every volume is its own wanted item that can be grabbed and upgraded.
* **Explains Every Decision:** Searches any newznab/torznab indexer plus Nyaa, and shows the exact approve/reject reasons for each release.
* **End-to-End Pipeline:** Sends to SABnzbd, NZBGet or qBittorrent, then imports, renames, upgrades and blocklists failed downloads.
* **E-Reader Conversion:** One-click manga conversion to XTC with tunable dithering and strip layout, feeding straight into KomaOS.

#### 🥋🃏 CapyDojo &nbsp;<img src="https://img.shields.io/badge/Private-555555?style=flat-square&logo=github&logoColor=white" alt="Private" />
A cosy elemental card battle game for kids on **Android**, starring capybaras. Fire, water and ice: collect a winning set before the Sensei does.

* **Unit-Tested Rules Engine:** Pure Kotlin game logic with no Android dependencies, driving a Jetpack Compose UI that stages every round as a little animated show.
* **Progression:** Nine belts, card packs, deck building, rule-bending ability cards, a Daily Dojo and a stamp book.
* **Built for Kids:** Colour-blind-friendly card shapes, an easy mode with a coach, and two-player modes on one phone.

#### 🎣 Bio Tackle Box
A dedicated, full-stack application designed for agricultural management. It streamlines digital tracking, workflows, and essential data management for specialized growing environments.
* **Stack:** TypeScript, React, and Angular framework infrastructure.

#### 💧 HydroLogix - DWC Monitor (Custom Hardware)
An automated Deep Water Culture (DWC) environmental monitor built from the ground up to track real-time reservoir metrics.
* **Hardware & Firmware:** Custom schematic capture and PCB layout routed entirely in **KiCad**.
* **Features:** Utilizes an Elegoo HC-SR04 ultrasonic sensor for precise, real-time liquid-level tracking and environmental telemetry, all housed in a custom-designed, 3D-printed enclosure.

---

### 💻 Technical Toolbelt

<table>
  <tr>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=cpp" width="48" height="48" alt="C++" />
      <br>C / C++
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=kicad" width="48" height="48" alt="KiCad" />
      <br>KiCad
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=react" width="48" height="48" alt="React" />
      <br>React
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=angular" width="48" height="48" alt="Angular" />
      <br>Angular
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=ts" width="48" height="48" alt="TypeScript" />
      <br>TypeScript
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=nodejs" width="48" height="48" alt="Node.js" />
      <br>Node.js
    </td>
  </tr>
  <tr>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=nextjs" width="48" height="48" alt="Next.js" />
      <br>Next.js
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=kotlin" width="48" height="48" alt="Kotlin" />
      <br>Kotlin
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=py" width="48" height="48" alt="Python" />
      <br>Python
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=sqlite" width="48" height="48" alt="SQLite" />
      <br>SQLite
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=docker" width="48" height="48" alt="Docker" />
      <br>Docker
    </td>
    <td align="center" width="100">
      <img src="https://skillicons.dev/icons?i=tailwind" width="48" height="48" alt="Tailwind" />
      <br>Tailwind
    </td>
  </tr>
</table>

### 🛠️ Hardware & Fabrication Capabilities
* **PCB Routing & Embedded Design:** Multilayer board layouts, physical input re-mapping, low-power display optimization, and hardware interrupt handling.
* **Rapid Prototyping:** 3D printing custom mechanical enclosures tailored to exact circuit and button configurations.
* **Telemetry & I/O:** Interfacing custom edge sensor arrays with digital frontend dashboards and embedded UI layouts.

---
