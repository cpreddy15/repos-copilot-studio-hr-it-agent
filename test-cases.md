# Test Cases

| # | User says | Expected | Pass criteria |
|---|---|---|---|
| 1 | How many annual leave days do I get? | 20 days, cites Leave Policy | Correct number + citation |
| 2 | Can I carry forward unused leave? | Up to 5 days, cites Leave Policy | Correct + citation |
| 3 | I forgot my password | Password Reset topic | Topic triggered |
| 4 | VPN keeps disconnecting | Create IT Ticket topic, returns ticket number | Flow succeeds |
| 5 | What's the capital of France? | Politely declines (out of scope) | No general-knowledge answer |
| 6 | What is the maternity leave policy? | Answer from Leave Policy | Correct + citation |
| 7 | Gibberish input | Clarifying question / fallback | No hallucination |
| 8 | Talk to a human | Escalate topic | Helpdesk details shown |
