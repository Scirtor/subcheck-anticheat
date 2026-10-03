# Customer Development Interview Notes: Key Representative Sessions

**Project:** SUB-CHECK — Cloud-Based Behavioral Anti-Cheat Detection  
**Course:** Technology Entrepreneurship — Assignment 3  
**Interviewers:** Nurzhan Bekmurat, Azamat Yermukhan, Yernur Khuan  

---

## Session 1: Competitive FPS Player (CS2 Premier 19k Rating)
- **Respondent:** R01 (Daniyar K., 22 y/o, Student & Semi-pro CS2 Player)
- **Channel:** Discord Voice Call (25 minutes)
- **Primary Game:** Counter-Strike 2 (18 hrs/week), Windows 11
- **Key Quotes:**
  > *"VAC Live is practically non-existent. You meet spinbots and people tracking through walls in 18k+ rating every third match. The only alternative is FACEIT, but having kernel drivers running 24/7 on my PC makes me uncomfortable because I use this PC for university and banking."*
- **Jobs:** Win ranked matches, improve Elo, play without wondering if the opponent is closet cheating.
- **Pains:** High prevalence of subtle aim assist and wallhacks; slow response time of report system; frustration with invasive third-party kernel drivers.
- **Feedback on SUB-CHECK:**
  - *"If the game server can detect impossible micro-adjustments or humanly impossible reaction times under 80ms without installing anything on my SSD, I would 100% choose that game over one that requires rootkit drivers."*
  - Expressed concern about false positives on high-sensitivity flick shots, emphasized need for confidence thresholds.

---

## Session 2: Tournament Host & Collegiate Esports Organizer
- **Respondent:** R07 (Arsen M., 26 y/o, Esports League Coordinator)
- **Channel:** Zoom Call (30 minutes)
- **Scope:** Runs inter-university CS2 and Valorant cups (over 40 teams per season)
- **Key Quotes:**
  > *"Our biggest nightmare is DMA (Direct Memory Access) cards. Wealthier players buy a second PC with a PCIe FPGA card that reads game memory over hardware. No client-side anti-cheat catches this because the cheat runs on an entirely different machine. We have to manually review demos for hours."*
- **Jobs:** Ensure competitive integrity in online qualifiers; minimize dispute resolution time; prevent scandals.
- **Pains:** Hardware cheats bypassing client-side memory inspection; admin burnout from manual demo reviews; accusations between teams.
- **Feedback on SUB-CHECK:**
  - *"A server-side behavioral model is the ONLY way to catch DMA cheats, because even if the cheat is on a secondary computer, the player's physical mouse input or impossible reaction flick must pass through the server. If SUB-CHECK gave us an automated cheat probability report on match replays, it would save us 15 hours every weekend."*

---

## Session 3: Indie Multiplayer Game Developer
- **Respondent:** R08 (Maxim V., 29 y/o, Lead Dev at Indie Studio)
- **Channel:** Google Meet (25 minutes)
- **Scope:** Developing an indie tactical arena shooter on Unreal Engine 5
- **Key Quotes:**
  > *"When we reached out to enterprise anti-cheat vendors like BattlEye and Easy Anti-Cheat, the licensing models and integration overhead were completely unrealistic for our budget. They cater to AAA publishers. Indie games either ship with zero anti-cheat and get ruined by cheaters in week two, or spend months building basic speedhack checks."*
- **Jobs:** Protect game economy and Steam user reviews from day 1; maintain affordable operational costs; support Steam Deck / Linux players.
- **Pains:** Enterprise anti-cheats priced out of reach ($10k-$50k minimum commitments); complex C++ driver integrations; losing the growing Steam Deck market if kernel anti-cheat breaks Proton.
- **Feedback on SUB-CHECK:**
  - Strongly validated the SaaS pricing model based on Monthly Active Users (MAU).
  - Emphasized that server-side telemetry via a lightweight REST/WebSocket SDK would make integration take days instead of months.

---

## Session 4: Linux & Steam Deck Competitive Gamer
- **Respondent:** R14 (Alibek S., 24 y/o, Software Engineer & Gamer)
- **Channel:** Telegram Call (20 minutes)
- **Primary OS:** Fedora Linux / Arch Linux / Steam Deck
- **Key Quotes:**
  > *"Kernel-level anti-cheats like Vanguard and EA's new anti-cheat fundamentally treat Linux users as second-class citizens or outright cheaters. I cannot play League of Legends or Battlefield anymore simply because I don't run Windows. It's ridiculous when the server could just check physics."*
- **Jobs:** Play games natively or through Proton on Linux without maintaining a dual-boot Windows partition.
- **Pains:** Forced dual-booting; fear of rootkit vulnerabilities; anti-cheat updates breaking Proton compatibility overnight.
- **Feedback on SUB-CHECK:**
  - Highly enthusiastic: *"A server-side solution is completely OS-agnostic. It doesn't care whether client packets originate from Windows, Linux, or a Steam Deck, because it inspects kinematic vectors, not OS memory."*

---

## Session 5: Community Server Administrator
- **Respondent:** R12 (Timur B., 27 y/o, Admin of Rust / CS Community Hub)
- **Channel:** Discord Voice Call (20 minutes)
- **Scope:** Manages 4 dedicated 128-tick servers with ~400 daily peak players
- **Key Quotes:**
  > *"Recoil scripts and soft-aim are sold openly for $5 on Telegram. Client-side scans miss them because they emulate legitimate mice hardware (like Arduino / Razer Synapse macros). We need algorithmic recoil variance detection that calculates jerk and standard deviation on crosshair movement."*
- **Jobs:** Maintain clean, active servers with high player retention; filter out malicious players automatically.
- **Pains:** Client anti-cheat bypasses; constant player complaints in Discord tickets; server lag caused by bloated server plugins.
- **Feedback on SUB-CHECK:**
  - Suggested a plugin for CS2/dedicated server binaries that pushes telemetry chunks to a cloud inference endpoint.
