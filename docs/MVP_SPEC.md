# AI SAHELI — One-Page MVP Spec

**Objective**
Deliver a privacy-first, voice-first Android companion that enables target users to complete essential smartphone tasks and a basic emergency flow using simple Hindi voice commands for a demonstrable MVP.

**Target Users**
- Elderly individuals living independently
- First-time smartphone users
- People with accessibility needs

**MVP Scope (Must-have)**
- Wake-word: local wake-word detection (device-first where feasible).
- Core Hindi intents: open WhatsApp, open Phone, call a preset family contact, open Camera, scroll up/down, back/home navigation.
- Emergency flow: emergency keyword detection (e.g., "Bachao" / "Madad"), 10s cancellable countdown with Hindi TTS prompts, escalation to Trusted Contact via SMS/call if not cancelled.
- Android Accessibility Service integration to perform UI actions reliably.
- Hindi TTS feedback for confirmations and countdown prompts.
- Demo harness: simple smartwatch simulator or guided demo flow for evaluators.

**Out of Scope (MVP)**
- Medical diagnosis or clinical features, production fall-detection, caregiver dashboard, long-term memory, multi-device sync, full offline LLM.

**Acceptance Criteria**
- 80%+ successful completion rate for core tasks in lab usability tests with representative users.
- Wake-word false-activation rate < 3% in 1-hour ambient tests.
- Emergency flow completes countdown and escalation correctly in 95% of simulated tests.
- TTS responses occur within ~2s of intent detection on target devices.
- Core permissions and onboarding flows completable in under 5 minutes by a non-technical user.

**Key Metrics / KPIs**
- Task Success Rate (end-to-end)
- Wake-word Precision / Recall (false-positive & false-negative rates)
- Emergency Reliability (% successful escalations)
- Time-to-action (median voice-command → action latency)
- User Satisfaction (SUS or quick NPS from elderly participants)

**Validation Plan**
- Recruit 8–12 representative users (elderly / low-tech) for moderated usability tests.
- Run 10 lab sessions measuring KPIs; record failure modes and friction points.
- Run 1-week ambient test on 3 devices to capture wake-word false-activations.
- Produce a short usability report and iterate two rapid cycles before demo.

**Timeline & Team Assumptions (21 days)**
- Week 1: Wake-word + Accessibility integration + 3 core intents + basic onboarding.
- Week 2: Additional intents, emergency flow, Hindi TTS, permission UI.
- Week 3: Demo polish, usability testing, bug fixes, and test report.
- Assumes: 2 engineers (Android + Voice), 1 designer/researcher, access to 3 test devices.

**Non‑Functional Requirements**
- Privacy: local-first audio processing where possible; explicit opt-in for any cloud features.
- Battery: background listening should not increase idle drain >10% on test devices.
- Localization: Hindi-first UX with plain-language prompts.
- Security: Trusted Contacts and preferences stored encrypted on-device.

**Top Risks & Mitigations**
- False emergencies: require cancellable countdown + clear voice confirmation before escalation.
- Wake-word accuracy limits: calibrate conservative thresholds prioritising precision for MVP.
- Accessibility edge cases: provide large on-screen manual fallback for critical actions.
- Regulatory/privacy exposure: document data flows and require explicit opt-in for cloud features.

**Deliverables (MVP demo)**
- APK with Accessibility-enabled flows and emergency demo.
- Demo checklist & test script for evaluators.
- Usability test report (summary + prioritized fixes).
- One-slide metrics dashboard showing KPIs.

---

Please review and tell me if you want this added to the PRD or adjusted for a different timeline or scope.