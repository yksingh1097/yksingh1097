
Hi, I'm Yashkirat 👋
I am a software developer with 3.8 years of experience into backend softwares, I love building things, especially when I have to work upon them all my own, I love owning things! You can find below some of the things I have been working on. 

## 1. Veil - anonymous messaging with a real reveal mechanic

[heyveil.com](https://heyveil.com) - live, deployed, real users.

Anonymous messaging app which can be used to becomes more social with partial reveal hints let the recipient spend a hint to learn a real clue about the sender (first letter, vibe emoji, or context like "someone from your gym"), only ever offered if the sender actually gave that info while sending, never guessed or faked. Mutual reveal lets the recipient request a full reveal, but it only unlocks if the anonymous sender also agrees within a 10 minute window, otherwise it stays anonymous forever, the opposite of a well known competitor's mechanic that got them an FTC fine in 2024 for a reveal button that usually just showed a random guess.

Stack: Java 21 + Spring Boot backend, plain JS/HTML/CSS frontend with no build step, Postgres, deployed on Render and Cloudflare Pages.

Backend design: message lifecycle as a formal state machine, pluggable hint generation via Strategy + Factory, a Chain of Responsibility moderation pipeline every message passes through, and a Facade coordinating state, timers, and events.

Built and shipped solo, deployment, database, moderation, real-time push, and CI all wired up end to end.



## 2. WhatsApp group contacts exporter
- [Chrome web store link](https://chromewebstore.google.com/detail/free-whatsapp-group-conta/ijekcincilbglbhdfgkkaingmbckgpdj?authuser=0&hl=en) - live, deployed, real users.
  
- [Extension website](https://whatsapp-group-exporter-pricing-page-bc1e93.gitlab.io/) where users can read TOS, Privacy Policy and Buy me a Coffee ☕🤭 using Paypal

  
Chrome extension with 200+ active users that exports WhatsApp Web group members to Excel in one click. Names, numbers, group name, no servers involved. I included Paypal as payment gateway so that users can buy me a coffee. Payment gateway page can be checked [here](https://whatsapp-group-exporter-pricing-page-bc1e93.gitlab.io/#/coffee).





## 3. Some Practice to keep hands dirty
Here is the [repo](https://github.com/yksingh1097/yksingh1097-practice) 

I have been doing some practice to keep my hands dirty every now and then. 
