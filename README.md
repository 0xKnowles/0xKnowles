<p align="center">
  <img src="assets/0xk-logo-rounded.png" alt="0xKnowles" width="150" />
</p>

**I like building things — across hardware and software.**

I build AI agents and tooling over MCP, self-hosted media apps, e-ink reader firmware, and a shipped Android game — plus a fair bit of custom hardware. I've designed and built several PCBs, including a deep-water-culture (DWC) grow monitor, custom FlipperZero GPIO tools, and custom adapters. My background spans IT, high-volume greenhouse production and integrated pest management, and I currently work in AgTech / AI.

Everything below is something I designed and built myself.

<b>Experience</b><br>
<img src="https://img.shields.io/badge/IT%20Repair-8%20yrs-0969DA?style=flat-square" alt="IT repair, 8 years" />
<img src="https://img.shields.io/badge/Greenhouse%20Production%20%26%20IPM-5%20yrs-2EA043?style=flat-square" alt="High-volume greenhouse production and integrated pest management, 5 years" />
<img src="https://img.shields.io/badge/Now%3A%20AgTech%20%26%20AI-CSM%20%26%20Dev-8957E5?style=flat-square" alt="Currently AgTech and AI, Customer Success Manager and Developer" />

<a href="https://github.com/0xKnowles"><img src="https://img.shields.io/badge/GitHub-0xKnowles-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
<a href="https://play.google.com/store/apps/details?id=com.capydojo.app"><img src="https://img.shields.io/badge/Google_Play-CapyDojo-414141?style=for-the-badge&logo=googleplay&logoColor=white" alt="CapyDojo on Google Play" /></a>
<a href="https://synapse-lab-nu.vercel.app"><img src="https://img.shields.io/badge/Live_Demo-Synapse_Lab-FF6B5E?style=for-the-badge&logo=vercel&logoColor=white" alt="Synapse Lab live demo" /></a>

---

## Featured Work

### CapyDojo · Shipped Android game &nbsp;[![Available on Google Play](https://img.shields.io/badge/Google_Play-Available_Now-34A853?style=flat-square&logo=googleplay&logoColor=white)](https://play.google.com/store/apps/details?id=com.capydojo.app) &nbsp;[![Watch the trailer](https://img.shields.io/badge/Watch_Trailer-YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://youtu.be/2yZWOrIU67c)

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=com.capydojo.app"><img src="assets/capydojo-banner.jpg" alt="CapyDojo — available now on Google Play" width="640" /></a>
</p>

A cosy elemental card battler for Android starring capybaras — **live on Google Play**. Fire, Ice and Water clash rock-paper-scissors style (Fire beats Ice, Ice beats Water, Water beats Fire); you win a round on the higher number and a match by collecting three of one element or one of each. Work up from White Belt to Black Belt — each belt unlocking special cards, outfits, card packs and deck-ability slots — then take on the Sensei's challenge, with rule-bending ability cards like Power Up, Element Twist, Shield and Magnet.

Modes include Arcade Endless and Timed, a Daily Dojo, a Friends Tour of five characters who each play by their own house rule, and pass-and-play two-player on a single phone. There's a full collection layer — 14 outfits, 11 card backs, a binder and stamp book, and cards that wear from Near Mint to Damaged and can be sealed in graded slabs. It's built kid-first: picture tutorials and a "Show Me" walkthrough, an easy mode with Coach Capy, a half-speed explain mode, colour-blind card shapes, and no ads, no chat and no accounts. Free to play with a single one-time Full Dojo unlock.

<sub>**Kotlin** · Jetpack Compose · Android · test-driven rules engine · [Google Play](https://play.google.com/store/apps/details?id=com.capydojo.app) · [Trailer](https://youtu.be/2yZWOrIU67c)</sub>

### F.R.A.M.E. · Self-hosted media "second brain" &nbsp;<img src="https://img.shields.io/badge/private-555?style=flat-square" alt="private" />

<p align="center">
  <img src="assets/frame-banner.png" alt="F.R.A.M.E. — File Retrieval & Advanced Media Engine" width="560" />
</p>

**File Retrieval &amp; Advanced Media Engine** — a self-hosted "second brain" for a seedbox media stack. Six apps each hold one slice of every title's story (requested → grabbed → downloaded → imported → playable → watched); F.R.A.M.E. polls them all through normalized adapters (Ombi, Sonarr, Radarr, SABnzbd, Plex/Tautulli, LazyLibrarian) and stitches the slices into a single graph where every node carries a health state — healthy, stalled, failed, orphaned or cold — so you can see exactly where any download is stuck and why.

It serves a live force-directed 3D view that updates in place over SSE, twelve read-only query tools (lifecycle tracing, reclaim ranking, read-only SQL) and a voice "ask orb" powered by an ElevenLabs agent. Safe by default: it observes and explains only — any optional action is off unless enabled and needs explicit approval.

<p align="center">
  <img src="assets/frame-graph.png" alt="F.R.A.M.E. live 3D media graph with the voice ask-orb" height="380" />
</p>

<sub>**TypeScript** · Fastify · SQLite · React · Three.js · ElevenLabs · observe-only by default</sub>

### Synapse Lab · Hands-on workbench for AI coding agents &nbsp;<img src="https://img.shields.io/badge/private-555?style=flat-square" alt="private" /> &nbsp;[![live](https://img.shields.io/badge/live-demo-FF6B5E?style=flat-square)](https://synapse-lab-nu.vercel.app)

<p align="center">
  <img src="assets/synapse-lab-banner.png" alt="Synapse Lab" width="560" />
</p>

An expert workbench for learning LLMs and AI coding agents (Claude Code, OpenAI Codex, Google Antigravity) with a voice coach that briefs you, works the screen and verifies your work. A zero-dependency MCP connector lets the lab see your agent and workspace, so lab steps turn green on their own when the work is genuinely done on disk.

<sub>**Next.js** · React · TypeScript · Tailwind · Claude API · MCP · ElevenLabs · Supabase</sub>

### [KomaOS](https://github.com/0xKnowles/KomaOS) · Manga-first e-reader firmware

Firmware for the XTEink X3/X4 (ESP32-C3) built so a page turn never decodes a JPEG. With only ~380&nbsp;KB of RAM, pages are pre-rendered off-device into 1-bit/2-bit XTC and a turn becomes a decode-free blit — tall pages split into 1:1 strips or reassemble into a full spread, over a reader engine that keeps EPUB, dictionary lookups, KOReader sync and OTA updates.

<p align="center">
  <img height="230" alt="KomaOS boot screen" src="https://raw.githubusercontent.com/0xKnowles/KomaOS/master/docs/images/boot-screen.png" />
  <img height="230" alt="KomaOS home screen" src="https://raw.githubusercontent.com/0xKnowles/KomaOS/master/docs/images/screens/Home.png" />
</p>

<sub>**C++** · ESP-IDF / Arduino-ESP32 · E-Ink · constrained-memory rendering</sub>

### [Ruby](https://github.com/0xKnowles/Ruby) · Passive RF signal analyzer firmware

Custom firmware that turns an XTEink e-ink reader into a stealthy, long-battery-life passive RF analyzer. Receive-only 802.11 monitor-mode sniffing (beacons, probe requests, WPA handshake detection) and BLE scanning, written to AES-256-GCM encrypted on-device logs — fronted by "Ruby," a small companion creature whose mood tracks what the radio is hearing.

<p align="center">
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/excited.bmp" width="70" alt="Ruby, excited" />
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/curious.bmp" width="70" alt="Ruby, curious" />
  <img src="https://raw.githubusercontent.com/0xKnowles/Ruby/claude/pocket-cryptid-firmware-a7td6q/bmp/content.bmp" width="70" alt="Ruby, content" />
</p>

<sub>**C++** · ESP32 · 802.11 / BLE · AES-256-GCM · `.pcap` export</sub>

### [CrossPlant](https://github.com/0xKnowles/CrossPlant) · Reading-driven firmware companion

An open-source firmware fork for the XTEink X3/X4 that merges CrossInk's typography and performance work with a re-engineered virtual plant companion. Plant vitals decay in real time and evolve down Scholar, Balanced or Wild branches based on actual reading habits, backed by a Dew Drops reward economy, a cosmetics shop and a research-backed typography engine.

<sub>**C++** · ESP32 · E-Ink · SD-backed asset rendering</sub>

### Stop 'n' Swop Restoration · N64 ROM research &nbsp;<img src="https://img.shields.io/badge/private-555?style=flat-square" alt="private" />

<p align="center">
  <img src="assets/stopnswop-emblem.jpg" alt="Stop 'n' Swop Restoration emblem" width="210" />
  &nbsp;&nbsp;
  <img src="assets/stopnswop-mascot.jpg" alt="Stop 'n' Swop Restoration mascot" width="210" />
</p>

ROM patches that restore Rare's cut *Stop 'n' Swop* feature across the Banjo-Kazooie → DK64 → Banjo-Tooie → Ocarina of Time chain, rebuilding the missing senders and receivers from decomp research up. Hand-written MIPS hooks tucked into unused ROM padding, a patched Mupen64Plus core that decays RDRAM to emulate a real cartridge swap, and a Qt launcher that applies `.bps` patches to your own ROMs — no game assets are ever distributed.

<sub>**MIPS assembly** · C++ · Qt · decomp / reverse engineering</sub>

### FlipNzb · Usenet &amp; torrent automation for books &nbsp;<img src="https://img.shields.io/badge/private-555?style=flat-square" alt="private" />

Sonarr/Radarr-style automation for ebooks, audiobooks and manga — built because LazyLibrarian is unmaintained and Readarr is retired. Monitors authors and manga per volume, searches any newznab/torznab indexer plus Nyaa with transparent approve/reject reasons, and runs the full grab → import → rename → upgrade pipeline, including one-click manga conversion that feeds straight into KomaOS.

<sub>**TypeScript** · Node.js · SABnzbd / NZBGet / qBittorrent</sub>

---

## Tech

<p>
  <b>Languages</b><br>
  <img src="https://skillicons.dev/icons?i=ts,js,cpp,kotlin,py" alt="TypeScript, JavaScript, C/C++, Kotlin, Python" />
</p>

<p>
  <b>Frameworks &amp; UI</b><br>
  <img src="https://skillicons.dev/icons?i=react,nextjs,angular,nodejs,tailwind" alt="React, Next.js, Angular, Node.js, Tailwind" />
</p>

<p>
  <b>Data &amp; Infra</b><br>
  <img src="https://skillicons.dev/icons?i=sqlite,docker,supabase,vercel" alt="SQLite, Docker, Supabase, Vercel" />
</p>

<p>
  <b>Embedded &amp; Hardware</b><br>
  <img src="https://skillicons.dev/icons?i=cpp,arduino,raspberrypi" alt="C++, Arduino, embedded" />
  &nbsp;<sub>ESP32 / ESP-IDF · FreeRTOS · E-Ink · schematic capture &amp; PCB layout in <b>KiCad</b></sub>
</p>

---

<p align="center">
  <sub>Embedded firmware · full-stack TypeScript · AI agents &amp; MCP · custom hardware &amp; AgTech</sub>
</p>
