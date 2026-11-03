# 0xKnowles

**Embedded firmware, self-hosted platforms and applied AI.**

I build software that runs close to the hardware and close to the people using it: firmware for
380 KB microcontrollers, self-hosted services that make other services observable, and AI tools
that teach and act through the Model Context Protocol. My background is in IT infrastructure, with
deep experience in Integrated Pest Management (IPM) and greenhouse automation.

Several of the projects below are private. They are described here with a
![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) badge and no link;
I am happy to walk through any of them on request.

---

## Projects at a glance

| Project | Area | What it is | Stack | |
|---|---|---|---|---|
| [**KomaOS**](https://github.com/0xKnowles/KomaOS) | Embedded | Manga-first e-reader firmware for ESP32-C3 Xteink devices | C++, ESP32-C3, PlatformIO | ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square) |
| [**Ruby**](https://github.com/0xKnowles/Ruby) | Embedded | Passive RF signal analyzer firmware for e-ink readers | C++, ESP32-C3, 802.11/BLE | ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square) |
| [**CrossPlant**](https://github.com/0xKnowles/CrossPlant) | Embedded | E-reader firmware with a reading-driven virtual plant companion | C++, ESP32-C3, PlatformIO | ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square) |
| **F.R.A.M.E.** | Self-hosted | Observability graph and voice-queryable "second brain" for a media server stack | TypeScript, Fastify, SQLite, Three.js | ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) |
| **FlipNzb** | Self-hosted | Usenet and torrent automation for ebooks, audiobooks and manga | TypeScript, Fastify, React, Docker | ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) |
| **Synapse Lab** | Applied AI | Hands-on lab for learning LLMs and AI coding agents, with a voice coach | Next.js, Claude API, MCP, ElevenLabs | ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) |
| **Stop 'n' Swop Restoration** | Reverse engineering | ROM patches that restore a cut cross-game feature across four N64 titles | MIPS assembly, Python, C | ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) |
| **CapyDojo** | Mobile | Elemental card battle game for Android | Kotlin, Jetpack Compose | ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square) |

---

## Embedded firmware

All three firmwares target the Xteink X3 and X4 e-ink readers: a single-core RISC-V ESP32-C3 at
160 MHz with about 380 KB of usable RAM, no PSRAM and one 48 KB framebuffer.

### [KomaOS](https://github.com/0xKnowles/KomaOS) ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square)

A manga-focused fork of CrossPoint Reader. The device cannot decode a full-resolution JPEG per page
turn inside its RAM budget, so KomaOS moves that work off-device: pages are pre-rendered to 1-bit or
2-bit XTC/XTCH at panel resolution, and a page turn becomes a decode-free blit.

- Two reading views: tall pages split into overlapping landscape strips at 1:1, or reassembled on
  the device into a full page using split geometry recorded in the file.
- Per-volume reading position, bookmarks and slice offset; LTR/RTL control; a custom KomaUI theme.
- Keeps the full EPUB engine, Wi-Fi transfer, OPDS, Calibre wireless, KOReader sync and OTA updates.

### [Ruby](https://github.com/0xKnowles/Ruby) ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square)

Turns the reader into a long-battery-life, receive-only RF signal analyzer.

- 802.11 monitor-mode capture (beacons, probe requests, WPA handshake detection) and passive BLE
  advertisement scanning.
- Deduplicated observations written to an AES-256-GCM encrypted daily log, decryptable on the device.
- `.pcap` handshake export for offline auditing; any active capability is off by default and gated
  behind an explicit allow/deny list.

### [CrossPlant](https://github.com/0xKnowles/CrossPlant) ![Public](https://img.shields.io/badge/-Public-2ea043?style=flat-square)

Merges the typography and performance work of CrossInk with a re-engineered virtual plant system
descended from CrossPet.

- Plant stats decay in real time and evolve along branches driven by actual reading habits and streaks.
- An in-firmware reward economy, accessory shop and sprite compositing on the e-ink canvas.
- An RTC-synced sleep screen summarising the day's reading.

---

## Self-hosted platforms

### F.R.A.M.E. ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square)

*File Retrieval & Advanced Media Engine.* Every app in a media server stack holds one slice of the
same story: one knows a title was requested, another that it was grabbed, another that it
downloaded, imported, became playable or was watched. F.R.A.M.E. polls all of them, stitches the
slices into a single graph and makes the whole lifecycle traceable.

- Normalised adapters for six services, merged into one graph with a health state on every node
  (healthy, pending, stalled, failed, orphaned, cold).
- Lifecycle tracing that names the stage an item is stuck at and the reason from the specific app;
  storage reclaim ranking by bytes per play.
- Interactive 3D force-directed visualisation, updated live over SSE.
- A natural-language and voice interface (ElevenLabs agent) backed by twelve read-only tools,
  including relationship walking and read-only SQL. Write actions are opt-in and require approval.
- Conservative joins by design: a missing edge shows an honest break instead of a confident false link.

**Stack:** TypeScript, Fastify, SQLite, zod, React, Three.js / react-force-graph, ElevenLabs.

### FlipNzb ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square)

Usenet and torrent automation for ebooks, audiobooks and manga, built the way Sonarr and Radarr
work. It exists because the incumbents stopped working: LazyLibrarian is largely unmaintained,
Readarr is retired and the Goodreads API is gone.

- Monitors authors and series, with manga tracked per volume as its own wanted item.
- Searches any newznab/torznab indexer plus Nyaa, and explains every approve/reject decision.
- Sends to SABnzbd, NZBGet or qBittorrent, then imports, renames, upgrades and blocklists failures.
- A library browser with an in-browser reader, and one-click manga conversion to XTC for e-readers,
  feeding straight into KomaOS.

**Stack:** TypeScript, Fastify, SQLite, React, TanStack Query, sharp, Docker.

---

## Applied AI

### Synapse Lab ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square)

A lab console for experienced engineers getting fluent in AI. A calibration quiz maps what you
already know; you then pull up any of 33 knowledge-base entries, get briefed, and run the matching
hands-on lab in Claude Code, OpenAI Codex or Google Antigravity.

- **Live verification:** a zero-dependency MCP connector lets the lab see the learner's agent and
  workspace, so steps turn green when the work is actually done on disk. Read-only and localhost-only.
- **Voice coach:** an ElevenLabs agent with client tools that can read the current step, spotlight
  controls, copy commands and run verifications.
- Per-agent lesson variants, a remote MCP endpoint for the Claude app on phones, invite-only
  accounts with Google sign-in, and a raw WebGL2 shader for the animated coach.

**Stack:** Next.js, React, TypeScript, Tailwind, Claude API, Model Context Protocol, ElevenLabs,
Supabase, WebGL2.

---

## Reverse engineering

### Stop 'n' Swop Restoration ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square)

Rare's Stop 'n' Swop was meant to pass items between N64 games by leaving a checksummed message in
RAM, relying on RDRAM fading slowly while cartridges were swapped. It was cut before release. This
project restores the chain as ROM patches: **Banjo-Kazooie → Donkey Kong 64 → Banjo-Tooie →
Ocarina of Time**.

- Hand-written MIPS hooks placed in unused ROM padding, which find and validate the message with
  Rare's own checksum before the game clears RAM.
- Restored and new in-game content in each title, built from the player's own ROM so no game
  assets are distributed.
- A patched Mupen64Plus core that simulates the swap (RDRAM dump, reload and bit decay), plus a Qt
  desktop launcher that verifies ROMs, applies `.bps` patches and checks every output against a
  tested build hash.

**Stack:** MIPS assembly, Python, C, Qt, Mupen64Plus.

---

## Mobile

### CapyDojo ![Private](https://img.shields.io/badge/-Private-6e7681?style=flat-square)

An elemental card battle game for young players on Android. A pure-Kotlin rules engine, fully unit
tested and independent of Android, drives a Jetpack Compose UI that stages each round as a short
animated scene.

- Nine-belt progression with an adaptive opponent, card packs, deck building and rule-bending
  ability cards.
- Accessibility built in: every card colour also has its own shape, and an easy mode for the
  youngest players.
- Local two-player modes and a drop-in asset system where every image and sound is a named slot.

**Stack:** Kotlin, Jetpack Compose, Android.

---

## Earlier work

- **HydroLogix:** a Deep Water Culture reservoir monitor with schematic and PCB designed in KiCad,
  ultrasonic level sensing and a custom 3D-printed enclosure.
- **Bio Tackle Box:** a full-stack application for tracking workflows and data in specialised
  growing environments (TypeScript, React, Angular).

---

## Technical toolbelt

| Area | Tools |
|---|---|
| Languages | C / C++, TypeScript, Kotlin, Python, MIPS assembly |
| Embedded | ESP32-C3 (RISC-V), PlatformIO, FreeRTOS, e-ink displays, KiCad PCB design |
| Web and services | Node.js, Fastify, Next.js, React, Angular, SQLite, Supabase, Docker |
| AI | Claude API, Model Context Protocol, ElevenLabs Agents |
| Mobile | Android, Jetpack Compose |
