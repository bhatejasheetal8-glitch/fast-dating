# FAST — Instant Dating (India)
## Product Requirements Document

**Version:** 1.1
**Last Updated:** January 2026
**Product Owner:** FAST Product Team
**Status:** Draft

---

## Table of Contents
1. [Executive Summary](#1-executive-summary)
2. [Problem Statement](#2-problem-statement)
3. [Target Users & Personas](#3-target-users--personas)
4. [Product Goals & Success Metrics](#4-product-goals--success-metrics)
5. [Core Features & User Flows](#5-core-features--user-flows)
6. [Functional Requirements](#6-functional-requirements)
7. [Design System & Brand Guidelines](#7-design-system--brand-guidelines)
8. [Appendix](#8-appendix)

---

## 1. Executive Summary

### 1.1 Product Vision
FAST is a dating app designed for **India's "instant" culture**—quick commerce, reels, low attention spans. Instead of endless chatting, it makes **activity + availability + expectations** visible upfront, so people can move from match → meeting with minimal friction.

### 1.2 Core Philosophy: Activity-First, Not Partner-First
**The most important principle of FAST:** Intentions are never stated explicitly. Users don't declare they're "looking for a relationship" or "finding a partner"—that creates pressure and awkwardness.

Instead, users simply choose **activities they want to do** (pottery, coffee, live music, etc.). When two people share interest in the same activity, they can meet to do that activity together. The meeting feels natural because there's a pre-decided, shared purpose—not a high-stakes "date" evaluation.

> **Why this works:** "Let's do pottery together" feels lighter than "Let's see if we're compatible partners." The activity becomes the reason to meet, and any romantic connection emerges organically.

### 1.3 Core Value Proposition
**"Less talking, more meeting (without the awkwardness)."**

FAST is especially helpful for:
- **Busy professionals** who lack time for endless back-and-forth
- **Introverts** who struggle with performative chat dynamics

### 1.4 Key Differentiators
| Traditional Dating Apps | FAST |
|------------------------|------|
| Explicit "looking for relationship" labels | Activity-first matching—no stated romantic intent |
| Endless chatting before meeting | Shared activity gives natural reason to meet |
| Manual bio writing | Auto-generated introductions from quick questions |
| Ambiguous scheduling | Clear time slots visible on profiles |
| Ghosting cycles | Structured, low-pressure interactions |
| Catfishing risk | Quick alignment via video/voice call before meeting |

---

## 2. Problem Statement

### 2.1 User Pain Points
| Problem | Description |
|---------|-------------|
| **Forced small talk** | Users spend excessive time on superficial conversations |
| **Planning fatigue** | Coordinating schedules is mentally exhausting |
| **Mental exhaustion** | Dating app interactions feel like a chore |
| **Ghosting cycles** | Conversations fizzle without real-world meetings |
| **Scheduling friction** | No clear way to align availability |
| **High-pressure framing** | "Looking for a partner" creates awkward expectations |
| **No reason to meet** | Without a shared activity, meetings feel like interviews |
| **Catfishing anxiety** | No way to verify if the person is genuine before meeting |
| **Time wastage** | Investment in chats that lead nowhere |

### 2.2 How FAST Solves These Problems
| Solution | Implementation |
|----------|----------------|
| **Activity-first matching** | Users choose activities they want to do; matches happen based on shared interests—no explicit "looking for partner" labels |
| **Natural meeting context** | When both parties want to do pottery (or any activity), the meeting has built-in purpose and lower pressure |
| **Clear expectations** | Bill preferences, activity types visible on profile |
| **Auto introductions & quick replies** | No typing required to start conversations |
| **Small talk made easy** | Pre-built conversation starters and quick responses |
| **Availability-led discovery** | Users see others' time slots based on distance settings; optional filter to show only people available in user's own time slot |
| **Introvert-friendly flow** | Structured interactions reduce social anxiety |
| **Quick alignment** | Video/voice call option to check the vibe and verify the person is genuine before meeting in person (anti-catfishing) |

---

## 3. Target Users & Personas

### 3.1 Primary Market
Urban India (Tier 1 cities), starting with Bangalore

### 3.2 Jobs To Be Done
> "Help me find someone who wants to do the same activity as me, at a time that works for both of us, so we can meet naturally without the pressure of a traditional 'date.'"

### 3.3 User Personas

#### Persona 1: Emotional Gen-Z
| Attribute | Details |
|-----------|---------|
| **Demographics** | Male, 22, Undergraduate |
| **Lifestyle** | Reels-heavy, fast decisions, social but selective |
| **Needs** | Emotional clarity, vibe match, low effort |
| **Motivation** | Meet someone who "gets it" quickly |
| **Traits** | Expressive, intuitive, impatient with boring chats |
| **Frustration** | *"I'm tired of texting for days just to realize we're not even on the same vibe."* |

#### Persona 2: Busy Professional
| Attribute | Details |
|-----------|---------|
| **Demographics** | Male, 28, Graduate / Professional diploma |
| **Lifestyle** | Gym, work, routines, high standards, time-poor |
| **Needs** | Efficient filtering, quick planning, confidence in intent |
| **Motivation** | Dating without losing momentum or time |
| **Traits** | Structured, decisive, quality-seeking |
| **Frustration** | *"I don't have energy for endless back-and-forth that never turns into a real plan."* |

#### Persona 3: Quiet Introvert
| Attribute | Details |
|-----------|---------|
| **Demographics** | Male, 30, Graduate |
| **Lifestyle** | Small circle, thoughtful, prefers calm settings |
| **Needs** | Low-pressure interactions, structured icebreakers, safety |
| **Motivation** | Meet someone without social overload |
| **Traits** | Observant, sincere, anxious about first moves |
| **Frustration** | *"I freeze when chats turn performative—dating apps feel louder than real life."* |

---

## 4. Product Goals & Success Metrics

### 4.1 Primary Goals
1. Reduce time from match to first activity together
2. Increase meeting conversion rate (matches that become real-world activities)
3. Decrease ghosting rate through shared activity purpose
4. Create a low-pressure, activity-focused meeting experience
5. Reduce catfishing through quick alignment (video/voice verification)

### 4.2 Key Performance Indicators (KPIs)
| Metric | Description |
|--------|-------------|
| Match-to-Activity Conversion | % of matches that result in scheduled activities |
| Time-to-Meeting | Average hours from match to confirmed activity |
| Quick Alignment Usage | % of users who do video/voice call before meeting |
| Activity Completion Rate | % of scheduled activities that actually happen |
| User Retention (D7/D30) | Users returning after 7 and 30 days |
| Completion Rate | % of users completing full onboarding |

---

## 5. Core Features & User Flows

### 5.1 User Journey Overview
```
Welcome → Login/Signup → Profile Creation → Activity & Availability Setup → Discovery → Matching → Chat → Quick Alignment (optional) → Activity Together
```

**Key principle:** The journey leads to a shared activity, not a "date." Users are meeting to do something together, which removes pressure and creates natural conversation.

### 5.2 Authentication Flow

#### Welcome Screen
- Display FAST branding with login and signup options
- Clean, minimal interface with neon-dark theme

#### Phone Authentication
- Phone number input → "Send OTP" button
- OTP verification screen
- **Prototype behavior:** Auto-fill dummy OTP to proceed

### 5.3 Profile Creation (Onboarding)

#### Step 1: Basic Information
- **Name:** Text input
- **Age:** Modern control (slider, segmented control, or picker sheet—not old-school steppers)

#### Step 2: Photos
- "Add Photos" opens a **dedicated photo management page**
- User must add **4 photos**
- Return to main profile flow after completion

#### Step 3: Bio Builder (No Manual Typing)
- "Create Bio" opens a **dedicated page** with ~10 quick questions
- Each question presents selectable options (single/multi-select)
- App **auto-generates** a short intro/bio from selected answers

**Bio Questions:**
| Question | Options |
|----------|---------|
| Pet preference | Cat person / Dog person / Both / Neither |
| Beverage | Coffee / Matcha / Chai / Cold brew |
| Weekend vibe | Home reset / Outdoors / Cafe hopping / Party |
| Movie type | Comedy / Romance / Thriller / True crime |
| Work style | Home / Office / Cafe / Hybrid |
| Fitness | Gym / Run / Yoga / Sports / None |
| Social battery | Extrovert / Ambivert / Introvert |
| Ideal date | Coffee / Drinks / Dinner / Walk |
| Music mood | Indie / Bollywood / Techno / Lo-fi |
| Communication style | Direct / Playful / Soft / Minimal |

#### Step 4: Bill Preference
- Icon: **₹ (Rupee symbol)**
- Options: Split 50–50 / Alternate / My treat

#### Step 5: Quick Alignment Preference
**Purpose:** Let users verify the other person's vibe before meeting in person—helps prevent catfishing and ensures genuine connection.

- Options: 5-minute voice call / 5-minute video call / No preference
- This preference is shown on the user's profile
- When both users have selected a call preference, the chat interface prominently suggests scheduling a quick call before the activity

#### Step 6: Activity Selection (Core Matching Criteria)
**This is the heart of FAST's matching logic.** Users select activities they genuinely want to do. Matches are shown based on shared activity interest.

- Activities: Coffee, Movie, Drinks, Dinner, Comedy show, Walk, Museum, Live music, Board games, Dessert, Mental health talk, Books/cafe, Fitness date, Pottery, Cooking class, Art gallery
- Users can select multiple activities
- Discovery prioritizes users who share at least one activity preference
- The shared activity is displayed prominently on match profiles

#### Step 7: Area Selection
- User types area name
- **Bottom sheet** displays:
  - Typed area + distance from current location (e.g., "Indiranagar — 2 km")
  - 3 nearby area suggestions (e.g., Indiranagar, Koramangala, HSR)
- Use Bangalore areas only for prototype

#### Onboarding Completion
- Full-screen success message: *"You're all set! Find someone who wants to do what you love."*
- Modern illustration/animation in neon-dark theme
- Emphasizes activity, not "dating" or "finding a partner"

### 5.4 Discovery & Matching

#### Matching Philosophy
Users are matched based on **shared activities**, not explicit relationship intent. When you see a profile, it means:
1. You both want to do at least one of the same activities
2. They are within your distance settings
3. Their availability is visible (so you can see if times might work)

#### Session-Based Discovery Setup
Before browsing profiles, users set their **intent for this session**:
1. **Select activity for now:** Choose what they want to do right now (e.g., "Drinks," "Coffee")
2. **Set availability:** Pick a time slot for today (e.g., "7:00 PM – 9:00 PM")

This session filter narrows discovery to profiles that match the selected activity. Users can change these settings anytime from the discovery screen header.

> **Example:** Priya opens the app at 5:30 PM, sets availability for 7–9 PM today, and selects "Drinks." She now sees profiles of people who also selected "Drinks" as an activity.

#### Availability-Led Discovery
- Users see other profiles' **time slots** based on their distance settings
- **Default behavior:** All profiles within distance are shown with their availability visible, **regardless of time slot overlap**
- Users can match with someone even if time slots don't perfectly align (they can negotiate timing in chat)
- **Optional filter:** "Show only people available in my time slot" narrows results to overlapping availability
- This filter is accessible from the discovery screen header

#### Profile Cards
- Generate **100+ fake profiles** with varied:
  - Availability times
  - Shared activity interests (the reason for the match)
  - Personality answers
- Each profile displays **4 photos**
- **Photo navigation:** Tap to advance to next photo (Tinder-style)
- **Shared activities badge:** Prominently shows which activities you both selected

#### Interaction Model
- **Primary interaction:** Swipe gestures (swipe right to like, swipe left to unlike)
- **Alternative:** Like/Unlike buttons (thumbs/tick/cross style) for users who prefer tapping
- **Unlike animation:** Card flies left (trash-like motion)
- **Like animation:** Card flies right with golden glow accent
- **Auto-sent introduction:** When user likes a profile, their auto-generated intro is automatically sent
- After like: Show popup *"Your intro has been sent to {Name}"* for 5 seconds
- **Match popup:** Display for 1 out of every 3 likes
- Do NOT auto-navigate to chat after like

### 5.5 Matches Screen

#### Display Requirements
- Show **name** prominently
- Show **shared activity** (e.g., "Both want: Pottery, Coffee")
- Show **availability as time range** (e.g., "6–8 PM", "7–9 PM")
- Shared activity + availability slot are the key decision factors for who to message first

### 5.6 Chat Screen

#### Header
- Display: **Name, Age, Shared Activity, Availability slot**
- Profile photo tap → Opens full profile
- Shared activity shown as badge (e.g., "🍻 Drinks")

#### Auto-Received Introduction
- When opening a chat, the user sees the **other person's auto-generated intro** already displayed
- This creates immediate context without requiring manual first messages

#### Quick Reply System (Minimal Typing Flow)
The chat offers **tap-to-communicate** via quick reply chips for common responses. Manual typing is **always available** for users who prefer it.

**Quick Reply Categories:**

| Category | Example Quick Replies |
|----------|----------------------|
| **Meeting Intent** | "Are you up for meeting today?" / "Want to meet this week?" |
| **Availability Confirmation** | "Yes, that time works!" / "Can we do a bit later?" |
| **Venue Discussion Starters** | "Yes, but where do you want to meet?" / "Any place you prefer?" |
| **Activity-Specific** | "Want to grab drinks at [time]?" / "Coffee sounds great!" |
| **Send Introduction** | Sends the auto-generated intro from Bio Builder |

**Design principle:** Quick replies reduce friction for common exchanges, but the keyboard is always accessible. Users can type freely at any point in the conversation.

#### Venue Discussion
Once both users agree to meet:
1. Users suggest specific venues via chat (e.g., "How about Toit in Indiranagar?")
2. Users exchange venue suggestions and finalize timing

#### Quick Alignment (Anti-Catfishing)
**Purpose:** Let users verify the other person's vibe and authenticity before meeting in person.

- **Call request flow:**
  1. User taps "Request Call" button (voice or video)
  2. Other user receives call request notification in chat
  3. Other user taps "Accept" or "Decline"
  4. If accepted, call initiates immediately
- If both users have selected a call preference in their profile, show banner: "You both prefer a quick call before meeting—schedule one?"
- Call acts as vibe check before committing to in-person activity
- On-screen keyboard visible for realism

### 5.7 Time & Calendar

#### Availability Selection
- Remove "now" from time slot options
- Calendar picker for **next 7 days**
- Time ranges (not single times)

---

## 6. Functional Requirements

### 6.1 Authentication
| ID | Requirement | Priority |
|----|-------------|----------|
| AUTH-01 | Support phone number + OTP login | P0 |
| AUTH-02 | Support both new signup and returning user login | P0 |
| AUTH-03 | Prototype: Auto-fill dummy OTP for testing | P0 |

### 6.2 Profile Management
| ID | Requirement | Priority |
|----|-------------|----------|
| PROF-01 | Name and age capture with modern UI controls | P0 |
| PROF-02 | Photo upload (exactly 4 photos required) | P0 |
| PROF-03 | Bio generation from questionnaire (no manual typing) | P0 |
| PROF-04 | Bill preference selection with ₹ icon | P1 |
| PROF-05 | Quick alignment preference (voice/video call before meeting) | P0 |
| PROF-06 | Activity type selection (16 options) — core matching criteria | P0 |
| PROF-07 | Area selection with location-aware suggestions | P0 |
| PROF-08 | No explicit "looking for" or relationship intent fields | P0 |

### 6.3 Discovery
| ID | Requirement | Priority |
|----|-------------|----------|
| DISC-01 | Generate 100+ fake profiles for prototype | P0 |
| DISC-02 | Profile cards with 4 photos, tap-to-navigate | P0 |
| DISC-03 | Swipe gestures (right to like, left to unlike) as primary interaction | P0 |
| DISC-04 | Like/Unlike buttons as alternative to swiping | P1 |
| DISC-05 | Card animations (left for unlike, right+glow for like) | P1 |
| DISC-06 | Auto-send user's intro when they like a profile | P0 |
| DISC-07 | "Your intro has been sent to {Name}" popup after like (5 seconds) | P0 |
| DISC-08 | Match popup for 1 in 3 likes | P0 |
| DISC-09 | Match based on shared activity interest (core logic) | P0 |
| DISC-10 | Display shared activities prominently on profile cards | P0 |
| DISC-11 | Show availability time slots on profiles (based on distance settings) | P0 |
| DISC-12 | Optional filter: "Show only available in my time slot" | P1 |
| DISC-13 | Distance-based filtering | P0 |
| DISC-14 | Session-based activity filter (select activity before browsing) | P0 |
| DISC-15 | Session-based availability setting (set time slot for today) | P0 |
| DISC-16 | Allow matching with non-overlapping time slots (negotiate in chat) | P0 |

### 6.4 Matching & Chat
| ID | Requirement | Priority |
|----|-------------|----------|
| CHAT-01 | Match list showing name + shared activity + availability range | P0 |
| CHAT-02 | Chat header with name, age, shared activity badge, availability | P0 |
| CHAT-03 | Auto-display other user's intro when opening chat | P0 |
| CHAT-04 | Quick reply chips for meeting intent (e.g., "Are you up for meeting today?") | P0 |
| CHAT-05 | Quick reply chips for availability confirmation | P0 |
| CHAT-06 | Quick reply chips for venue discussion starters | P0 |
| CHAT-07 | Activity-specific quick reply options | P1 |
| CHAT-08 | Manual typing always available (keyboard accessible at all times) | P0 |
| CHAT-09 | Voice and video call request button (Quick Alignment) | P0 |
| CHAT-10 | Call request/accept/decline flow | P0 |
| CHAT-11 | Quick Alignment banner when both users prefer a call | P0 |
| CHAT-12 | On-screen keyboard UI (always accessible) | P2 |

### 6.5 Calendar & Scheduling
| ID | Requirement | Priority |
|----|-------------|----------|
| CAL-01 | 7-day calendar picker for availability | P0 |
| CAL-02 | Time range selection (not single times) | P0 |
| CAL-03 | No "now" option in time slots | P0 |

---

## 7. Design System & Brand Guidelines

### 7.1 Brand Identity

#### Brand Positioning
- **Premium, confident, modern, distraction-free focus** (Black)
- **Speed, energy, "instant action," high clarity** (Neon)

#### Logo Direction
- Logo mark + FAST wordmark (not text-only)
- Style: Modern, minimal, geometric
- Cues: Speed / lightning / forward motion
- Neon treatment: Soft glow, not harsh

#### Glow Rules
| Property | Value |
|----------|-------|
| Glow color | `#BEEE02` |
| Outer glow | 12–20px blur, 20–35% opacity |
| Inner glow (optional) | 6–10px blur, 12–18% opacity |
| Application | Logo and key active elements only—never large backgrounds |

### 7.2 Color Palette

#### Primary Colors
| Name | Hex | Usage |
|------|-----|-------|
| Black (Base) | `#0F1008` | Primary background |
| Neon Accent | `#BEEE02` | CTAs, active states, highlights |

#### Supporting Neutrals
| Name | Hex | Usage |
|------|-----|-------|
| Text on dark | `#F5F7EB` | Primary text |
| Muted text | `#A7AD93` | Secondary text, labels |
| Surface/Card | `#17180F` | Card backgrounds, elevated surfaces |
| Divider | `rgba(190, 238, 2, 0.12)` | Separators, borders |

#### Neon Usage Rules
- **Use for:** Primary CTAs, active states, key highlights, focus rings, progress/selection indicators
- **Avoid:** Large background areas—neon is the "spark," not the wallpaper
- High contrast improves scannability and supports rapid decisions

### 7.3 Typography

| Element | Size | Weight | Line Height |
|---------|------|--------|-------------|
| Display/H1 | 28–32px | Semibold | 130% |
| H2 | 20–22px | Semibold | 130% |
| Body | 15–16px | Regular | 150% |
| Caption/Meta | 12–13px | Medium | 140% |

### 7.4 Layout & Spacing

**Grid:** 8pt grid throughout

| Element | Specification |
|---------|---------------|
| Screen padding | 16px left/right |
| Section spacing | 24px between major blocks |
| Component spacing | 12–16px between related elements |
| Safe top padding | 16–24px (device dependent) |

### 7.5 Component Specifications

#### Buttons
| Property | Value |
|----------|-------|
| Height | 48–52px |
| Corner radius | 14–18px |
| Horizontal padding | 16–20px |
| Disabled opacity | 40–50% |

#### Cards
| Property | Value |
|----------|-------|
| Radius | 18–24px |
| Padding | 16–20px |
| Shadow | Minimal; use surface color for elevation |

#### Inputs
| Property | Value |
|----------|-------|
| Height | 48–52px |
| Radius | 14–16px |
| Focus ring | 2px neon outline (`#BEEE02`) with subtle glow |

#### Dividers
| Property | Value |
|----------|-------|
| Height | 1px |
| Color | Low-opacity neon-tinted or neutral |
| Spacing | 16–20px vertical |

#### Icons
| Property | Value |
|----------|-------|
| Size | 20–24px |
| Touch target | 44px minimum |

---

## 8. Appendix

### 8.1 Glossary
| Term | Definition |
|------|------------|
| Activity-first matching | Core FAST philosophy: users match based on shared activities (not explicit relationship intent), creating natural reasons to meet |
| Auto-sent introduction | When a user likes a profile, their auto-generated bio is automatically sent to that person |
| Availability-led discovery | Users see other profiles' time slots based on distance settings; optional filter narrows to overlapping availability only |
| Bio Builder | Feature that generates user bios from quick questionnaire responses |
| Quick Alignment | Pre-meeting video/voice call to verify the other person's vibe and authenticity (anti-catfishing measure) |
| Quick reply system | Tap-to-communicate chat interface using pre-built response options; minimizes typing in early conversation |
| Session-based filtering | Setting activity and availability for the current browsing session before swiping |
| Shared Activity | The activity both users have selected (e.g., pottery, coffee), displayed prominently as the reason for the match |
| Venue discussion phase | Chat phase where users suggest and agree on specific meeting locations |

### 8.2 Out of Scope (v1.0)
- Payment/subscription features
- Real location services (prototype uses hardcoded Bangalore areas)
- Real OTP verification
- Backend matching algorithm
- Push notifications
- Profile verification

### 8.3 Future Considerations
- Expand to other Tier 1 cities
- Add women-focused safety features
- Implement premium tiers
- Add group date features
- Integrate with calendar apps

### 8.4 Sample User Journey

This end-to-end example illustrates how FAST is intended to be used:

---

**User:** Priya (looking to meet someone for drinks tonight)

**5:30 PM — Session Setup**
1. Priya logs into FAST
2. She sets her availability: **7:00 PM – 9:00 PM today**
3. She selects her activity: **"Drinks"**

**5:32 PM — Discovery**
4. Priya starts swiping through profiles filtered by "Drinks" activity
5. Each profile shows the person's availability time slot (may or may not overlap with hers)
6. She swipes left on 10 profiles that don't interest her

**5:35 PM — Finding a Match**
7. On the 11th profile, she sees **Rahul**—a nice-looking guy whose bio resonates with her
8. Rahul's availability is **9:00 PM – 11:00 PM** (different from her slot)
9. Despite the time mismatch, she's interested—she swipes right
10. Popup appears: *"Your intro has been sent to Rahul"*

**5:36 PM — Chat Begins**
11. Priya opens the chat with Rahul
12. She sees Rahul's **auto-generated intro** already displayed (no waiting for first message)
13. Priya taps a quick reply: **"Are you up for meeting today?"**
14. Rahul responds with quick reply: **"Yes, but where do you want to meet?"**

**5:38 PM — Venue Discussion**
15. Now they discuss where to meet
16. Priya types: "How about Toit in Indiranagar?"
17. Rahul replies: "Perfect, see you at 8:30?"
18. They negotiate a time that works for both (between their availability windows)

**5:40 PM — Quick Alignment Call**
19. Priya wants to verify Rahul's vibe before meeting
20. She taps **"Request Call"** (voice)
21. Rahul receives the request and taps **"Accept"**
22. They have a quick 5-minute call
23. Priya feels confident and confirms the plan on the call

**8:30 PM — Activity Together**
24. Priya and Rahul meet for drinks 🍻

---

**Key Observations from This Journey:**
- Total time from login to confirmed plan: ~15 minutes
- Quick replies accelerated the early conversation; manual typing used for venue specifics
- Time slot mismatch didn't prevent matching—they negotiated in chat
- Quick Alignment call provided confidence before meeting in person
- The "activity" (drinks) provided natural context for the meeting

---

*Document maintained by FAST Product Team*
