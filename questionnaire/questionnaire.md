# SUB-CHECK: Customer Development (CustDev) Questionnaire & Methodology

**Project:** SUB-CHECK — Cloud-Based Behavioral Anti-Cheat Detection  
**Course:** Technology Entrepreneurship — Assignment 3  
**Authors:** Nurzhan Bekmurat, Azamat Yermukhan, Yernur Khuan  

---

## 1. Objectives of the Customer Development Study

1. **Problem Validation:** Confirm the severity and frequency of cheating in competitive games, and assess dissatisfaction with existing anti-cheat systems (e.g., kernel-level access, performance degradation, privacy concerns, platform limitations).
2. **Customer Jobs Identification:** Understand what players, server admins, and indie studios are trying to accomplish when dealing with game integrity.
3. **Pain Points & Gain Drivers:** Uncover the exact pain points (false bans, privacy invasion, hardware cheat evasion like DMA/Cronus) and desired gains (seamless cross-platform play, transparent trust metrics).
4. **Value Proposition Validation:** Test hypotheses surrounding server-side behavioral analytics, privacy-preserving telemetry, and risk-scoring mechanisms without leading the respondent.

---

## 2. Target Audience Segmentation & Prioritization

| Segment | Description | Accessibility (1-5) | Market Volume (1-5) | Impact/Satisfaction (1-5) | Priority Rank |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Segment A: Competitive & Ranked Gamers** | Active players in ranked FPS/competitive games (CS2, Valorant, Apex, Rainbow Six). Concerned with fair play and intrusive software. | 5 (High - peers, Discord, Steam) | 5 (Massive - millions) | 4 (High demand for fair matches) | **P1 (Primary)** |
| **Segment B: Community Admins & Tournament Hosts** | Organizers of collegiate, amateur, and semi-pro tournaments; Discord clan admins; FACEIT/Fastcup players. | 4 (Medium-High - gaming communities, universities) | 3 (Moderate) | 5 (Critical - direct liability for fair play) | **P2 (Secondary)** |
| **Segment C: Indie & Mid-Tier Game Developers** | Small studios and solo developers building multiplayer games who cannot afford proprietary anti-cheat licenses. | 3 (Moderate - itch.io, Reddit /r/gamedev) | 3 (Niche but growing) | 5 (Extremely high - no viable current options) | **P3 (Strategic)** |

---

## 3. CustDev Interview Rules & Best Practices

- **Follow "The Mom Test" framework:** Ask about specific past behavior, not hypothetical future promises.
- **Do not pitch the solution early:** Let the respondent describe their experiences, emotions, and workarounds first.
- **Listen actively:** Avoid correcting or arguing with respondents. Keep questions neutral.
- **Duration:** 15–20 minutes per in-depth interview or 5–7 minutes for structured written survey forms.

---

## 4. Interview Script & Question Bank

### Part 1: Screener & Profile (1–2 minutes)
1. What competitive multiplayer games do you play most frequently, and at what competitive level (casual, ranked, semi-pro, tournament)?
2. How many hours per week do you spend playing or managing multiplayer game environments?
3. What platforms/operating systems do you play on (Windows 10/11, Linux, SteamOS / Steam Deck, macOS)?

### Part 2: Customer Jobs & Experience with Cheating (4–5 minutes)
4. Tell me about the last time you encountered a cheater in a match. How did you identify it, and how did it affect your experience?
5. How frequently do you feel you run into illegitimate players (aimbots, wallhacks, triggerbots, recoil scripts)?
6. When you suspect someone of cheating, what actions do you take (in-game report, leave game, review replay, complain on forums)? How effective do those actions feel?

### Part 3: Customer Pains — Current Anti-Cheat Frustrations (5–6 minutes)
7. Which anti-cheat software do you currently have installed (e.g., Riot Vanguard, Easy Anti-Cheat, BattlEye, VAC)?
8. What is your opinion on kernel-level (Ring 0) anti-cheat systems running on your personal computer?
   - *Probing:* Have you experienced system crashes (BSOD), performance drops, boot issues, or privacy concerns?
9. Have you or anyone you know ever been falsely flagged or temporarily banned by an anti-cheat system? How was the appeal handled?
10. Have you heard of hardware cheats (DMA cards, mouse macros, Cronus Zen)? Do you feel existing anti-cheats can stop them?

### Part 4: Customer Gains & Solution Hypotheses (4–5 minutes)
11. If you could change one thing about how anti-cheat operates today, what would that be?
12. If a game used a **server-side anti-cheat** that requires **zero software installation on your PC** and analyzes kinematic behavioral telemetry (e.g. mouse movement physics and reaction mechanics) instead of scanning your files:
   - What would be your immediate reaction?
   - What concerns, if any, would you have about such an approach?
13. How important is it for you to play games on Linux, Steam Deck, or virtualized environments without being blocked by anti-cheat?

### Part 5: Wrap-up & Follow-up (1 minute)
14. Is there anything else about game security or fair play that you think we should know?
15. Would you be willing to test a prototype or review telemetry samples in a follow-up session?
