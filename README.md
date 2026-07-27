# Ava — AI IT Helpdesk Voice Agent

An AI voice agent that handles Level 1 IT support calls: password resets, Wi-Fi/VPN troubleshooting, printer issues, and software install requests — with automatic escalation to Level 2 when needed.

Why I built this

I came across Vapi while exploring how AI voice agents work under the hood, and wanted to understand the space hands-on instead of just reading about it. Since I'm targeting IT support and helpdesk roles, I built something directly relevant to that work: an agent that mirrors the kind of L1 triage a real support desk handles every day.

Stack
Voice orchestration: Vapi
LLM: Groq (Llama 3.3 70B)
Speech-to-text: Deepgram (Nova-2)
Entirely free-tier — no paid infrastructure used
What it does
Verifies caller identity (employee ID + department) before processing password resets
Walks through troubleshooting one step at a time, rather than dumping a full checklist on the caller
Detects when an issue can't be resolved with basic steps and escalates to Level 2, generating a ticket handoff
Stays within IT support scope — politely redirects off-topic requests (HR, payroll, etc.)
Handles interruptions and mid-conversation topic changes gracefully
System prompt

The full prompt used to configure the agent is in prompt.md.

Demo

A 60–90 second highlight reel showing password reset, multi-turn Wi-Fi troubleshooting, and an escalation flow: [add your trimmed video link/embed here]

Full 5-minute stress test recording: see demo/demo-link.md

Testing approach

I tested the agent against 10 categories of real-world conversational behavior — happy path, identity verification, multi-turn troubleshooting, escalation triggers, interruptions, off-scope requests, vague input, frustrated callers, call closure, and silence handling. Full scenario list and results: testing/test-scenarios.md

What I'd add next
Integration with a real ticketing system (Freshdesk/Zendesk) so escalations create actual tickets
Multi-language support (Hindi/Hinglish) for a broader caller base
Basic call analytics (common issue categories, escalation rate, average handle time)
Knowledge base lookup for less common issues beyond the five core scenarios
About me

Recent MCA graduate (AI & ML) exploring practical applications of AI in support/ops workflows. Open to IT Support, Helpdesk, and Operations Analyst roles. [Connect on LinkedIn / GitHub: imantasha]
