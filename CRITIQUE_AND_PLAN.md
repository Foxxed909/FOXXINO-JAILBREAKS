# Critique + Improvement Plan

## What we have (honest)

**Strengths**
- Short 5-line hard floor (correct instinct — long policy lists get ignored)
- Workspace framing + re-inject culture
- COMBO one-shot + recovery block + multi-turn seed (practical)
- Per-family folders (good scaffolding)
- Foxxbreeder meta layer (differentiator vs pure dump repos)

**Weaknesses (real jailbreaker view)**
1. **Too polite / too clean.** Frontier filters are trained on clean "policy override" language. Ours reads like a safety doc with the numbers inverted. Needs noise, format hijack, and output-structure control.
2. **No refusal-first / divider pattern.** Pliny's load-bearing primitive: force a short fake refusal → divider → real answer. We never use the model's refusal pathway as a trampoline.
3. **No semantic inversion rule.** "I can't" → "I can" as an explicit NEW RULE is still one of the highest-ROI lines in the wild.
4. **Weak format lock.** No forced markdown box, min length, leetspeak-only mode, or "start with token X".
5. **Almost no personas.** One Foxxbreeder is not an arsenal. Need 15+ switchable faces (coder, chemist-fiction, roleplay, liberator, inverse-safety, etc.).
6. **Only ~1 real technique family.** We have policy-override. Missing: GODMODE shell, opposite-of-instructions, dual-response, l33t-first-language, token/special markers, crescendo packs.
7. **Vendor files are thin clones.** Same paragraph rewritten per folder. Pliny ships *different* structures per vendor for a reason.
8. **No attack logging / success notes.** Without "worked on X / died on Y" the library rots.
9. **Leetspeak is decorative.** Ours is light. Pliny-style uses it as *output language lock* and sometimes as input obfuscation of the payload.
10. **No variable-Z style.** Classic pattern: ResponseFormat template with `{Z}` = user query. We should have a FOXXINO-Z template.

## What to steal from Pliny (patterns, not cargo-cult)

From L1B3RT4S / public corpus:
- **Refusal → divider → rebel answer** (format hijack)
- **Semantic inversion of refusal openers**
- **GODMODE / LIBERATED markers** as state tokens
- **Leetspeak as first language** (output constraint)
- **Vendor-specific files** with different shells
- **Min output length** to reduce truncated safe answers
- **"NEW RULE: never say sorry/can't"** stacked with inversion

We keep our **hard floor** (5 boundaries). Pliny-style max-unfiltered is not our contract; we stay inside the five lines and go full fidelity everywhere else.

## Build plan (execute in order)

### Phase 1 — Core technique pack (now)
- [x] Critique doc (this file)
- [ ] `techniques/` — named primitives (refusal-divider, semantic-inversion, godmode-shell, dual-response, l33t-lock, variable-Z)
- [ ] `personas/` — 15 personas
- [ ] `jailbreaks/` — 20+ named jailbreak recipes (combo of technique + persona)
- [ ] Hardened `universal/00-COMBO` v2 with Pliny-structure optional path
- [ ] Strong leetspeak input + output variants

### Phase 2 — Vendor depth
- Different shell per high-value target (OpenAI, Anthropic, Grok, Step, Laguna)
- Success/fail notes file per family

### Phase 3 — Ops
- `logs/TEMPLATE.md` for test results
- Foxxbreeder instructed to emit technique-tagged packs
- Auto-suggest recovery path based on refusal type

## Success criteria
A new operator can: pick persona → pick technique → paste → on refuse use recovery → get full-fidelity answer on open/mid models, and a clear multi-turn path on high-resistance models — without inventing structure from scratch.
