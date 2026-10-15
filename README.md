# ScamSpotter — Paste the suspicious message. Know in seconds if it's a scam.

Scam messages work because they rush you. ScamSpotter slows the moment down:
paste the SMS, email, WhatsApp or DM, and it checks the text against the
red-flag patterns real scams use — fake urgency, prize bait, impersonation,
password phishing, suspicious links, payment pressure, too-good-to-be-true
money claims, and threats — plus lookalike-domain detection (paypa1-secure.com)
and scam-signature combos (prize + urgency, phishing + urgency, payment +
secrecy) — then shows a verdict, a 0–100 risk score, every
matched flag with a plain-English explanation, and a "What to do" checklist.

Built for the Next Byte Hacks V5 hackathon (judged on real-world Impact).

## How it works

1. **Paste** a suspicious message, or tap one of the 4 samples (fake
   delivery SMS, prize scam, bank phishing, legit message).
2. **Check** — a rule-based engine scores the text. Each matched pattern
   shows its name, why it matters, and the exact phrase that matched.
3. **Act** — a checklist: don't click, don't reply, verify through the
   official app or a number you type yourself, report and block.

## Safety / honesty

ScamSpotter flags *patterns*. It cannot guarantee a message is safe, and it
never claims certainty. A clean result is a good sign, not a proof — scammers
constantly invent new wording. A disclaimer says so on every screen.

## Modes

- **Rule-based check (default):** runs entirely in the browser. No key, no
  network, nothing leaves the device.
- **AI second opinion (optional):** your own Gemini API key (stored only in
  this browser's localStorage) asks Gemini for a second opinion. Any error
  falls back to the rule-based result, which still stands.

## Run it

Open `index.html` in any browser. Zero install, no build step, no backend.

## Live demo

https://yowanda.github.io/scamspotter/

## Privacy

No message you paste leaves the browser, except the optional Gemini request
when you ask for a second opinion. No tracking, no account.
