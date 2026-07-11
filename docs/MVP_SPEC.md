# AI SAHELI — Interview MVP Specification

**Version:** v1.0
**Status:** Draft (Post PRD v1.0)

---

# Purpose

This document defines the **first implementation milestone** for AI SAHELI.

It does **not** redefine the product vision described in **PRD v1.0**. Instead, it identifies the smallest production-quality subset of functionality required to demonstrate AI SAHELI's core value during technical interviews and early validation.

All functionality described here is a subset of **PRD v1.0**. Future releases will progressively implement the remaining product capabilities.

---

# Objective

Deliver a **privacy-first, voice-first Android companion** that enables target users to complete essential smartphone tasks and perform a reliable emergency flow using simple Hindi voice commands.

The MVP should clearly demonstrate AI SAHELI's philosophy of being **a trusted AI Companion rather than a traditional AI Assistant**.

---

# Target Users

* Elderly individuals living independently
* First-time smartphone users
* People with accessibility needs

---

# MVP Principles

* Production-quality implementation.
* Demonstrate the AI Companion philosophy.
* Privacy-first by default.
* Voice-first interaction.
* Build upon the final AI SAHELI architecture rather than creating a disposable prototype.

---

# MVP Scope (Must Have)

## Voice Interaction

* Local wake-word detection (device-first where feasible).
* Hindi voice interaction.

## Core Voice Intents

* Open WhatsApp
* Open Phone
* Call a preset family contact
* Open Camera
* Scroll Up / Down
* Home
* Back

## Emergency Support

* Emergency keyword detection (e.g. *"Bachao"* / *"Madad"*).
* 10-second cancellable countdown.
* Hindi voice confirmation throughout the countdown.
* Escalation to a Trusted Contact through SMS and/or phone call if not cancelled.

## Accessibility

* Android Accessibility Service integration for reliable UI interaction.

## Voice Feedback

* Hindi Text-to-Speech confirmations.
* Clear spoken status updates during emergency handling.

## Demonstration

* Guided interview demo flow.
* Optional smartwatch simulator for demonstrating wearable integration concepts.

---

# Out of Scope

The following capabilities remain part of the full AI SAHELI vision but are intentionally excluded from this MVP:

* Medical diagnosis
* Clinical health features
* Production-grade fall detection
* Caregiver dashboard
* Long-term companion memory
* Multi-device synchronisation
* Full offline LLM
* Advanced situational reasoning
* Smart home integration
* Wearable production support

---

# Acceptance Criteria

* ≥80% successful completion rate for core voice tasks during moderated usability testing.
* Wake-word false activation rate below 3% during a one-hour ambient test.
* Emergency flow successfully completes countdown and escalation in at least 95% of simulated scenarios.
* Hindi TTS feedback begins within approximately 2 seconds of successful intent detection.
* Core onboarding and permission setup completed by a non-technical user in under five minutes.

---

# Success Demonstration

At the end of the MVP, a first-time user should be able to:

* Wake AI SAHELI using voice.
* Open WhatsApp hands-free.
* Call a family member using voice.
* Navigate the phone using voice commands.
* Trigger an emergency.
* Cancel an emergency.
* Complete an emergency escalation.
* Receive clear Hindi voice confirmations throughout the interaction.

---

# Key Metrics (KPIs)

* Task Success Rate
* Wake-word Precision
* Wake-word Recall
* Emergency Reliability
* Time-to-Action (Voice Command → Action)
* User Satisfaction (SUS or lightweight NPS)

---

# Validation Plan

* Recruit 8–12 representative users (elderly and low-technology users).
* Conduct 10 moderated usability sessions.
* Record task completion, failures, and usability friction.
* Perform a one-week ambient wake-word evaluation across three test devices.
* Produce a usability report and complete two rapid improvement iterations before the interview demonstration.

---

# Timeline & Assumptions

**Estimated Duration:** 21 Days

This estimate assumes that **HLD and MVP-focused LLD have already been completed**.

### Week 1

* Wake-word integration
* Accessibility Service
* Three core voice intents
* Basic onboarding

### Week 2

* Remaining voice intents
* Emergency flow
* Hindi TTS
* Permission management

### Week 3

* Demo polishing
* Usability testing
* Bug fixing
* Performance tuning
* Interview preparation

Assumptions:

* 2 Engineers (Android + Voice/AI)
* 1 UX Designer / Researcher
* 3 Android test devices

---

# Non-Functional Requirements

### Privacy

* Local-first audio processing wherever feasible.
* Explicit user consent for any cloud-based functionality.

### Performance

* Voice interactions should feel responsive.
* Background processing should minimise battery impact.

### Battery

* Background listening should not increase idle battery consumption by more than 10% on supported test devices.

### Localization

* Hindi-first user experience.
* Simple, accessible language.

### Security

* Trusted Contacts and user preferences stored securely using Android encryption mechanisms.

---

# Top Risks & Mitigations

| Risk                       | Mitigation                                                               |
| -------------------------- | ------------------------------------------------------------------------ |
| False emergency activation | Cancellable countdown with spoken confirmation before escalation         |
| Wake-word accuracy         | Conservative detection thresholds prioritising precision                 |
| Accessibility limitations  | Large on-screen manual fallback for critical actions                     |
| Privacy concerns           | Document data flows and require explicit user consent for cloud services |

---

# Deliverables

* Android APK
* GitHub source repository
* Demo checklist
* Interview demonstration script
* Installation guide
* Project README
* Usability test summary
* One-page KPI dashboard

---

# Relationship to Project Documentation

| Document                    | Purpose                                                    |
| --------------------------- | ---------------------------------------------------------- |
| Manifesto                   | Defines why AI SAHELI exists                               |
| ROADMAP                     | Defines the long-term product evolution                    |
| PRD                         | Defines the complete product behaviour and user experience |
| Interview MVP Specification | Defines the first implementation milestone                 |
| HLD                         | Defines the complete system architecture                   |
| LLD                         | Defines the MVP implementation design                      |

---

**Engineering Principle**

> **Design the architecture for the complete AI SAHELI vision. Build the Interview MVP as the first production-quality implementation. Every MVP component must remain compatible with the long-term architecture rather than becoming a disposable prototype.**
