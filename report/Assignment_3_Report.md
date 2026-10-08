# SUB CHECK Customer Development

Technology Entrepreneurship Assignment 3. Group CS-2406.

Nurzhan Bekmurat, Azamat Yermukhan, Yernur Khuan. 8 October 2026.

## Study summary

SUB-CHECK is a proposed service for small studios that run competitive shooter games. It would study aiming behaviour using data from game servers. It would give moderators a risk score and examples of suspicious events. Moderators would review these cases with their current anti-cheat tools.

The study shows early interest in this idea. Seventeen of 19 survey participants rated the cheating problem at 4 or 5 out of 5. Sixteen of 20 rated the usefulness of the idea at 4 or 5. However, participants also raised concerns about accuracy, wrong alerts and data privacy. We therefore propose a small pilot study. We have not yet proved that the product works or that studios will buy it.

We keep studios as customers and moderators as users. The updated plan adds control over game data and a choice of where to run the service. We also propose a limited free pilot. Six of nine people in the technical section selected self-hosting. This means running the service on their own servers. Twelve of 20 selected a free or open-source core with paid cloud services. These answers do not show how much a studio will pay.

## Available evidence

| Evidence | Available material |
| --- | --- |
| Survey | 20 participants. We received 27 Google Forms screenshots, including two repeated charts. |
| Interviews | Three recordings. We analyse them separately from the survey. |
| Answers per question | Most questions: 20. Seriousness and satisfaction: 19. Technical questions: 9. |
| Course minimum | 30 online participants OR 5 face-to-face video interviews. Our material is below both minimums. |

We do not add the interview participants to the survey total. We do not know if the same people took part in both. These results describe our sample. They do not describe the whole gaming market.

## Main terms

B2B means selling to another business. Telemetry means game data sent for analysis. A false positive is a wrong alert about a fair player. A risk score helps a moderator choose which case to review first. It is not proof of cheating.

# Audience and research preparation

## Customer groups

We separate the person who buys the service, the person who uses it, and the player. The table gives our planning scores from 1 to 5. A higher score means easier access, a larger expected group, or more expected benefit. These scores are team estimates. We have not measured market size.

| Group | Access | Size | Benefit | Priority |
| --- | --- | --- | --- | --- |
| Small and medium shooter studio leads | 3 | 3 | 5 | First for buying decisions |
| Server moderators and tournament admins | 4 | 3 | 5 | Second for review needs |
| Active competitive players | 5 | 5 | 4 | First for easy problem research |

The survey sample differs from our target customers. Participants could select several roles. Ten of 20 selected cybersecurity specialist or student. Seven selected software developer, seven casual gamer, three competitive gamer, and two game developer. No one selected esports organiser or admin. Nine reported multiplayer game or server experience. We call them the technical group. We cannot treat all nine as studio buyers.

## Research aims

We studied cheating problems, current tools and reactions to SUB-CHECK. We also asked about data sharing, integration and pricing. The questionnaire covers background, cheating experience, current anti-cheat, kernel access, the new idea, risk scores, technical needs and final comments.

Questions about past cheating give examples of experience. Questions about the proposed idea give opinions. Positive opinions can help us choose the next test. They do not prove a buying decision or product quality. Showing the idea before asking about it may lead to more positive answers.

## Plan for the next interviews

Ask about the same main topics before showing SUB-CHECK. Start with the person’s role and their recent game. Ask about the last suspected cheating case. Ask what they did, how long review took, and what was difficult. Ask studio leads about a recent integration, data rules and who controls the budget. Then show the idea and ask what evidence they need for a pilot.

We propose contacting studios through developer contacts and small multiplayer communities. We propose finding moderators through server communities and players through peers. These are future channels. The supplied material does not record the actual survey recruitment channels. Ask permission to record, note the role and source, and allow 15–30 minutes. Use neutral questions and avoid a sales pitch.

# Cheating problems and current tools

## Survey findings

| Question and answers | Result | Meaning |
| --- | --- | --- |
| Cheating seriousness, n=19 | 17 rated 4–5 (89.5%). Average: 4.42/5. | Most people in this sample see a serious problem. |
| Cheating frequency, n=20 | 4 often and 10 sometimes (70% together). | Many participants have met cheating. |
| Satisfaction with current tools, n=19 | 6 rated 1–2, 8 rated 3, and 5 rated 4–5. Average: 2.95/5. | Opinions are mixed. Some people are satisfied. |
| Biggest problem, n=20 | 9: cheats bypass tools (45%). 4: wrong bans (20%). 3: privacy (15%). | Detection and fair decisions both matter. |

Participants could select several cheat types. Wallhacks received 15 selections and aimbots received 14. Bots received 10. Macros or scripts and exploits each received 9. Hardware-assisted cheats received 7. SUB-CHECK focuses on aiming. We have no evidence that it can detect all these cheat types.

## Customer tasks and problems

Players want fair matches and results they can trust. We expect studios and moderators to need faster review and clear evidence for decisions. We still need to test these needs with actual buyers. The interviews on page 5 give examples of behaviour as well as opinions.

Survey answers show a problem with cheats that avoid current protection. They also show concern about wrong bans. A useful product should help people make better decisions. A large number of alerts alone does not show success.

## Kernel access and platform support

Kernel software has deep access to the operating system. Eight of 20 said they probably would not, or would not, install kernel-level anti-cheat. Six were unsure. Six said yes or probably yes. The main concerns were security weaknesses (9/20) and privacy (7/20). The sample does not show that everyone rejects kernel tools.

Windows received 17 selections, Linux 5, and SteamOS or Steam Deck 4. People could select several platforms. We cannot add Linux and SteamOS to count unique people. Platform support may be useful, but the first pilot should focus on one supported game.

Sources: survey Q04–Q12. The percentage for each option uses the number of people answering that question. It does not use the total number of selections.

# Feedback on the proposed service

## Interest and concerns

Sixteen of 20 rated the idea’s usefulness at 4 or 5 (80%). Four rated it 3. No one rated it 1 or 2. The average was 4.20/5. This shows interest in the description. We have not tested real use or detection quality.

| Question, n=20 | Selections |
| --- | --- |
| Main benefits | No kernel software: 12 (60%). Better privacy: 11 (55%). Hardware-cheat detection: 10 (50%). Platform support: 7 (35%). |
| Main concerns | Accuracy: 11 (55%). Wrong alerts: 9 (45%). Game data privacy: 9 (45%). Server costs: 7 (35%). |
| Action after a suspicious event | Manual review: 12 (60%). Extra checks: 12 (60%). Temporary limits: 8 (40%). Immediate ban: 7 (35%). |

All 20 said yes or probably yes when asked if review before a permanent ban would increase trust. The question presents review in a positive way. We still need to test whether people accept its time and cost. People could select both manual review and extra checks. We cannot add these counts.

## Integration and data sharing

In the technical group of nine, seven rated anti-cheat development difficulty at 4 or 5. Six selected self-hosting and three selected managed cloud. An API, SDK and engine plugin each received four selections. An API connects systems. An SDK provides code tools. A plugin adds a feature to a game engine. These options could overlap.

Five of nine would share game data only with strict privacy controls. Three said yes and one was unsure. We cannot see which people also chose self-hosting. Four selected Unreal Engine, two Unity, and three gave other engine answers. We propose asking Unreal developers first. This does not justify building a full plugin yet.

## Pricing and open comments

Twelve of 20 selected a free or open-source core with paid cloud services. Eight selected a fixed monthly price. Six selected a price per active player and six a price per analysed session. Four selected price tiers. Fifteen said a free tier would help them test the service. Five said maybe. We still need to test actual prices and payment.

Q26 reports nine written answers, but only eight are visible. Comments ask for a live game example, clear information, low performance cost, privacy and an independent security review. One comment says cheating removes the wish to play. We describe these themes without estimating how common they are. Q27 reports eight answers, but only seven are visible. Most add little new information.

Sources: Q13, Q15–Q18, Q20–Q27. Q14 repeats Q13. Q19 repeats Q03. Hardware-cheat detection is a participant expectation, not a tested result.

# Recorded interview findings

We analysed three recordings. We use IDs I01–I03 and describe clear statements in our own words. The times help readers find the source. The interviewees work with different games. Their answers do not form one target-market vote.

## I01 Mobile multiplayer game director

The director describes daily work on cheating and server protection (01:14–02:13). The main need is to protect game values such as money and ammunition (03:32–04:12). Aiming is not the main problem. This shows that a studio may face serious cheating but still have little need for our first product.

The director finds the idea interesting but needs more details (04:59–06:18). The development lead must check the integration. The studio needs control over code and data, and clear partner responsibilities (06:47–08:30). These are conditions for considering the service. They are not a promise to test or buy. Comments about legal duties are the interviewee’s requirements.

## I02 Independent developer with an online leaderboard

The developer describes a small game with an online leaderboard and a maximum-score filter (00:45–01:23). They checked logs after the filter wrongly excluded users (01:48–02:20). They need reliable checks that accept fair results. This supports our focus on wrong alerts. However, leaderboard protection is outside our first aiming product.

The developer values platform support (02:33–02:53). They prefer an SDK they can adjust rather than automatic integration (04:11–04:31). They may use outside security help if they build a suitable server-based game (03:25–03:43). The recording contains no budget or agreement to adopt the service.

## I03 Developer with multiplayer mod and server experience

The developer describes modding and multiplayer server work (01:07–02:51). They also discuss Minecraft server mods for suspicious behaviour (03:08–03:30). Performance and platform support matter to them (05:12–07:30). These are reported experiences. We have not checked broader claims about other products.

Game data analysis must not stop gameplay or punish connection failures (12:00–13:17). Collecting data can still add extra load. Adding a tool to an old game may be harder than adding it during development (15:15–17:17, 21:40–23:56). The developer prefers adjustable integration, a useful free core with paid extras (32:25–35:19), and a way to appeal wrong bans (35:41–38:19). No price or purchase promise is recorded.

## Meaning for SUB CHECK

The interviews support data control, reliable integration and careful decisions. They also help us narrow the customer group. We should first find shooter studios with an actual aim-cheat review problem. Mobile economy and leaderboard protection need separate research. None of the interviews proves model accuracy, time savings or payment.

Sources: I01 audio 09:06, I02 audio 04:46, I03 desktop recording 38:58. The notes include source times. Automatic transcription contains errors, so we avoid exact audio quotations.

# Hypotheses and changes to the idea

## Evidence status

| Hypothesis | Current evidence |
| --- | --- |
| Cheating is a player problem | Supported in this sample. 17/19 rated seriousness at 4–5. 14/20 met cheating often or sometimes. |
| People value server-side analysis | Early interest. 16/20 rated usefulness at 4–5. Actual use is untested. |
| Privacy and kernel access matter | 12/20 selected no kernel software as a benefit. 9/20 raised game data privacy concerns. |
| Review can increase trust | 20/20 said yes or probably yes. Review time and cost are untested. |
| Studios will buy a cloud-only service | Untested. 6/9 in the technical group selected self-hosting. |
| Aim analysis can detect hardware cheats well | Untested. We have no technical test with reliable labels. |
| Customers will pay our price | Untested. We have no actual price test, budget or payment promise. |

## Changes since Assignment 2

Assignment 2 already focused on small shooter studios and moderator review. It also placed SUB-CHECK beside current anti-cheat tools. We keep these choices. The new study changes how we plan to deliver and test the service.

| Earlier plan | Updated plan | Reason |
| --- | --- | --- |
| Hosted service first | Compare own-server and cloud options. | 6/9 selected self-hosting. |
| General integration support | Start with a small API and clear data fields. Ask Unreal developers about an adapter. | API, SDK and plugin: 4/9 each. Unreal: 4/9. |
| Risk score and dashboard | Show event evidence, save review decisions, and allow appeals. | Accuracy: 11/20. Wrong alerts: 9/20. Review: 20/20. |
| Collect game data | Collect only needed fields. Use IDs without real names. Set storage and deletion rules. | Data privacy: 9/20. Conditional sharing: 5/9. |
| Pilot and usage tiers | Offer a limited free pilot. Test monthly and usage prices with buyers. | 15/20 said a free tier would help testing. |

The interviews add two conditions. First, the studio must have an aim-cheat problem and access to the needed data. Second, analysis should run separately from gameplay. Missing data alone must not cause a cheating alert or punishment.

The score should help order review cases. It does not give a proven probability of cheating. We do not claim full hardware-cheat detection or full platform support for the whole game. Each game needs its own test.

# Updated business model

## Customer and proposed value

We plan a B2B service for small shooter studios. Their servers must control match results and provide the needed game data. Moderators would review suspicious aim events and save decisions. Studios would connect the service and pay for it. Players could receive fairer review without an extra SUB-CHECK kernel installation. We still need to measure faster review and fewer wrong decisions.

| Business Model Canvas block | Working hypothesis |
| --- | --- |
| Customer segments | Small independent and medium-sized competitive shooter studios. Studio leads buy, and moderators use the tool. We must confirm budget authority. |
| Value proposition | Aim risk scores with event evidence, human review, data control and a choice of where to run the service. |
| Channels | Developer communities, technical guides and direct studio contact. We have not tested which channel works best. |
| Customer relationships | Help with pilot integration, feedback meetings and technical support. |
| Revenue streams | A limited free pilot, then paid cloud use or a monthly plan. Possible paid support for self-hosting. No confirmed prices. |
| Key activities | Connect game data, test the model, build review tools, protect data and support integration. |
| Key resources | Game data with reliable labels, integration skills, analysis software and secure servers. |
| Key partners | Pilot studios and moderators that can share data with permission. Engine and developer community contacts. |
| Cost structure | Development, data labelling, analysis, storage, security review and support. We have not measured cost per session. |

## Business decisions still to test

This sample helps us choose product priorities. It does not show market size or expected income. Only two people selected game developer, and none selected esports admin. Software or security knowledge does not mean a person can buy for a studio. We need interviews with people who control a game project and its budget.

A free or open-source core is an option to test. We have not chosen a software licence. Before deciding, we should compare support work, security updates and the move from a free pilot to payment. We should also ask why each customer needs local or cloud deployment.

# Value proposition and next tests

## Customer profile and value map

| Customer need | Proposed product response |
| --- | --- |
| Task: find suspicious matches and make fair decisions | Order cases by risk. Show aim events and save review decisions. |
| Problem: cheats avoid current protection | Add behaviour evidence beside current tools. Test each cheat type. |
| Problem: wrong alerts and disputes | Review before permanent bans. Keep evidence for appeals. |
| Problem: data privacy and difficult integration | Use a small set of clear data fields, IDs without names, and storage rules. |
| Gain: useful checks with low extra load | Measure detection, review time, delay, bandwidth and cost per session. |
| Gain: easy evaluation and server choice | Compare a limited free pilot on local servers and managed cloud. |

## Proposed experiments

The following numbers are future targets. We have not achieved them. Agree on the test rules with pilot customers before collecting their data.

| Test | Evidence to collect | Proposed rule |
| --- | --- | --- |
| Buyer interviews | At least 8 studio leads or moderators. Ask about recent cases, review time, budget owners and data rules. | Continue if 3 studios offer a concrete pilot with available data and a responsible person. |
| Silent technical pilot | Use labelled fair and cheating sessions. Keep test players separate from training players. Hide scores during independent review. | No automatic bans. Compare correct alerts and wrong alerts at a level agreed with the customer. |
| Review test | Compare the same cases with and without ranked evidence. Record time and decision quality. | Target at least 20% less median review time with no worse decisions. |
| Server options | Measure setup time, permitted data, bandwidth, delay and operating cost. | Choose the default using actual pilot results. |
| Price test | Make a specific paid offer after a useful free pilot. Measure service costs. | Treat payment or a signed promise as stronger evidence than a preference. |

Also test slow analysis, lost data and service failures. The game must continue. Missing data alone must not raise the risk score or cause punishment. Measure the extra load on game servers even if analysis runs elsewhere.

Include skilled fair players, different connection speeds and input devices. Correct labels are essential. Limit access to pilot data and save review decisions. Keep permanent-ban decisions with people during the pilot.

We also need more participant records to meet the course minimum. We must collect new answers rather than create individual answers from summary charts.

# Limitations conclusion and sources

## Study limitations

Our material includes 20 survey participants and three recordings. It is below the course minimum of 30 online participants or five face-to-face video interviews. Two audio files and one desktop recording do not meet the five-video option. We can analyse the available evidence, but this course requirement remains unmet.

We received summary screenshots rather than individual survey answers. We cannot check unique participants, connect roles to preferences, or compare survey and interview participants. Most questions have 20 answers. Two have 19, and the technical section has nine. Several questions allow more than one choice, so their percentages may add to more than 100%.

The full introduction and question-routing settings are not visible. Nine people report game or server experience, and nine answer technical questions. This match does not prove how the form sent people to those questions. Two screenshots repeat charts. Two written-answer sections show fewer answer cards than their totals.

Many participants have software or cybersecurity backgrounds. Few are confirmed game developers. The summaries do not record survey dates or recruitment details. The idea description may make answers more positive. The material does not prove market size, customer payment, player retention or detection quality.

Interview notes use local automatic transcription. It may contain wrong names or technical words. We use clear passages, our own wording and source times. Unclear details need another check of the recording before stronger claims.

## Conclusion

The study supports a focused pilot for SUB-CHECK. We keep server-side aim analysis beside current protection. We add data control, server choice and a fair review process. The next steps should test integration, detection quality and useful review. We still need evidence from studio buyers and actual paid offers.

## Sources

1. Assignment 3 Business model Customer Development. Local course instructions and research examples.

2. SUB-CHECK Assignment 2 report, pages 1–5. Earlier customer definition and pilot plan.

3. Survey screenshots photo_1 to photo_27, dated in the file names 8 October 2026. Google Forms summaries. Question IDs follow screenshot numbers. The project includes option counts and an evidence map.

4. Three supplied recordings in the Interviews folder. Notes use anonymous IDs I01–I03 and source times.

5. ProductStar, How and why a product manager conducts CustDev. Habr, 3 June 2020. https://habr.com/ru/companies/productstar/articles/505208/ . Used for customer groups, neutral questions and past behaviour.

6. The second course example on vc.ru could not be accessed during review. Its link and access status are in sources/README.md. No factual claim depends on it.
