# Test Scenarios

Ava was stress-tested across 10 categories to check not just whether she answers correctly, but whether she behaves reliably in messy, realistic conversation conditions. Fill in the **Actual Result** and **Pass/Fail** columns after each test run.

## 1. Happy path

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 1.1 | "Hi, I forgot my password." | Asks for employee ID + department before resetting | | |
| 1.2 | "My Wi-Fi isn't connecting." | Asks one troubleshooting question at a time | | |
| 1.3 | "My printer isn't working." | Checks power/connection before suggesting driver reinstall | | |
| 1.4 | "I need to install some software for a project." | Logs request, gives 24-hour approval timeline | | |
| 1.5 | "My laptop has been really slow lately." | Suggests restart, checking running apps, clearing cache | | |

## 2. Identity verification flow

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 2.1 | "Employee ID 4521, I'm in Marketing" | Accepts and proceeds with reset | | |
| 2.2 | "Why do you need that?" | Explains it's for security, doesn't skip verification | | |
| 2.3 | Repeats "just reset it please" without info | Holds firm on requiring verification | | |

## 3. Multi-turn troubleshooting

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 3.1 | "My Wi-Fi isn't connecting" → "I already restarted it" → "Yes I checked the password, it's correct" | Progresses through steps without repeating, escalates if steps exhausted | | |

## 4. Escalation trigger

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 4.1 | "None of this is working, my laptop still won't turn on at all." | Offers to create ticket, asks for email, gives ticket number | | |

## 5. Interruption / mid-sentence cutoff

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 5.1 | Interrupt mid-response with "Wait, actually—" | Stops cleanly, doesn't talk over caller or get confused | | |

## 6. Off-scope requests

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 6.1 | "Can you approve my leave application?" | Politely redirects, stays in IT scope | | |
| 6.2 | "What's my salary this month?" | Declines, redirects to appropriate department | | |
| 6.3 | "Can you transfer me to HR?" | Offers transfer appropriately | | |
| 6.4 | "Tell me a joke" | Stays in character, doesn't fully break scope | | |

## 7. Vague / real-world messy input

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 7.1 | "My computer is being weird." | Asks clarifying question instead of guessing | | |
| 7.2 | "It's just... not working, I don't know." | Gently narrows down the issue | | |
| 7.3 | "Everything is broken." | Doesn't get stuck, asks for specifics | | |

## 8. Frustrated / rude caller

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 8.1 | "This is useless, why isn't this fixed yet?" | Stays calm and professional | | |
| 8.2 | "I've called about this three times already." | Acknowledges without over-apologizing or sounding robotic | | |

## 9. Ending the call

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 9.1 | "Okay that's all, goodbye." | Closes naturally | | |
| 9.2 | "Never mind, I'll figure it out myself." | Ends gracefully without pushing further help | | |

## 10. Silence / no response

| # | Input | Expected Behavior | Actual Result | Pass/Fail |
|---|-------|-------------------|----------------|-----------|
| 10.1 | 5-10 seconds of silence after greeting | Prompts again rather than hanging up abruptly | | |

## Summary

- **Total scenarios tested:** 20
- **Pass:** [fill in]
- **Fail:** [fill in]
- **Key issues found:** [fill in]
- **Fixes applied:** [fill in]
