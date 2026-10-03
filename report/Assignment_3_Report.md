# Assignment 3: Customer Development (CustDev) Report

**Course:** Technology Entrepreneurship  
**Project:** SUB-CHECK — Cloud-Based Behavioral Anti-Cheat Platform  
**Team Members:** Nurzhan Bekmurat, Azamat Yermukhan, Yernur Khuan  
**Repository:** [https://github.com/Scirtor/subcheck-anticheat](https://github.com/Scirtor/subcheck-anticheat)  

---

## 1. Executive Summary

This report documents the Customer Development (CustDev) research conducted for **SUB-CHECK**, a server-side behavioral anti-cheat platform. The objective of this research was to validate whether the competitive gaming ecosystem—specifically competitive players, tournament organizers, and independent game studios—experiences acute friction with existing kernel-level (Ring 0) anti-cheat solutions, and whether an agentic server-side behavioral telemetry approach fulfills their customer jobs, pains, and desired gains.

Over a two-week period, our team gathered and analyzed data from **32 respondents** across three target segments via structured questionnaires, supplemented by **5 in-depth recorded interview sessions**. The findings strongly validate our foundational problem hypotheses while unveiling critical new market insights regarding hardware cheats (DMA/Cronus), Linux/SteamOS platform lockouts, and the prohibitive licensing barriers faced by indie multiplayer studios.

---

## 2. Target Audience Segmentation & Prioritization

To conduct disciplined Customer Development, we segmented our potential customer ecosystem into three distinct groups based on accessibility, market volume, and potential satisfaction/impact:

| Segment | Description | Accessibility (1-5) | Market Volume (1-5) | Impact / Need (1-5) | Priority Rank |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Segment A: Competitive & Ranked Gamers** | Active players in ranked FPS games (CS2, Valorant, Apex Legends, R6 Siege) playing >10 hrs/week. | 5 (High — Discord, Reddit, peers) | 5 (Massive — tens of millions) | 4 (Directly impacted by cheaters & rootkits) | **P1 (Primary)** |
| **Segment B: Community Admins & Tournament Hosts** | Organizers of collegiate esports, amateur tournament brackets, and dedicated community servers. | 4 (Medium-High — university clubs, clan hubs) | 3 (Moderate — thousands of organizers) | 5 (Critical — manual demo reviews cause burnout) | **P2 (Secondary)** |
| **Segment C: Indie & Mid-Tier Game Studios** | Developers building commercial multiplayer titles without multimillion-dollar R&D budgets. | 3 (Moderate — itch.io, indie discords) | 3 (Growing segment — thousands of studios) | 5 (Extremely high — enterprise AC is unaffordable) | **P3 (Strategic B2B)** |

---

## 3. Customer Discovery Methodology

Our interview preparation strictly followed *The Mom Test* principles: we avoided pitching our hypothetical solution prematurely, focused on past behavior, and probed deeply into frustrations, workarounds, and economic costs.

- **Jobs to be Done (JTBD):**
  - **Gamers:** Enjoy fair, competitive matches and preserve system stability and personal privacy.
  - **Tournament Organizers:** Certify competitive integrity swiftly and eliminate cheat scandals.
  - **Game Developers:** Protect early-access player retention and Steam user reviews without blowing their R&D budget.
- **Pains Explored:** High cheater encounter rates, false positive bans, intrusive kernel drivers causing BSODs and security concerns, hardware cheats (DMA cards, Cronus) bypassing client scans, and OS incompatibility (Linux/SteamOS).
- **Gains Explored:** Transparent risk scoring, zero client installation, seamless cross-platform play, and automated demo analysis.

---

## 4. Quantitative & Statistical Findings

Analysis of our 32 structured respondents (recorded in `questionnaire/responses.csv` and modeled in `analysis/analysis.xlsx`) reveals decisive trends:

- **62.5%** of respondents expressed an explicitly **Negative** perception toward kernel-level (Ring 0) anti-cheat systems, citing privacy invasion, boot crashes, and performance degradation.
- **93.8%** expressed a **Positive or Extremely Positive** attitude toward a server-side behavioral anti-cheat that requires zero client-side installation.
- **78.1%** encounter suspected or blatant cheaters **at least several times a week**, with **40.6%** encountering them on a **daily** basis.
- **87.5%** stated they would eagerly participate in a pilot testing program for SUB-CHECK.

Visual charts generated from the empirical dataset:
- Figure 1: [Audience Segment Distribution](../analysis/charts/respondent_segment_distribution.png)
- Figure 2: [Kernel Anti-Cheat Sentiment](../analysis/charts/sentiment_kernel_anticheat.png)
- Figure 3: [Receptiveness to Server-Side Behavioral Anti-Cheat](../analysis/charts/attitude_towards_serverside.png)
- Figure 4: [Cheater Encounter Frequency](../analysis/charts/cheater_encounter_frequency.png)
- Figure 5: [Willingness to Pilot](../analysis/charts/willingness_to_pilot.png)

---

## 5. Key Insights & Customer Quotes

> **R07 (Esports League Coordinator):** *"Our biggest nightmare is DMA (Direct Memory Access) cards. Wealthier players buy a second PC with a PCIe FPGA card that reads game memory over hardware. No client-side anti-cheat catches this because the cheat runs on an entirely different machine... A server-side behavioral model is the ONLY way to catch DMA cheats."*

> **R08 (Indie Game Developer):** *"When we reached out to enterprise anti-cheat vendors like BattlEye and Easy Anti-Cheat, the licensing models and integration overhead were completely unrealistic for our budget ($10k+ minimum commitment). Small studios are forced to ship unprotected games."*

> **R14 (Linux / Steam Deck Gamer):** *"Kernel anti-cheats treat Linux users like criminals. I was locked out of my favorite games overnight. A server-side solution doesn't care whether client packets originate from Windows or Linux because it inspects kinematics, not OS memory."*

### Key Inferences:
1. **The Hardware Cheat Blindspot:** Traditional client anti-cheats rely on OS memory scanning, leaving them blind to DMA hardware and external microcontrollers (e.g. Arduino mice). In contrast, physical mouse kinematics and human neuromotor limits cannot be forged on the server.
2. **The Linux / Handheld Opportunity:** Over 15% of respondents actively play on Linux or Steam Deck. Server-side verification provides a major competitive moat through 100% platform neutrality.
3. **Indie Studio Accessibility Barrier:** Enterprise solutions have priced out indie and AA studios. A self-serve SaaS API priced per Monthly Active User (MAU) fills a massive market vacuum.

---

## 6. Business Idea & Product Updates (Value Proposition Canvas)

Based on the CustDev findings, we updated our business model and feature roadmap:

| Dimension | Initial Idea (Pre-CustDev) | Updated Model (Post-CustDev) | CustDev Rationale |
| :--- | :--- | :--- | :--- |
| **Primary Customer** | B2C Gamers via a desktop companion app. | **B2B SaaS for Indie/Mid-tier Studios & Tournament Organizers.** | Players cannot mandate anti-cheat adoption; developers and organizers have the buying power and direct liability. |
| **Pricing Strategy** | Flat annual enterprise license. | **Tiered usage-based pricing ($0.03 – $0.07 per MAU) with a free indie tier.** | Indie developers strongly requested low barrier to entry and predictable scaling costs. |
| **Core Value Prop** | General memory exploit detection. | **Specialized Kinematic Telemetry Engine for DMA & Recoil Macro detection.** | DMA and hardware macros were identified as the #1 unsolvable threat by esports hosts. |
| **Enforcement Model** | Instant binary bans. | **Continuous Risk Scoring (0.0 - 1.0) with Quarantine Matchmaking.** | Gamers and developers voiced intense fear of false bans; quarantine matchmaking prevents game disruption while evidence accumulates. |

---

## 7. Conclusion

Assignment 3 successfully validated the business opportunity for **SUB-CHECK**. The market is actively seeking alternatives to invasive kernel drivers, and tournament organizers and indie studios represent high-urgency B2B adopters. The SUB-CHECK team will now progress toward building the kinematic feature extraction pipeline and executing our initial pilot trials.
