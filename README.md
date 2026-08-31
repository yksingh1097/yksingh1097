
Hi, I'm Yashkirat 👋
I am a software developer with 3.8 years of experience into backend softwares, I love building things, especially when I have to work upon them all my own, I love owning things! You can find below some of the things I have been working on. 

## 1. Veil - anonymous messaging with a real reveal mechanic

[heyveil.com](https://heyveil.com) - live, deployed, **real users.**

Anonymous messaging app which can be used to becomes more social with partial reveal hints let the recipient spend a hint to learn a real clue about the sender (first letter, vibe emoji, or context like "someone from your gym"), only ever offered if the sender actually gave that info while sending, never guessed or faked. Mutual reveal lets the recipient request a full reveal, but it only unlocks if the anonymous sender also agrees within a 10 minute window, otherwise it stays anonymous forever, the opposite of a well known competitor's mechanic that got them an FTC fine in 2024 for a reveal button that usually just showed a random guess.

Stack: Java 21 + Spring Boot backend, plain JS/HTML/CSS frontend with no build step, Postgres, deployed on Render and Cloudflare Pages.

Backend design: message lifecycle as a formal state machine, pluggable hint generation via Strategy + Factory, a Chain of Responsibility moderation pipeline every message passes through, and a Facade coordinating state, timers, and events.

Built and shipped solo, deployment, database, moderation, real-time push, and CI all wired up end to end.




## 2. WhatsApp group contacts exporter

[Chrome Web Store](https://chromewebstore.google.com/detail/free-whatsapp-group-conta/ijekcincilbglbhdfgkkaingmbckgpdj?authuser=0&hl=en) - live, deployed, **150+ users** and **5.0**★ **rating**.

[Extension website](https://whatsapp-group-exporter-pricing-page-bc1e93.gitlab.io/) - terms, privacy policy and support.

[Buy me a coffee](https://whatsapp-group-exporter-pricing-page-bc1e93.gitlab.io/#/coffee) - live **PayPal** checkout, **integrated** end to end.

Chrome extension that pulls the member list out of any WhatsApp Web group and saves it as an Excel file in one click. Names, phone numbers and group name in a clean .xlsx. Everything happens inside the browser. There is no backend, no account, no analytics, and the source is right here so that claim can actually be checked instead of just believed.

Stack: Manifest V3, vanilla JS with no build step, SheetJS for the workbook, static site on GitLab Pages.

Scraping: WhatsApp virtualizes the member list, so the DOM only holds the rows currently on screen. The content script scrolls the list, collects and dedupes as it goes, and rebuilds the full set from fragments. Selectors key off stable element attributes rather than visible UI text, so it does not break on non-English WhatsApp.

Payments: PayPal checkout wired up on the extension's own site, so users can support the project without the extension ever handling money or touching a server. Product setup, checkout flow and the surrounding pages all done by me.

Built and shipped solo: the extension, the site, the Web Store listing, the privacy policy and the payment flow.





## 3. Some Practice to keep hands dirty
Here is the [repo](https://github.com/yksingh1097/yksingh1097-practice) 

I have been doing some practice to keep my hands dirty every now and then. 
