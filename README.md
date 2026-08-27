
Hi, I'm Yashkirat 👋
I am a software developer with 3.8 years of experience into backend softwares, I love building things, especially when I have to work upon them all my own, I love owning things! You can find below some of the things I have been working on. 


🔗 Veil — anonymous messaging with a real reveal mechanic
heyveil.com · Live, deployed, real users
Anonymous-messaging app (NGL/Sendit category) with two things that set it apart from the usual playbook:
Partial reveal hints — the recipient can spend a hint to learn a real clue about the sender (first letter, vibe emoji, or context like "someone from your gym"). A hint is only ever offered if the sender actually supplied that info when sending — never guessed or faked.
Mutual reveal — the recipient can request a full reveal, but it only happens if the anonymous sender also agrees, within a 10-minute window. No response = stays anonymous forever. (This is the opposite of a well-known competitor's mechanic, which got them an FTC fine in 2024 for a reveal button that usually just showed a random guess.)
Stack: Java 21 + Spring Boot backend, vanilla JS/HTML/CSS frontend (no build step), Postgres, deployed on Render + Cloudflare Pages.
A few of the design patterns in the backend:
State — message lifecycle (received → moderated → hint-revealed → reveal-requested → revealed/expired/declined) modeled as a formal state machine, each state its own class.
Strategy + Factory — pluggable hint generation, one strategy per hint type.
Chain of Responsibility — a moderation pipeline (length → profanity → spam → harassment pattern) every message passes through before it's shown.
Facade — a single service coordinates the state machine, expiry timers, and event publishing behind a simple interface.
Observer — WebSocket push, analytics logging, and browser push notifications all react to the same event independently.
Built and shipped solo — deployment, database, moderation pipeline, real-time push, and CI all wired up end to end.
