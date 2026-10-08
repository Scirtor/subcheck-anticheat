# SUB CHECK Customer Development

Technology Entrepreneurship • Assignment 3 • Group CS-2406

Nurzhan Bekmurat, Azamat Yermukhan, Yernur Khuan

8 October 2026

## Executive summary

SUB-CHECK is a proposed B2B service for independent and AA studios operating competitive shooters. It would analyse aiming behaviour from authoritative game servers, return a risk score with supporting events, and help moderators review suspicious cases alongside existing anti-cheat tools.

Our customer development study provides an early signal of a relevant problem and interest in the concept. In the survey, 17 of 19 participants rated cheating seriousness at 4 or 5, and 16 of 20 rated the proposed server-side system’s usefulness at 4 or 5. Respondents nevertheless highlighted detection accuracy, false positives and telemetry privacy. These findings support a controlled pilot, rather than a claim of proven demand or technical effectiveness.

The updated idea retains a studio customer and human enforcement decisions. It adds a self-hosted option for evaluation, explicit telemetry controls, a free pilot and evidence about detection quality. Deployment preferences in the technical section favour self-hosting (6 of 9). Pricing responses favour a free or open-source core with paid cloud services (12 of 20), but this mixed audience does not establish a studio budget or willingness to pay.

## Research scope

| Evidence | Available material |
| --- | --- |
| Online survey | 20 participants shown in Google Forms summaries; 27 screenshots, including 2 repeats |
| Recorded interviews | 3 supplied recordings; analysed separately from survey totals |
| Question-specific bases | 19 for seriousness and satisfaction; 9 for technical questions; otherwise 20 |
| Assignment minimum | 30 online respondents OR 5 face-to-face recorded video interviews. The current evidence is below both thresholds. |

We do not add interview participants to the survey total because overlap is unknown. The results describe this sample and guide the next experiments. They do not estimate the wider gaming market.

# Audience and interview preparation

## Segmentation and priority

We distinguish the buyer, the operational user and the player affected by enforcement. The scoring below is a team judgement for recruitment planning, on a 1–5 scale. Volume scores are relative estimates, not measured market sizes. Buyer relevance takes precedence when choosing the next interviews.

| Segment | Access | Volume | Benefit | Priority |
| --- | --- | --- | --- | --- |
| Indie or AA shooter studio leads | 3 | 3 | 5 | 1 for purchase validation |
| Server moderators and tournament administrators | 4 | 3 | 5 | 2 for workflow validation |
| Active competitive players | 5 | 5 | 4 | 1 for accessible problem discovery |

The reachable survey sample differs from this intended market. Roles are multiple selection: 10 of 20 selected cybersecurity specialist/student, 7 software developer, 7 casual gamer, 3 competitive gamer, 2 game developer, and none esports organiser/admin. Nine reported experience developing, managing, moderating or hosting a multiplayer game/server. Those nine are a technical-experience subgroup, not nine confirmed studio buyers.

## Research objectives and question design

Our objectives were to identify customer jobs, pains and desired gains, test reactions to server-side risk scoring, and explore integration and business-model preferences. The questionnaire separates respondent background, cheating experiences, existing solutions, kernel access, the SUB-CHECK concept, risk scoring, technical integration, pricing and final feedback.

Problem questions ask about actual cheating encounters and experience managing games. Concept, trust and pricing questions capture stated preferences after presenting the idea. They are useful for prioritisation but can encourage agreeable answers and do not demonstrate behaviour, purchasing intent or technical results.

## Interview guide and recruitment plan

For follow-up interviews, ask everyone about the same core topics before describing SUB-CHECK: their role and recent game; the last suspected cheating incident; what they did; time spent reviewing or appealing; the current tools and their shortcomings; and what outcome would improve their work. Ask technical leads about a recent integration, its effort, data restrictions and actual budget authority. Only then show the concept and ask what evidence would justify a pilot.

Recruit studio leads through existing developer contacts and small multiplayer communities, moderators through server communities, and competitive players through peers. These are proposed channels, not a record of how the existing respondents were recruited. Record permission, role, duration and the source reference. Aim for 15–30 minutes, with neutral probes, no argument and no sales pitch.

# Cheating problems and existing alternatives

## Observed problem

| Question and base | Result | Interpretation |
| --- | --- | --- |
| Cheating seriousness, n=19 | 17 rated 4–5 (89.5%); mean 4.42/5 | Strong perceived problem in this sample |
| Encounter frequency, n=20 | 4 frequently, 10 sometimes (70% combined) | Past experience supports relevance |
| Existing solution satisfaction, n=19 | 6 rated 1–2; 8 rated 3; 5 rated 4–5; mean 2.95/5 | Moderate satisfaction, not universal rejection |
| Biggest current problem, n=20 | 9 bypasses (45%); 4 false bans (20%); 3 privacy (15%) | Effectiveness and fair enforcement both matter |

Wallhacks (15/20) and aimbots (14/20) lead the multiple-selection list of problematic cheat types. Bots received 10 selections, macros/scripts and exploits 9 each, and hardware-assisted cheats 7. SUB-CHECK’s aim-analysis scope addresses part of this list. It does not justify a promise to detect wallhacks, bots or every hardware cheat.

## Customer jobs and pains

The player’s functional job is to participate in fair matches. Cheating interrupts that goal and makes results less trustworthy. The studio and moderator jobs remain hypotheses to validate with buyers: investigate reports efficiently, make defensible enforcement decisions and handle appeals without excessive work. The interview analysis on page 5 adds examples of actual behaviour to the survey summaries.

Survey feedback points to two linked pains: existing tools can be bypassed, while incorrect sanctions can harm legitimate players. This means a useful product must improve the quality of evidence and keep a review process. A high volume of alerts alone would not demonstrate value.

## Kernel access and platforms

Eight of 20 would probably not or would not install a kernel-level anti-cheat, six were unsure, and six would or probably would. The largest individual concerns were security vulnerabilities (9/20) and privacy (7/20). These answers indicate friction, without proving that all customers reject kernel tools.

Windows received 17 selections, Linux 5 and SteamOS/Steam Deck 4. Platform selections overlap, so Linux and SteamOS cannot be combined into a unique participant count. Compatibility remains a relevant secondary benefit, while the immediate pilot should focus on reliable analysis in one supported game.

Sources: survey screenshots Q05–Q12 and Q04. Multiple-selection percentages use the number answering that question, not the total number of selections.

# Concept feedback and adoption conditions

## Useful concept with unresolved accuracy concerns

Sixteen of 20 rated concept usefulness at 4 or 5 (80%), four rated it 3, and none rated it 1 or 2. The mean is 4.20/5. Positive responses to a described concept are an interest signal. They do not prove detection quality or adoption.

| Multiple-selection question, n=20 | Selections |
| --- | --- |
| Main advantages | No kernel software 12 (60%); better privacy 11 (55%); hardware-cheat detection 10 (50%); platform compatibility 7 (35%) |
| Main concerns | Detection accuracy 11 (55%); false positives 9 (45%); telemetry privacy 9 (45%); server costs 7 (35%) |
| Response to suspicious behaviour | Manual review 12 (60%); additional verification 12 (60%); temporary restriction 8 (40%); immediate ban 7 (35%) |

All 20 said yes or probably yes to trusting an anti-cheat more when a suspicious player receives review before a permanent ban. This question presents review positively, so the result supports testing a review workflow without showing that respondents will accept its delay or cost. Manual review and verification selections overlap and cannot be added.

## Technical integration and data control

In the technical-experience subgroup (n=9), seven rated the difficulty of implementing effective anti-cheat at 4 or 5. Six selected a self-hosted solution and three a managed cloud service. REST API, SDK and game-engine plugin each received four selections. These are overlapping preferences, not mutually exclusive product alternatives.

Five of nine would send anonymised telemetry with strict privacy controls, three said yes, and one was unsure. Self-hosting preference and conditional data sharing can coexist. The available aggregates do not reveal which people selected both. Unreal Engine received four preferences, Unity two, and the remaining three selected Godot, a custom engine or a free-text engine answer. This supports an Unreal-first interview plan, not an immediate commitment to a full plugin.

## Pricing and open feedback

Twelve of 20 selected a free/open-source core plus paid cloud service, eight a fixed monthly subscription, six per active player, six per analysed session and four tiered subscription. Fifteen said a free tier would increase their likelihood of testing, and five said maybe. These findings motivate a bounded pilot; price levels and paid conversion remain untested.

Q26 reports nine open answers but only eight are visible. Among the visible comments are “live game ban showcase” and “Cheaters, they make you lose all desire to play”. Other substantive comments request transparency, low overhead, privacy protection and independently audited security. We treat these as qualitative themes without a prevalence estimate. Q27 reports eight answers with seven visible, mostly brief non-additions.

Sources: Q13, Q15–Q18 and Q20–Q27. Q14 repeats Q13 and Q19 repeats Q03.

# Recorded interview findings

Three recordings add qualitative context to the survey. We use anonymised IDs, paraphrase the clear passages and retain timestamps for traceability. Interviewees describe different game types, so their comments should not be combined into a single target-market vote.

## I01 Multiplayer mobile game director

The respondent describes daily work on cheating and server protection (01:14–02:13). The main protection need concerns key game values such as money and ammunition rather than aim input (03:32–04:12). This is a useful negative fit signal: a studio can have a serious cheating problem without needing SUB-CHECK’s proposed aim-analysis product.

The respondent finds the general idea interesting but needs details to evaluate it (04:59–06:18). Integration requires development-lead review, control over code and data, and clear responsibility when a partner handles data (06:47–08:30). These are adoption conditions, not a pilot or purchasing commitment. The remarks about legal obligations are the respondent’s requirements, not a legal assessment in this report.

## I02 Independent game developer with an online leaderboard

The respondent describes a small game with a leaderboard and a server-side maximum-score filter (00:45–01:23). They describe inspecting logs after the system excluded users incorrectly (01:48–02:20). Their desired gain is reliable validation without errors that reject legitimate results. This supports attention to false positives, while leaderboard integrity is outside the initial aim-analysis scope.

The respondent values platform reach (02:33–02:53) and prefers a configurable SDK over automatic integration, citing control over a personal project (04:11–04:31). Interest in delegation is conditional on having a suitable server-based game (03:25–03:43). No budget or agreement to adopt is recorded.

## I03 Developer with multiplayer mod and server experience

The respondent describes modding and small-game development, including multiplayer/server work (01:07–02:51), and discusses adding Minecraft server mods for suspicious behaviour (03:08–03:30). Performance and compatibility are important concerns (05:12–07:30). These are reported experiences, not verified industry claims.

Telemetry must not block gameplay or punish network/service failures (12:00–13:17). Collecting additional data can still add overhead, and retrofitting an existing game differs from integrating during development (15:15–17:17; 21:40–23:56). The respondent favours configurable engine integration for a new game, a usable free core with paid extras (32:25–35:19), and an appeal route for false positives (35:41–38:19). No price or commitment is recorded.

## Cross-interview interpretation

The interviews support control, integration reliability and fair handling of uncertainty. They also narrow the segment: prioritise a shooter studio with an actual aim-cheat review problem. Mobile economy protection and leaderboard validation belong in a later discovery backlog. No interview demonstrates model accuracy, measured time savings, a price or a paid commitment.

Sources: I01 audio 09:06; I02 audio 04:46; I03 desktop recording 38:58. Timestamped notes and the evidence manifest map findings to the original recordings. We paraphrase clear passages because automatic transcription contains errors.

# Hypotheses and changes to the business idea

## What the evidence supports

| Hypothesis | Evidence and status |
| --- | --- |
| Cheating is a meaningful player problem | Supported within this sample: 17/19 seriousness ratings at 4–5 and 14/20 frequent or occasional encounters |
| Customers value a server-side approach | Early interest: 16/20 usefulness ratings at 4–5. Adoption is untested |
| Privacy and kernel access matter | Supported as concerns: 12/20 selected no kernel software as an advantage; 9/20 worry about telemetry privacy |
| Review increases trust | Stated preference supported: 20/20 yes or probably yes; operational cost and delay untested |
| Studios will buy a cloud-only product | Unvalidated, with a deployment challenge: 6/9 select self-hosting |
| Behaviour analysis detects hardware cheats accurately | Unvalidated. The survey measures expectations; no labelled technical benchmark exists |
| Customers will pay at the proposed rate | Unvalidated. No actual budgets, commitments or price-level experiment |

## Changes relative to Assignment 2

Assignment 2 already narrowed the customer to an indie or AA shooter studio, positioned the tool beside existing protection and required moderator review. We retain that baseline. The current study changes the delivery and validation priorities rather than presenting those earlier choices as new discoveries.

| Before | Updated proposal | Reason |
| --- | --- | --- |
| Hosted service first | Evaluate self-hosted deployment alongside managed cloud | 6/9 technical respondents select self-hosting |
| General integration support | Minimal API and event schema first; assess Unreal adapter in buyer interviews | API, SDK and plugin tie at 4/9; Unreal is 4/9 |
| Risk score and dashboard | Supporting events, review trail and appeal workflow in the pilot | Accuracy 11/20; false positives 9/20; review preference 20/20 |
| Telemetry ingestion | Minimise fields; pseudonymous session IDs; retention and deletion controls | Telemetry privacy 9/20; conditional sharing 5/9 |
| Pilot and usage tiers | Free bounded evaluation; test fixed and usage pricing with buyers | Free tier yes 15/20; preferences do not prove payment |

The recordings also change qualification and architecture. Mobile game values and leaderboard validation are adjacent problems, so we prioritise actual aim-cheat review needs. Before a pilot, confirm that the studio can export the required data: I03 distinguishes new-game integration from potentially expensive retrofitting. Use asynchronous analysis and never treat missing telemetry alone as proof of cheating.

We do not promise immunity to hardware cheats, an unbreakable cloud model, calibrated cheat probability or full operating-system compatibility for an entire game. A server-side score is a hypothesis to evaluate per game and should remain a prioritisation signal until the evidence supports a stronger interpretation.

# Updated business model

## Customer and value proposition

SUB-CHECK is a proposed B2B tool for small shooter studios with authoritative servers, a moderation workflow and feasible access to the required telemetry. It would help moderators prioritise suspicious aim events, inspect evidence and record decisions. The studio integrates and pays; players gain fairer review without an additional SUB-CHECK kernel installation. Faster review and fewer incorrect decisions are intended gains to measure.

| Business Model Canvas block | Updated working hypothesis |
| --- | --- |
| Customer segments | Indie and AA competitive shooter studios. Technical leads or owners as buyers, moderators as users. Budget authority still unverified |
| Value proposition | Explainable aim-analysis risk scores, human review, controlled telemetry and a choice of deployment |
| Channels | Developer communities, technical documentation and direct studio outreach. Channel effectiveness untested |
| Customer relationships | Assisted pilot integration, feedback sessions and technical support |
| Revenue streams | Bounded free pilot, followed by tested paid cloud usage or predictable monthly plans; optional self-hosted support. No confirmed prices |
| Key activities | Telemetry integration, model evaluation, moderator workflow development, privacy controls and integration support |
| Key resources | Game-specific labelled data, integration expertise, a model pipeline and secure processing infrastructure |
| Key partners | Pilot studios and moderators supplying permissioned data; engine/community contacts for integrations |
| Cost structure | Engineering, data labelling, inference and storage, security review and customer support. Unit costs remain unmeasured |

## Commercial implications

The sample can inform product priorities but cannot establish market size or revenue. Only two respondents selected game developer, and none selected esports organiser/admin. Software or cybersecurity experience does not imply a studio purchasing role. The next commercial decision therefore depends on interviews with people who own a game, an integration decision and a budget.

A free/open-source core is a pricing preference to test, not a licence commitment. Before choosing it, compare support burden, security update responsibility, evaluation-to-paid conversion and whether customers need local deployment because of privacy policy, latency or infrastructure control.

# Value proposition and validation roadmap

## Updated customer profile and value map

| Customer profile | Proposed product response |
| --- | --- |
| Job: identify suspicious matches and make defensible decisions | Risk-ranked cases with highlighted aim events and a review log |
| Pain: bypasses reduce confidence in existing protection | Add behavioural evidence to the existing detection stack; measure coverage by cheat type |
| Pain: false positives and disputes | Human review before permanent bans; preserve supporting events and an appeal trail |
| Pain: data exposure and integration uncertainty | Minimal documented schema, pseudonymous IDs and explicit storage/deletion policy |
| Gain: useful detection with manageable overhead | Benchmark detection, time to review, latency, bandwidth and cost per session |
| Gain: deployment and evaluation flexibility | Bounded free pilot plus self-hosted and managed options to compare |

## Next experiments and proposed decision rules

These experiments and thresholds are proposed by the team. They are not outcomes of the current study and should be agreed with pilot customers before collecting data.

| Experiment | Evidence to collect | Decision rule |
| --- | --- | --- |
| Buyer discovery | At least 8 studio leads or moderators; recent incidents, review effort, budget owner, data constraints | Continue if at least 3 studios offer a concrete pilot with available data and an owner |
| Silent technical pilot | Labelled clean and cheating sessions, separate train/test players, reviewers blind to model score | No automatic bans; compare precision and false alerts at the customer-agreed threshold |
| Review workflow test | The same cases with and without ranked evidence; paired review time and decision quality | Target at least 20% shorter median review time without worse decisions |
| Deployment comparison | Integration time, permitted data, bandwidth, latency and operating cost | Choose default deployment from actual pilot constraints, not survey counts alone |
| Commercial test | A specific paid offer after a successful free pilot and measured unit costs | Treat payment or signed commitment as stronger evidence than a pricing preference |

I03 adds a reliability test: simulate slow or unavailable analysis and packet loss. Gameplay must continue, and missing telemetry alone must not increase a player’s risk or cause a sanction. Measure the overhead on the authoritative server rather than assuming a remote service is free of performance cost.

Precision, recall and false alerts require trusted labels and game-specific evaluation. Include high-skill legitimate players, latency variation and different input devices. Restrict access to pilot data and log reviewer decisions. A risk score should not become a permanent-ban trigger during this validation phase.

Separately, close the assignment evidence gap by adding the required participants with verifiable records. Do not retrospectively reconstruct individual survey answers from the aggregate charts.

# Limitations conclusions and references

## Limitations

The available survey contains 20 participants, below the 30 required online respondents. Three recording files also fall below the five face-to-face video-interview alternative; audio files and a desktop recording should not be described as five face-to-face videos. This affects the interview execution criterion even though the available findings can still support analysis and an updated idea.

We have aggregate screenshots rather than the response export. Therefore we cannot verify participant uniqueness, compare roles with preferences, estimate overlap with interviewees or reconstruct individual response rows. Some questions have 19 responses, and the technical branch has nine. Roles, platforms and several preference questions allow multiple selections. Their percentages can exceed 100% when added.

The original questionnaire introduction and branching settings are not fully visible. The nine-person technical section matches the number answering yes to game/server experience, but this alone does not verify routing. Two screenshots repeat other charts. Two open-response screenshots show fewer answer cards than their displayed totals, so those sections are incomplete.

The small reachable sample contains many software and cybersecurity respondents and few confirmed game developers. Recruitment details and survey dates were not documented in the supplied summaries. Concept questions and feature descriptions may bias respondents toward the proposed solution. No market-size estimate, customer payment, retention effect or working detection benchmark follows from these materials.

Interview notes rely on local automatic transcription, which can misrecognise names and specialised terms. Findings use clear, relevant passages and include timestamps, while exact quotations from the audio are avoided. Uncertain details require source-audio review before being used as stronger evidence.

## Conclusion

The study supports continuing SUB-CHECK as a focused tool for studios and moderators, with detection quality and fair review as the immediate priorities. We retain server-side aim analysis alongside existing protection, add data control and deployment choice, and use a free bounded pilot to test integration and operational value. Buyer demand and technical performance remain the central questions for the next stage.

## Sources

1. Assignment 3 Business model Customer Development instructions. Local course document. Assessment requirements and supplied methodology examples.

2. SUB-CHECK Assignment 2 report. Local project baseline, pages 1–5. Customer, value proposition and original pilot model.

3. Survey/photo_1 … photo_27_2026-10-08_14-51-25.jpg. Google Forms aggregate summaries. Question IDs follow screenshot numbers. Aggregate transcription and evidence map accompany this report.

4. Interviews folder. Three supplied recordings, referenced by anonymised IDs I01–I03 and source timestamps in the interview notes.

5. ProductStar. How and why a product manager conducts CustDev. Habr, 3 June 2020. https://habr.com/ru/companies/productstar/articles/505208/ . Used for role segmentation, neutral questions about past behaviour and evidence-linked insights.

6. The second course-supplied methodology example on vc.ru was inaccessible during review. Its URL and access status appear in sources/README.md; no factual claim relies on it.
