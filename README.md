<img width="2752" height="1536" alt="Persistent_AI_Framework_Overview" src="https://github.com/user-attachments/assets/856358f0-2ea5-42eb-beb9-71f9ab67e2cc" />
# Engineering-Persistent-Memory-and-Personality-in-OpenClaw-
Build AI with memory using OpenClaw. Set personality, store user context, and add security guardrails

# Give Your Assistant a Memory

---

## Introducing Today's Project!

In this project, I'm going to give my OpenClaw assistant a persistent memory and a distinct personality. Right now, most chat apps forget everything when I start a new conversation. But here, I'll make sure my assistant actually remembers me across sessions.

Specifically, I'll create two key files. First, SOUL.md, which defines how my assistant speaks and behaves. Second, USER.md, which teaches the assistant who I am and what I care about.

Then I'll have a real conversation and watch how OpenClaw automatically writes daily notes to remember context. Those notes live on my computer, not inside Telegram, but my assistant can still reference them next time I start a session.

This will help me understand how to build AI assistants that don't just reply intelligently in the moment, but actually learn and remember over time. That's a huge step beyond most basic bots.

I'm interested in this because I want my assistant to feel less like a tool and more like a collaborator. 

### Key tools and concepts

The key tools I used include SOUL.md to define my assistant's personality and communication style, USER.md to define my identity and preferences, and the openclaw.json configuration file with tool profiles like "coding" to set hard guardrails. I also used the "openclaw gateway restart" command to load changes and "openclaw security audit" to check my security posture. The automatic daily notes feature wrote memory from our conversations without me lifting a finger.

Key concepts I learned include the difference between manual memory (SOUL.md and USER.md) and automatic memory (daily notes). I also learned the distinction between soft guardrails (rules in SOUL.md that my assistant tries to follow) and hard guardrails (physical restrictions in the config that my assistant cannot bypass because the capabilities don't exist).

### Challenges and wins

I did this project today to learn how to give my OpenClaw assistant persistent memory and a unique personality, plus set up security guardrails that keep it safe as it becomes more powerful. Another skill I want to learn is connecting my assistant to external APIs and tools so it can take real actions, like sending messages or automating tasks across my workspace.

---

## Verifying the OpenClaw Setup

In this step, I'm verifying that my OpenClaw assistant from Part 1 is still up and running before I start adding memory and personality features.

I need to make sure three things are working. First, I'll confirm the OpenClaw gateway is still running on my computer. If I've restarted since Part 1, it probably stopped, so I may need to launch it again.

Second, I'll send a test message to my Telegram bot to verify the assistant actually responds. This is my quick health check. If the bot replies, I know the connection between Telegram and OpenClaw is solid.

Third, I'll check that my workspace directory still exists. That's where my SOUL.md and USER.md files will go, so I need to know that folder is ready.

This step is basically my baseline check. I can't build new features on a broken setup, so I'm taking two minutes to confirm everything from Part 1 is still functional. Once I verify these three things, I'll be ready to move forward with confidence.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_p3w8n5v2)

---

## Defining a Personality with SOUL.md

In this step, I'm creating a SOUL.md file that defines my assistant's personality, communication style, and behavioral rules. This file lives in my OpenClaw workspace and gets loaded every time the Gateway starts up.

I'm doing this because right now my assistant sounds generic, like any other chatbot. Without a SOUL.md file, it has no consistent identity. It doesn't know how I want it to speak, what kind of tone to use, or what rules to follow. By creating this file, I'm essentially giving my assistant a character. I can decide if it's formal or casual, verbose or concise, humorous or serious. I can even give it a name and set boundaries for how it interacts with me.

The reason this matters is persistence. Once I define these traits in SOUL.md, my assistant will maintain that personality across every session, every conversation, every time I start it up. It won't forget how I want it to behave. This is the first step toward making the assistant feel less like a generic tool and more 

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_m8t3k6y1)

### How Personality Changes Behavior

The SOUL.md file changes my assistant's behavior by giving it a consistent identity that persists across every session. Without this file, my assistant sounds generic like any other chatbot. With SOUL.md, the assistant loads these instructions at startup and follows them for every response.

The file influences three areas. Personality traits shape the assistant's attitude. Communication style determines sentence length and formality. Rules set boundaries like not inventing facts.

For my assistant, I defined the Steve Irwin style enthusiast. My chosen traits are curiosity, bravery, and relentless positivity. I want my assistant to use nature analogies to explain technical concepts. For communication style, I set short bursts of energy followed by one clear takeaway.

For rules, I set two boundaries. First, never invent facts about animals, safety, or tools. Say when unsure. Second, keep technical steps safe and actionable.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_v5n9b2x7)

---

## Teaching the Assistant About Me

In this step, I'm creating a USER.md file that tells my assistant who I am. This file lives in my OpenClaw workspace alongside SOUL.md and gets loaded every time the Gateway starts up.

I'm doing this because right now my assistant has a personality but no context about me. It doesn't know my name, my preferences, or anything that would make conversations feel personal. Without USER.md, every session starts from scratch. The assistant treats me like a stranger every single time I message it.

With USER.md, my assistant will know who it's talking to. It can greet me by name, remember what I care about, and tailor its responses to me specifically. This is the second half of the memory puzzle. SOUL.md defines the assistant's identity, and USER.md defines my identity.

After I create this file, I'll restart the Gateway so it loads both personalities. Then I'll test it by chatting in Telegram to see if my assistant acknowledges who I am.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_s3p7q4n9)

### Understanding SOUL.md vs USER.md

SOUL.md defines who the assistant is. It sets the assistant's name, personality traits, communication style, and behavioral rules. This file gives the assistant its identity and voice.

USER.md defines who I am. It contains my personal context like my name, timezone, what to call me, and my preferences for how the assistant should interact with me.

Together, they create a two-sided relationship. SOUL.md tells the assistant how to behave. USER.md tells the assistant who it's talking to. Both files are loaded at boot time so the assistant knows its own identity and mine from the start of every session.

---

## Having a Personalized Brainstorm

In this step, I'm having a real conversation with my assistant about my goals and interests to see how OpenClaw automatically writes and persists memory across sessions.

So far I've only done manual memory. I created SOUL.md to define my assistant's personality and USER.md to tell it who I am. Those are static files I wrote myself. But I don't want to edit a file every time I share something new.

This step shows me the automatic side of memory. When I talk about what matters to me, OpenClaw writes daily notes on its own. These notes capture key points from our conversation without me doing anything.

After the conversation, I'll check the daily note file OpenClaw created automatically on my computer. Then I'll test memory persistence by starting a new conversation and seeing if my assistant remembers what I told it.

Manual memory gives my assistant a foundation. Automatic memory lets it build a living record over time. Together they make the assistant feel like it actually knows me.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_u4b3k8w5)

### Three Sources of Context

The assistant uses three sources of context to personalize its responses.

First, it uses SOUL.md, which defines who the assistant is. This includes its name, personality traits, communication style, and behavioral rules. This shapes how it delivers recommendations, whether enthusiastic or calm, detailed or concise.

Second, it uses USER.md, which defines who I am. This includes my name, timezone, preferences, and any personal context I have written down. The assistant knows how I like to communicate and what matters to me from this file.

Third, it uses the ongoing conversation, including the daily notes OpenClaw automatically writes. This captures what I've told my assistant about my goals, interests, projects, and tech stack. The assistant pulls from this live record to make suggestions that feel personal, not generic.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_b7m2k9w4)

---

## Exploring Daily Notes and Memory Persistence

The assistant uses three sources of context to personalize its responses.

First, it uses SOUL.md, which defines who the assistant is. This includes its name, personality traits, communication style, and behavioral rules. This shapes how it delivers recommendations, whether enthusiastic or calm, detailed or concise.

Second, it uses USER.md, which defines who I am. This includes my name, timezone, preferences, and any personal context I have written down. The assistant knows how I like to communicate and what matters to me from this file.

Third, it uses the ongoing conversation, including the daily notes OpenClaw automatically writes. This captures what I've told my assistant about my goals, interests, projects, and tech stack. The assistant pulls from this live record to make suggestions that feel personal, not generic.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_y4d5r7j3)

---

## Configuring Security Guardrails

In this project extension, I learned that soft guardrails are rules written into SOUL.md that my assistant tries to follow. They are polite instructions, like asking someone not to touch something. A creative prompt could theoretically convince my assistant to bend them. Soft guardrails are policy, not physical locks.

Hard guardrails are physical restrictions in the OpenClaw configuration file. No matter what my assistant is asked, it cannot bypass them because the capabilities don't exist. Hard guardrails are like locking the cabinet instead of asking nicely. Even if I claim authority or create emotional urgency, my assistant cannot override hard guardrails.

The key difference: soft guardrails are a choice my assistant makes to follow rules. Hard guardrails are architectural limits where the capability does not exist.

![Image](http://learn.nextwork.org/radiant_blue_innocent_pawpaw/uploads/ai-openclaw-memory_w3x7y1z5)

---

## Wrapping Up

This project took me approximately 45 to 60 minutes from start to finish. The most challenging part was understanding the difference between soft and hard guardrails and remembering that hard guardrails mean the capability simply doesn't exist, not just that the assistant chooses to refuse. Testing the social engineering attack with emotional urgency helped this click for me.

---

---
