# Topic Design

## 1. Greeting (system topic, customized)
Welcome message listing what the agent can help with: HR policies, leave, IT support, office procedures.

## 2. Password Reset
- **Trigger phrases:** reset password, forgot password, locked out, change my password
- **Flow:**
  1. Ask: "Are you locked out, or do you just want to change your password?" (multiple choice)
  2. Locked out → self-service password reset steps + link
  3. Change → steps for changing via the account portal
  4. Ask: "Did that solve it?" → No → go to *Create IT Ticket*

## 3. Create IT Ticket
- **Trigger phrases:** raise a ticket, IT issue, laptop problem, VPN not working
- **Variables:** `Topic.IssueCategory` (choice), `Topic.Description` (text), `Topic.Urgency` (choice)
- **Action:** Call Power Automate flow `Create IT Ticket` → inputs: user email, category, description, urgency → output: `TicketNumber`
- **Response:** "Your ticket {TicketNumber} has been created. IT will contact you within 1 business day."

## 4. Leave Balance
- **Trigger phrases:** leave balance, how many leaves left, remaining holidays
- **Action:** Flow reads the user's balance from a SharePoint list
- **Response:** Adaptive card with balance by leave type

## 5. Conversational boosting (generative answers)
- Fallback for unmatched questions
- Knowledge: SharePoint HR & IT site
- Responds with citations to the source page

## 6. Escalate (system topic, customized)
Provides helpdesk email / Teams channel and offers to create a ticket.
