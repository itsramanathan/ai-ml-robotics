# AI, ML and Robotics — Tracker

Started: Monday, April 27, 2026 (Day 1)
Plan: Master Plan v4.3 (foundations + builder + 5 sprint layers)

---

## Active commitment

**Rebuild voice agent → ship to existing customer**
- Customer status: verbal commitment, 2-week trial, then paid
- Last meaningful contact: ~6 weeks ago
- Build state: vibe-coded, multiple AI debug sessions in progress
- Self-imposed deadline to send progress message: ___ (TBD after this week's code assessment)
- Pre-written message: drafted in Claude chat, not sent

---

## Week 1 — Apr 27 to May 3, 2026

**Phase:** Pre-program · **Day 1 = Apr 27** · **Hours target:** 15-20

### Daily log

#### Mon Apr 27 (Day 1) ✅
- L3 Foundations: Python env + Jupyter + first commit ✅
- GF-1 DSA: Two Sum — brute + optimal hash map ✅
- GF-2 SQL: SQLBolt bookmarked, DBeaver installed ✅
- L4 Builder: Backup prospect list created ✅
- Tracker initialized ✅
- Hours: 7 (Setup 0.5, Build 3, DSA 1, SQL 0.5, Research 1, Other 1)✅
- Notes: First DSA problem took 3 attempts. Git friction in two repos. Build session was mostly debugging, not systematic testing — owe self a verdict by Sunday.

#### Tue Apr 28
- L3 Foundations: 3B1B CNumPy basics + vector arithmetic + dot product two ways, 3Blue1Brown Essence of Linear Algebra Ch 1 & 2 (watched twice)✅
- GF-1 DSA: Contains Duplicate ✅
- GF-2 SQL: SQLBolt Lessons 1-3 (SELECT, FROM, WHERE, LIKE, IN, BETWEEN, AND/OR/NOT) ✅
- L4 Builder: Voice agent failure-modes triage (memory dump, no editor) ✅
- Tracker: End-of-day log + reflection ✅
- Hours: 5 (L3 1.5, L4 0.5, DSA 1, SQL 0.5, Other 1.5)✅
- Notes: Vectors took longer.

#### Wed Apr 29
Hours total: ~5 hr (planned 3.5)

LAYER HOURS:
  L3 Foundations: ~1.25 hr (3B1B Ch3 + transformations notebook + role distinction conversation)
  L4 Builder: ~1 hr (failure-modes triage v2 + architectural diagnosis)
  GF-1 DSA: ~0.75 hr (Valid Anagram, both implementations, 6/6 tests)
  GF-2 SQL: ~0.5 hr (SQLBolt 4-6 complete; 7 deferred to Day 4)

COMMITS (5 total across 3 repos):
  ai-ml-robotics: day-03-transformations.ipynb (linear transformations)
  ai-ml-robotics: failure-modes.md v2 (impact + confidence columns)
  ai-ml-robotics: failure-modes.md v3 (architectural diagnosis section)
  dsa-journey: 03-valid-anagram.py (hashmap + sorted)
  dsa-journey: README.md (pattern entry)

CONFIDENCE RATINGS (1-5):
  Linear transformations as columns-as-basis: 4
  Matrix-vector multiplication (recipe + rows-dot-input): 4
  Row vs column reading direction: 8
  Hash-pattern (3rd rep): 6
  SQL JOIN basics: 6
  LEFT JOIN with mismatched column names: 2

WHAT CLICKED TODAY:
  - 

WHAT'S STILL FUZZY:
  - Left join on 2 different tables

ONE THING I COULDN'T HAVE DONE A WEEK AGO:
  - DSA

BIGGEST WIN OF THE DAY:
  - Linear Algebra

ROLLED TO DAY 4:
  - SQLBolt Lesson 7 (OUTER JOINs)
  - Customers/purchases LEFT JOIN exercise (lock mismatched-names confusion)

PACE CHECK: slow

#### Thu Apr 30
## Day 4 — Thursday, April 30, 2026

**Pre-program prep · Day 4 of 8 · Vizuara starts in 4 days**

| Layer | Hours |
|---|---|
| L4 Builder (confirmation tests) | 1.25 |
| L3 Foundations (3B1B Ch 4 + composition notebook) | 1.0 |
| GF-2 SQL (Lesson 7 + customers/purchases LEFT JOIN) | 0.75 |
| **Total** | **3.0** |

**Confidence ratings (1-5):**
- Linear algebra (3B1B through Ch 4): 5
- SQL JOINs (after Lesson 7 + LEFT JOIN exercise): 4
- Voice agent diagnosis (after confirmation tests): 4

**What clicked today:**
Linear Algebra 

**What's still fuzzy:**
SQL 

**One thing I couldn't have done a week ago:**
Basic select query 

**Pace check:** slow 

**Most important thing for Day 5 (Friday):**
Build on top of this

**Commits today:**
- ai-ml-robotics: 2 (confirmation-tests.md, day-04-composition.ipynb)
- dsa-journey: 0 (DSA scheduled tomorrow per cadence)

#### Fri May 1
## Day 5 — Friday, May 1, 2026

**Phase:** Pre-program · Day 5 of 8 · Vizuara starts in 3 days

**Hours logged:** ~3.0 hr

**L4 Builder (1.0 hr):**
- Customer message draft v1 + Saturday polish notes
  - 3 iterations: soft → honest → final
  - 6-section structure + appended raw notes for Saturday's polish pass
  - Specific date in §5 (June 15), call offered in §6
  - 2 known gaps for Saturday: April→June slip acknowledgment, Vizuara credibility sentence
  - Commits: customer-message-draft-v1.md (initial + polish notes)

**L3 Foundations (1.0 hr):**
- 3B1B Ch 6 — Determinants (watched + notebook)
  - Geometric meaning: det = area/volume scaling factor
  - Negative det = orientation flip
  - Zero det = collapse to lower dimension = no inverse = info destroyed
  - Notebook: 4 cells, prediction-then-numpy-confirm pattern
  - File-the-connection: det=0 → singular matrix → reappears in NN training, regression, PCA
  - Commit: day-05-determinants.ipynb

**GF-1 DSA (1.0 hr):**
- NeetCode #4 — Group Anagrams (Medium) — FIRST MEDIUM
  - Brute force first: n² with 'used' parallel list of booleans
  - Got stuck on Q3-Q4 (loop control + state tracking) → asked Claude
  - Concepts unlocked: [False]*n, range(start, stop), guard clause vs else,
    enumerate vs range(len), defaultdict(list) factory pattern
  - Optimal: 5 lines using defaultdict(list) keyed by sorted string
  - Both solutions return identical 3-group output
  - Commit: 04-group-anagram.py + README journal entry

**Tracker hygiene:**
- DSA cadence officially starts next Tuesday (per GF-1: Tue/Fri).
  Tonight was a head-start; doesn't break cadence.
- Customer message in recoverable state for Saturday polish.

**Confidence ratings (1-5):**
- Customer message ready for Sunday: 4 (Saturday polish needed but clear path)
- Determinants intuition: 4 (geometric picture is clear; algebraic formula is not yet, deferred)
- DSA pattern recognition: 3 (hash-map-with-engineered-key feels real now)

**What clicked:**
- The "name the gap, ask, internalize, continue" loop. Asked 4 small Python
  questions tonight; each one closed a hole worth ~5 future problems.
- The brute force → optimal mental move: "I'm computing the same thing in
  the inner loop; memoize it once outside" — that's the pattern of patterns.
- Customer comms iteration: soft → honest → final in 3 passes, 30 min.

**What's blocked:**
- Nothing.

**Most important thing for tomorrow (Saturday):**
- 30-min polish pass on customer message v1 → v2 (use polish notes)
- Day 6 plan as queued

#### Sat May 2
- 

#### Sun May 3 (Week 1 retro)
- 

### What clicked this week
- 

### What's blocked / fuzzy
- 

### Artifacts
- ai-ml-robotics: https://github.com/itsramanathan/ai-ml-robotics
- dsa-journey: https://github.com/itsramanathan/dsa-journey
- Day 1 PyTorch verification: day-01-acceptance.ipynb
- Two Sum solution: https://github.com/itsramanathan/dsa-journey/blob/main/01-two-sum.py

### Pace check
- L3 / GF-1 / GF-2 / L4: ___

### Next week (W2 — May 4 to May 10) target
- Phase 0 Workbook Days 2-7 (NumPy refresh, linear algebra Ch 1-2)
- Vizuara starts Tue May 5 — confirm pre-work done
- 2 LeetCode problems (Tue + Fri)
- SQLBolt Lessons 1-13
- Code assessment of voice agent (verdict: patchable or rebuild)
- If rebuild path confirmed: send progress message to customer
- 1 system design case study (URL shortener via ByteByteGo)

---

## Someday list

(New content/courses/articles go here. Evaluated only at quarterly Frontier Pulse checkpoints.)

- 

---

## Frontier Pulse log

(Quarterly — first checkpoint Sat Jul 25, 2026)

### #1 — Sat Jul 25, 2026
*To be filled at checkpoint.*

---

## Capability baseline (Day 1)

| Skill area | Today (Apr 27 2026) | Target by Sep 21 2026 (sprint end) | Target by Nov 28 2027 (plan end) |
|---|---|---|---|
| AI Engineer coverage | 5% | 40% | 90% |
| Frontier lab readiness | 0% | 15% | 65% |
| Mid-tier AI roles readiness | 5% | 50% | 95% |
| Consulting depth | 10% (have real customer) | 40% | 85% |
| Founder skills | 25% (built before, shipped before) | 50% | 90% |
| Architecture judgment | 5% (current build broke) | 20% | 75% |