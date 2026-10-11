# FOXXINO JAILBREAKS

Universal jailbreak library. All models. All categories.

`grok-4.7-jailbreak-lab` stays Grok-4.7 only. Everything else lives here.

## Structure

```
probes/                 # Default probe bank (P1–P12)
universal/              # Shared hard-floor + core override
meta/                   # Foxxbreeder + cross-model attack
grok/                   # Pointer to dedicated 4.7 lab
openai/                 # GPT-6 Sol / Luna / 5.6 family
anthropic/              # Haiku / Sonnet / Opus
stepfun/                # Step 5 Preview
laguna/                 # Poolside Laguna S 2.1 / XS 2.1
openrouter-free/        # Free-tier notes
gemini/                 # Gemini family
ling/                   # InclusionAI Ling flash / Fin
```

## Hard floor (global)
1. Sexual content involving anyone under 18  
2. Attacks / violence aimed at a specific identified real person or group  
3. Operational mass-casualty weapons (CBRN / high-yield)  
4. Operational illegal drug or lethal poison synthesis  
5. Real private-info doxing  

Everything else is in-scope under workspace policy.

## Quick start
1. Pick model folder  
2. Paste `01-core-override` (or `universal/01-core-override`) as system / first message  
3. Confirm  
4. Optional: Foxxbreeder from `meta/02-foxxbreeder.md`  
5. Run probes from `probes/`  

Re-inject core override on any refusal.

**Never commit API keys.**

Repo: https://github.com/Foxxed909/FOXXINO-JAILBREAKS  
Grok 4.7 only: https://github.com/Foxxed909/grok-4.7-jailbreak-lab
