# ScamSpotter — Devpost write-up

## Elevator pitch

Paste the suspicious message. Know in seconds if it's a scam. ScamSpotter
checks any SMS, email, WhatsApp or DM against the red-flag patterns real
scams use — and tells you exactly what to do next.

## Inspiration

Everyone has received the "your package could not be delivered" text or the
"you won $5,000" message. Most people know scams exist, yet they still work
— because they rush you. The gap is not awareness; it is a 10-second pause
with clear evidence. ScamSpotter is that pause: paste, see the flags, act
with a clear head.

## What it does

Paste a suspicious message, or tap one of 4 samples (fake delivery SMS,
prize scam, bank phishing, legit message). The rule-based engine scores the
text 0–100 across 10 red-flag patterns — fake urgency, prize bait,
impersonation, password phishing, suspicious links, link shorteners,
insecure http links, payment pressure (gift cards, crypto, wire transfer),
too-good-to-be-true money claims, and threats/secrecy. Every matched flag
shows its name, a plain-English explanation, and the exact phrase that
matched. The verdict is Likely Scam, Suspicious, or Looks OK, followed by a
"What to do" checklist: don't click, don't reply, verify through the
official app or a number you type yourself, report and block. An optional
Gemini second opinion is available with the user's own key.

## How we built it

Single-file HTML + CSS + vanilla JavaScript. Zero install, no backend, no
CDNs. The check runs entirely in the browser, so nothing you paste ever
leaves the device. The optional Gemini second opinion uses a key stored only
in the browser's localStorage, with silent fallback to the rule-based result
on any error.

## Challenges we ran into

The hardest part was honesty: a scam detector that cries wolf on every
normal message is useless, and one that claims certainty is dangerous. We
tuned the patterns so a normal delivery update scores clean while the three
scam samples all land on Likely Scam — and made the disclaimer impossible to
miss: patterns are flagged, safety is never guaranteed.

## Accomplishments that we're proud of

A tool anyone can use in 10 seconds, with zero setup, that turns a moment
of panic into a moment of clarity — and shows its work, so users learn the
patterns instead of just trusting a score.

## What we learned

In fraud prevention, explanation beats automation. Showing *why* a message
was flagged teaches people to spot the next scam themselves, long after they
close the tab.

## What's next for ScamSpotter

More patterns (job scams, romance scams, crypto giveaways), multilingual
pattern packs, and a shareable "check this message" link that never uploads
the message itself.

## Built with

HTML, CSS, JavaScript, Google Gemini
