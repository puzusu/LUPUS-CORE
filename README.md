# 🐺 LUPUS-CORE
### Adaptive Artificial Life for Family Time

**An experimental, offline artificial-life framework designed to give the pups of Family Time the ability to learn, remember, adapt, and share knowledge through their own interactions.**

> **Development status:** Active research and development  
> **Current milestone:** Experiment 001A accepted; Experiment 001B integration prototyping  
> **Game:** Family Time — Episode 3, Build b108  
> **Platform:** Windows / Unity / BepInEx  
> **Architecture:** C# / .NET / Offline simulation

---

## 🌱 The Vision

Most game characters follow predefined instructions. They react to conditions, execute scripted behaviors, and repeat those behaviors when the same conditions occur.

**LUPUS-CORE explores a different approach.**

Our goal is to create pups that can develop knowledge from experience, make decisions influenced by that knowledge, and communicate useful discoveries to other pups.

Rather than assigning every pup a permanently fixed personality, we want individual behavior to develop from experience, memory, and social interaction.

The long-term ambition is a living, decentralized artificial-life system in which each pup has its own evolving history.

## 🧠 How It Works

LUPUS-CORE is designed around five interconnected capabilities.

### 1. Learning Through Experience

A pup encounters something meaningful in its environment.

The system records what happened, who experienced it, and the available evidence.

Knowledge should be grounded in actual events rather than appearing automatically in every pup's memory.

### 2. Individual Memory

Each pup maintains its own knowledge and experience.

Memory must preserve identity, distinguish direct experience from information received from others, and account for uncertainty.

### 3. Social Knowledge Transmission

A pup can communicate a discovery to another pup through an in-game interaction, such as vocalization.

The receiving pup evaluates the information rather than automatically treating every message as a confirmed fact.

### 4. Independent Verification

Information received from another pup can influence decisions, but firsthand verification provides stronger evidence.

A pup may investigate a reported discovery and update its knowledge based on the result.

### 5. Emergent Behavioral Development

Over time, differences in experiences may lead to differences in choices, preferences, social relationships, and behavioral tendencies.

This is a future development objective, not a claim that fully emergent personality is already implemented.

---

## 🐾 Example: One Discovery, Three Pups

Imagine a small group exploring their environment.

1. **Pup A** independently discovers a food source.
2. Pup A remembers where it was found.
3. Pup A communicates that discovery to **Pup B**.
4. Pup B receives information with its original source and confidence preserved.
5. Pup B decides to investigate the reported location.
6. After independently confirming the discovery, Pup B gains firsthand evidence.
7. Pup B can subsequently communicate that verified knowledge to **Pup C**.

This illustrates the core experimental goal: knowledge moving through a group because of individual experience and observable interactions.

The complete sequence has been demonstrated in a controlled headless experiment. Equivalent live gameplay behavior remains under development.

---

## ⚙️ Technical Architecture

LUPUS-CORE is intended to operate as a standalone, offline Family Time mod.

It uses conventional local algorithms and deterministic software components rather than requiring an external language model or cloud service.

| Component | Responsibility |
|---|---|
| Identity system | Track individual pups and prevent ambiguous identity reuse |
| Evidence ledger | Record discoveries, provenance, confidence, and verification |
| Learning engine | Update knowledge from observations and communicated evidence |
| Social communication | Coordinate and validate knowledge-transfer interactions |
| Decision integration | Allow learned information to influence behavior |
| Persistence | Preserve validated knowledge between sessions |
| Game adapter | Connect the learning core to Family Time's native systems |

The architecture separates the learning engine from the game adapter. This allows the core algorithms to be tested independently before live integration.

### Integration with GAT

Family Time uses a custom entity and behavior framework referred to as **GAT**.

Our reverse engineering has identified managed-code interfaces, GPU compute workloads, entity handles, movement services, speech systems, and native command ownership.

LUPUS-CORE aims to cooperate with those systems rather than replace the game's movement, animation, or audio engine.

Native integration details are still being investigated and validated.

---

## 🔬 Development Progress

### Experiment 001A — Accepted

The first experiment established a deterministic, headless proof of social learning and knowledge transmission.

Verified acceptance results included:

- **320/320 formal acceptance cases passed**
- **78/78 regression checks passed**
- Four matched experimental control groups
- Deterministic replay and evidence tracing
- Identity, provenance, and duplicate-delivery safeguards
- Versioned persistence validation
- A 10,000-logical-step benchmark

These results establish the behavior of the isolated experimental core—not live compatibility with Family Time.

### Experiment 001B — In Development

The next phase focuses on connecting the accepted learning machinery to game-facing interfaces.

Development targets include:

- A deterministic GAT adapter prototype
- Pup identity and native-handle validation
- Observation provenance
- Vocal-action lifecycle tracking
- Player-command and ownership coordination
- Fail-closed behavior under uncertainty
- Automated integration tests

Live game integration will be evaluated separately from headless prototype results.

### Longer-Term Goals

Future experiments may explore learned exploration habits, social preferences, cooperative activities, adaptive play, and more sophisticated decentralized knowledge sharing.

These are research objectives, not announced completed features.

---

## 🛠️ Development and Research

The project draws on analysis of Family Time's native systems and practical integration knowledge from existing community and privately developed mods, including:

- **Uppies:** Voice, emotion, and interaction integration
- **Pup Traits:** Behavioral scheduling, traits, and social activities
- **Pups Wander:** Scripted pup autonomy
- **Family Time Dedicated Server Tool:** Native entity mapping, snapshots, and rendering integration

Reference implementations and experimental findings are evaluated independently. Their behavior is not treated as proof that LUPUS-CORE's learning requirements have been satisfied.

## 📦 Installation and Availability

**LUPUS-CORE is not yet presented as a finished, publicly installable gameplay mod.**

The current work focuses on a validated experimental core and its integration with Family Time.

Installation instructions, supported configurations, and release builds will be documented once a playable build has been tested.

## 📚 Wiki Navigation

As development progresses, this wiki will include:

- Getting Started
- Architecture
- Artificial Life and Learning
- Social Knowledge Transmission
- Game Integration
- Experiments and Test Results
- Development Roadmap
- Troubleshooting
- Changelog

---

## ❤️ Project Philosophy

LUPUS-CORE began with a simple question:

**What if the pups could learn from one another instead of only following predefined behaviors?**

The project is an attempt to explore that question through real software, observable evidence, and incremental experimentation.

We are not trying to simulate intelligence merely through random animations or scripted interactions.

We want individual experiences to matter, knowledge to have a traceable origin, and decisions to change because something was genuinely learned.

**One pup discovers. Another learns. A third inherits the knowledge.**

*And eventually, each develops a story of its own.*

---

**LUPUS-CORE**  
*Learning. Memory. Autonomy. Social Life.*
