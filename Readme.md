# RAIA — The Calling Agent That Works While You Don't



**RAIA is your company's AI voice agent.**
She calls your clients. She gives updates. She asks the right questions. She remembers everything.
You just check the dashboard.



## ⚠️ Demo Notice

The backend powering RAIA is live but **private** — it's tied to my personal server, n8n workflows, and Google Sheets setup. You won't be able to plug this in and run it yourself without rebuilding the backend side.

This is also a **proof-of-concept**, not a production-ready product. There are known security gaps (see below) that need fixing before this is deployed in a real business environment.

That said — the core works. RAIA places real calls. She talks. She listens. She reports back.

**Suggestions, feedback, and ideas are very welcome.** Open an issue.

## Meet RAIA

Most businesses have the same problem: a list of clients that need to be called, updates that need to be communicated, and questions that need answers — and not enough hours in the day to do it all.

So it doesn't get done. Leads go cold. Clients feel ignored. Follow-ups slip through.

**RAIA fixes that.**

She is an AI voice agent that lives inside your company's dashboard. She knows your clients, knows their projects, knows what to say — and she picks up the phone so you don't have to. When she's done with a call, she logs everything: what the client said, whether they're planning a visit, a summary of the conversation. Your team sees it instantly.

No scripts to read. No calls to make. No follow-ups to remember.
RAIA handles it.

---

## What RAIA Does

**She calls your clients — and actually sounds human.**
Not a robocall. Not a stiff IVR. RAIA speaks naturally in Hindi, English, or Hinglish depending on how the client talks. She introduces herself, delivers the update, asks about their plans, and wraps up the call warmly.

**She knows what to say because you tell her once.**
When you add a client, you write one progress update — *"Foundation 60% complete, electrical starts next week."* RAIA turns that into a full, natural conversation. You never write a script.

**She records everything.**
After every call: transcript saved, site visit intent captured (Yes / Maybe / No), preferred date noted, summary written. All of it back in the dashboard within minutes.

**She keeps your whole team in sync.**
Results push automatically to Google Sheets. Email summaries go out after every call. Everyone knows what every client said — without being on the call.

**She answers questions about your business.**
RAIA has a built-in AI chat. Ask her anything: *"Who confirmed a site visit this week?"* or *"Which clients haven't been called yet?"* or *"What's the status on Tower A?"* She answers instantly, because she has full context of your client data and call history.

**She works on your schedule.**
Set a calling window — say, 9am to 7pm — and RAIA only calls within those hours. If a client doesn't pick up, she retries once. If you want to pause a client, one click does it.

---

## How It All Works — Step by Step

You don't need to be technical to understand this. Here's the full picture:

**Step 1 — Add your clients**
Use the dashboard to add clients one by one, or upload a CSV with your whole list. Each client needs: name, phone number, project name, and a short progress update.

**Step 2 — RAIA gets to work**
The moment a client is set to Active, RAIA schedules a call. She uses a voice AI service called Bland AI to place a real phone call — from a real number — to your client.

**Step 3 — The conversation happens**
RAIA calls the client, speaks naturally, delivers the project update, and asks: *"Are you planning a site visit? What day works for you?"* The client responds like they would to any person on the phone.

**Step 4 — RAIA reports back**
After the call, the recording and transcript are processed. RAIA extracts the key information — visit intent, preferred date, what the client said — and writes it all to the dashboard and Google Sheets automatically.

**Step 5 — Your team sees everything**
The dashboard updates in real time. Your sales manager, your admin, anyone with access — they all see the same picture. Who was called, what they said, who needs a follow-up.

**Step 6 — You ask RAIA questions**
At any point, open RAIA Chat and ask whatever you need. She knows the data. She'll answer.

---

## The Stack

| What | Why | Tool |
|---|---|---|
| Voice calls | Places and conducts the AI phone calls | [Bland AI](https://bland.ai) |
| Automation backbone | Connects calls → Sheets → Email | [n8n](https://n8n.io) |
| Data & reporting | Stores and shares call results | Google Sheets |
| AI chat assistant | Answers questions about your business | Claude by Anthropic |
| Frontend dashboard | Everything you see and interact with | HTML / CSS / JavaScript |

---

## Known Security Issues (Please Read)

This is a demo. These gaps exist and need fixing before going live with real client data:

| Issue | Current State | What's Needed |
|---|---|---|
| API keys | Stored in browser localStorage | Move to a secure backend / env vars |
| Authentication | None — URL = access | Add login / password gate |
| Data encryption | Client names & phones unencrypted | Encrypt sensitive fields at rest |
| Backend validation | Frontend trusts itself | Server-side validation on all mutations |
| CORS | Wide open | Restrict to known origins |
| Multi-user | Single user only | Roles, teams, permissions |

I'd genuinely welcome pull requests or suggestions on any of these.

---

## What I'd Love Feedback On

- Better API key handling — what's the simplest secure pattern for a solo-built tool like this?
- Making the n8n workflow exportable so others could import it
- Replacing localStorage with a lightweight backend (Supabase? PocketBase?)
- Handling mid-call failures from Bland AI more gracefully
- Internationalisation — RAIA speaks Hinglish today, could she speak Tamil? Bengali?

---

## Who Could Use Something Like This?

RAIA was built for real estate — but the problem she solves isn't unique to real estate.

Any business that has a client list and needs to call them regularly could use her:

- **Real estate** — project updates, site visit follow-ups, possession reminders
- **Healthcare** — appointment reminders, post-visit check-ins
- **Education** — parent updates, fee reminders, admission follow-ups
- **Property management** — maintenance updates, inspection scheduling
- **Financial services** — document collection, KYC follow-ups

If your team is spending hours on the phone doing routine calls — RAIA can take that off their plate.

---

## Project Status

🟡 **Demo — actively in development**

| Feature | Status |
|---|---|
| Core calling loop | ✅ Working |
| Dashboard | ✅ Working |
| n8n backend | ✅ Live (private) |
| Google Sheets sync | ✅ Working |
| RAIA Chat | ✅ Working |
| Production security | ❌ Not yet |
| Public backend | ❌ Not yet |

---

## Want to See It Live?

The backend is mine, so I can run a demo. If you're curious what RAIA actually sounds like on a call, or want to see the full dashboard in action — open an issue or reach out. Happy to show it.

---


*Built by a solo founder who got tired of watching leads go unanswered.*

**RAIA — your company's smartest employee. She never misses a call.**

</div>
