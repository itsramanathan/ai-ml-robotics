 Voice Agent — Known Failure Modes

**Author:** Ramanathan
**Date created:** 2026-04-28 (Day 2 of 18-week sprint)
**Status:** Triage from memory — pre-systematic-testing
**Purpose:** Document everything broken or suspect in the current build, to drive systematic testing Wed-Fri and produce a code-assessment verdict by Sun May 3.

## Context

Customer status: verbal commitment, 2-week trial, then paid. Last meaningful contact ~6 weeks ago. Build is vibe-coded with multiple AI debug sessions; some fixes appear to have introduced new failures. This document is the basis for deciding: patch-and-ship, partial rebuild, or full rebuild.

---

## Failure modes

## FM-01: STT - Mishears/audio drop, background noise

**Trigger:**
**Symptom:**
**Suspected cause: Does not use live kit's noise suppression / isolation
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Annoying
**Confidence in cause (high / medium / low / unknown): High

## FM-02:LLM responseHallucinates? Wrong format? Forgets context? Refuses unexpectedly?

**Trigger:**
**Symptom:**
**Suspected cause: Check sales.yaml and instructions
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Medium

## FM-03:TTS (text-to-speech)Mispronunciations? Wrong voice? Audio artifacts? Weird pauses?
**Trigger:**
**Symptom:**
**Suspected cause: Voice changes from time to time. It also mispronounces and hallucinates
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Annoying
**Confidence in cause (high / medium / low / unknown): Medium

## FM-04:Latency
**Trigger:**
**Symptom:**
**Suspected cause: multiple llm calls
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Annoying
**Confidence in cause (high / medium / low / unknown): High

## FM-05:Conversation flow
**Trigger:**
**Symptom:**
**Suspected cause: Talks over
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Annoying
**Confidence in cause (high / medium / low / unknown): Low

## FM-06:State management
**Trigger:**
**Symptom:**
**Suspected cause: Session management has to be implemented
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Medium

## FM-07:Integration
**Trigger:**
**Symptom:**
**Suspected cause: Livekit has to be integrated properly
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Low

## FM-08: UI changes automatically in different scenarios (text only/voice)
**Trigger:**
**Symptom:**
**Suspected cause: Multiple failing cases
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Unknown

## FM-09:Prompt/persona
**Trigger:**
**Symptom:**
**Suspected cause: Out of character
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Low

## FM-10:Basic conversation flow failing
**Trigger:**
**Symptom:**
**Suspected cause: Abrupt
**Frequency: Often
**Last seen:**
**Impact (Critical / annoying / cosmetic): Critical
**Confidence in cause (high / medium / low / unknown): Unknown

---

## Architectural diagnosis (Day 03 — Apr 29, 2026)

The triage process surfaced that these failures are not independent
bugs but symptoms of architectural rot:

1. Tests exist but are not enforced as gates — fixes can land red
2. Coupling between components is implicit, not designed — changes
   ripple unpredictably
3. Code was authored by Claude Code without an architect specifying
   boundaries — organic coupling was the inevitable result

**Verdict (preliminary, to be confirmed Saturday):** rebuild, not patch.
The prototype was the spec. v2 will be built using Vizuara curriculum
(starts May 5) as the architectural foundation, with each lecture's
domain (ASR, TTS, state machine, etc.) implemented as a clean module
in v2.

**No more patches to the existing codebase between now and Saturday.**
Saturday is for reading the codebase as data, not editing it.