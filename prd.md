# FAST — Instant Dating (India)
## Product Requirements Document

**Version:** 2.0
**Last Updated:** January 2026
**Product Owner:** FAST Product Team
**Status:** Draft — Extended with Viral Growth & Distribution Strategy

---

## Table of Contents
1. [Executive Summary](#1-executive-summary)
2. [Problem Statement](#2-problem-statement)
3. [Target Users & Personas](#3-target-users--personas)
4. [Product Goals & Success Metrics](#4-product-goals--success-metrics)
5. [Viral Growth & Distribution Strategy](#5-viral-growth--distribution-strategy)
6. [Launch Playbook](#6-launch-playbook)
7. [Notification Strategy](#7-notification-strategy)
8. [Core Features & User Flows](#8-core-features--user-flows)
9. [Functional Requirements](#9-functional-requirements)
10. [Design System & Brand Guidelines](#10-design-system--brand-guidelines)
11. [Appendix](#11-appendix)

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

#### Persona 1: Clarity-Seeking Gen-Z
| Attribute | Details |
|-----------|---------|
| **Demographics** | 20–25 years old, college student or early career |
| **Lifestyle** | Digital-native, scroll-heavy, values authenticity over polish |
| **Needs** | Upfront intentions, no games, clear signals |
| **Motivation** | Skip the guesswork—know what the other person wants before investing time |
| **Traits** | Direct, values honesty, dislikes vague "let's see where this goes" energy |
| **Frustration** | *"Just tell me what you're looking for. I hate wasting time decoding mixed signals."* |
| **Why FAST works** | Activity-first matching removes ambiguity—both people know why they're meeting |

#### Persona 2: Transparency-First Gen-Z
| Attribute | Details |
|-----------|---------|
| **Demographics** | 22–26 years old, working professional or postgraduate |
| **Lifestyle** | Career-focused but socially active, prefers quality interactions over quantity |
| **Needs** | Real profiles, verified intentions, no catfishing |
| **Motivation** | Meet genuine people without the performance theater |
| **Traits** | Skeptical of curated personas, values realness, quick to spot inauthenticity |
| **Frustration** | *"Everyone's profile is a highlight reel. I want to know who they actually are."* |
| **Why FAST works** | Quick Alignment calls verify the person; auto-generated bios reduce fake personas |

#### Persona 3: Time-Starved Professional
| Attribute | Details |
|-----------|---------|
| **Demographics** | 26–32 years old, working professional (tech, consulting, finance, etc.) |
| **Lifestyle** | Long work hours, limited personal time, structured routines |
| **Needs** | Efficient filtering, fast scheduling, minimal back-and-forth |
| **Motivation** | Date without sacrificing productivity or mental bandwidth |
| **Traits** | Decisive, values efficiency, outcome-oriented |
| **Frustration** | *"I have 2 hours free this week. I can't spend them on small talk that goes nowhere."* |
| **Why FAST works** | Availability slots + activity matching = meetings happen fast, not conversations |

#### Persona 4: Burned-Out Professional
| Attribute | Details |
|-----------|---------|
| **Demographics** | 28–35 years old, mid-career professional |
| **Lifestyle** | Mentally drained from work, values low-effort social interactions |
| **Needs** | Low-pressure meeting formats, no obligation to "perform" |
| **Motivation** | Meet someone without adding to decision fatigue |
| **Traits** | Selective with energy, prefers structured interactions, avoids high-stakes situations |
| **Frustration** | *"Dating apps feel like another job. I don't have the mental energy to be 'on' all the time."* |
| **Why FAST works** | Quick replies reduce effort; activity-focus removes the "interview" pressure |

---

## 4. Product Goals & Success Metrics

### 4.1 Primary Goals
1. Reduce time from match to first activity together
2. Increase meeting conversion rate (matches that become real-world activities)
3. Decrease ghosting rate through shared activity purpose
4. Create a low-pressure, activity-focused meeting experience
5. Reduce catfishing through quick alignment (video/voice verification)

### 4.2 Key Performance Indicators (KPIs)

#### Core Product Metrics
| Metric | Description | Target |
|--------|-------------|--------|
| Match-to-Activity Conversion | % of matches that result in scheduled activities | >15% |
| Time-to-Meeting | Average hours from match to confirmed activity | <24 hours |
| Quick Alignment Usage | % of users who do video/voice call before meeting | >40% |
| Activity Completion Rate | % of scheduled activities that actually happen | >70% |
| User Retention (D7/D30) | Users returning after 7 and 30 days | D7: >40%, D30: >20% |
| Completion Rate | % of users completing full onboarding | >80% |

#### Growth & Viral Metrics
| Metric | Description | Target |
|--------|-------------|--------|
| K-Factor | Viral coefficient (invites sent × conversion rate) | >0.5 |
| Invites per User | Average referral invites sent per active user | >2 |
| Invite Conversion Rate | % of invites that result in new signups | >20% |
| Waitlist Conversion | % of waitlist users who complete signup when area launches | >60% |
| Time to First Invite | Hours from signup to first friend invitation | <48 hours |
| Network Density | Active users per neighborhood | >500 for launch |
| Share Rate | % of users who share after positive activity feedback | >15% |

#### Engagement Metrics
| Metric | Description | Target |
|--------|-------------|--------|
| DAU/MAU Ratio | Daily active users / Monthly active users | >30% |
| Swipes per Session | Average profile interactions per app open | >15 |
| Notification Open Rate | % of push notifications that drive app opens | >25% |
| Peak Time Participation | % of users active during Friday/Saturday evenings | >50% |
| Availability Set Rate | % of sessions where user sets availability | >70% |

---

## 5. Viral Growth & Distribution Strategy

### 5.1 Growth Philosophy

**The cold, hard truth:** Dating apps live or die by network density. You need enough attractive, available people in the same area at the same time, or the product is worthless. This isn't a "nice to have"—it's existential.

FAST's time-slot mechanic creates a unique constraint: we need people available at overlapping times. This means we need **10x the user density** of a typical dating app to deliver value.

**The good news:** This same constraint creates urgency and FOMO that can fuel viral growth—if we architect it correctly.

### 5.2 Viral Loop Architecture

#### Primary Viral Loop: "Tonight's Activity" Share
```
User sets availability → Sees "X people available for [activity] tonight" →
User has great meetup → Shares success → Friend downloads → Loop repeats
```

#### Secondary Viral Loop: "Activity Invite"
```
User wants to do activity → Not enough matches available →
Prompted to "Invite friends to unlock more people" →
Friend joins → Both users see expanded pool → Value delivered
```

#### Tertiary Viral Loop: "Waitlist FOMO"
```
User in waitlisted area → Sees "247 people ahead of you in Koramangala" →
User shares to unlock faster access → Friends join waitlist → Density builds before launch
```

### 5.3 K-Factor Optimization

| Metric | Target | Mechanism |
|--------|--------|-----------|
| **Invites sent per user** | 3+ | Activity invite prompts, unlock features |
| **Invite acceptance rate** | 25%+ | Pre-written messages, social proof |
| **Time to first invite** | <24 hours | Prompted after first match or activity |

### 5.4 Core Viral Features

#### Feature 1: Activity Heatmap (Social Proof Engine)
Show real-time activity to create urgency:
- "🔥 47 people available for Drinks tonight in Indiranagar"
- "☕ 23 people want Coffee this weekend in Koramangala"
- Numbers update in real-time
- **Critical:** Only show when numbers are impressive (>15 for an activity)

#### Feature 2: "Unlock More" Mechanic
When a user runs out of profiles to swipe:
- "Want to see more people available for [activity]?"
- "Invite 2 friends to unlock 20 more profiles"
- Alternative: "Share your availability to unlock"

#### Feature 3: Success Story Prompts
After a completed activity (user confirms they met):
- "How was drinks with Priya? 🍻"
- Options: "Amazing!" / "Good vibes" / "Not my type"
- If positive: "Your friends would love this. Share your experience?"
- Pre-written, privacy-safe share: "Just had a great time meeting someone new on FAST. Way better than endless texting 💬→🍻"

#### Feature 4: Neighborhood Leaderboard
- "Most active neighborhoods this week"
- Shows which areas have most activity
- Creates FOMO for users in less active areas
- Drives word-of-mouth in hot neighborhoods

#### Feature 5: "Your Friends on FAST" (Phase 2)
- Contact sync (optional, with clear privacy controls)
- "3 of your contacts are on FAST"
- Never reveal who—just the number
- Creates curiosity and normalizes usage

### 5.5 Anti-Viral Patterns to Avoid

| Pattern | Why It Kills Growth |
|---------|---------------------|
| Empty states | "No one available" destroys retention. Never show this. |
| Slow onboarding | Every extra second = 10% drop-off. Target <90 seconds to first swipe. |
| Requiring too much upfront | 4 photos is aggressive. Consider 2 required, 2 optional. |
| No immediate value | User must see appealing profiles within first session or they churn. |
| Generic sharing | "Share FAST" doesn't work. Share moments, not apps. |

### 5.6 Network Effect Multipliers

#### Density Thresholds
| User Density | User Experience |
|--------------|-----------------|
| <100 users/neighborhood | **Unusable.** User sees few/no matches. |
| 100-500 users/neighborhood | **Marginal.** Occasional matches, high churn risk. |
| 500-2000 users/neighborhood | **Good.** Regular matches, product works. |
| 2000+ users/neighborhood | **Excellent.** Real-time availability matching. |

**Strategy implication:** Launch narrow and deep. One neighborhood at 2000 users beats 10 neighborhoods at 200 users each.

---

## 6. Launch Playbook

### 6.1 Pre-Launch Phase: Build Density Before Opening

#### Waitlist Strategy
1. **Landing page** with area selection
2. **"Your area isn't live yet"** message with waitlist signup
3. **Show position in line** for their specific area
4. **Unlock faster access** by sharing/inviting friends

#### Waitlist Viral Mechanics
| Action | Reward |
|--------|--------|
| Sign up | Position #X in line |
| Share unique link | Move up 10 spots per signup |
| 3 friends join | Guaranteed early access |
| 10 friends join | VIP access + profile boost |

#### Target Density Before Launch
- Minimum 500 waitlist signups per neighborhood before going live
- Ideal: 1000+ signups with 60%+ completing pre-registration

### 6.2 Launch Sequence: City-by-City, Neighborhood-by-Neighborhood

#### Phase 1: Bangalore Pilot (Weeks 1-8)
| Week | Focus Area | Target Users |
|------|------------|--------------|
| 1-2 | Indiranagar only | 500 active |
| 3-4 | Indiranagar + Koramangala | 1500 active |
| 5-6 | Add HSR Layout | 3000 active |
| 7-8 | Full Bangalore (6 neighborhoods) | 6000 active |

#### Phase 2: Expansion (Weeks 9-16)
- Mumbai launch (same neighborhood-by-neighborhood approach)
- Delhi NCR launch
- Hyderabad launch



#### First 48 Hours
| Hour | Action |
|------|--------|
| 0 | Open access, send "You're in!" notification |
| 2 | Send "X people available tonight in [area]" |
| 24 | "Yesterday's stats: X meetups happened in [area]" |
| 48 | "This weekend: X people planning activities" |

### 6.4 Cold Start Solutions

#### Problem: New user signs up, no one is available
**Solutions:**
1. **Stagger availability display**: Show profiles with upcoming availability (next 48-72 hours), not just "right now"
2. **"Notify me" option**: "No one's available for Drinks tonight. Get notified when someone is?"
3. **Activity scheduling**: "Set your availability for later this week and we'll match you"
4. **Never show zero**: If <3 profiles available, show a friendly "More people coming soon! Invite friends to speed it up"

#### Problem: Gender imbalance (common in dating apps)
**Solutions:**
1. **Women-first access**: Give women earlier access to build the more valuable side first
2. **Activity-based framing**: Position as "activity partners" not "dating" in initial marketing
3. **Women-only referrals**: Let women earn rewards for inviting other women
4. **Quality control**: More aggressive filtering on male profiles initially

---

## 7. Notification Strategy

### 7.1 Notification Philosophy

**Rule #1:** Every notification must deliver value or create anticipation. No "engagement bait."

**Rule #2:** Notifications are the primary re-engagement mechanism. Master this or die.

**Rule #3:** Timing matters more than content. A mediocre notification at the right time beats a perfect notification at the wrong time.

### 7.2 Notification Types & Triggers

#### Tier 1: High-Priority (Always Send)
| Trigger | Notification | Timing |
|---------|--------------|--------|
| New match | "You matched with [Name]! You both want [Activity]" | Immediate |
| Message received | "[Name]: [Message preview]" | Immediate |
| Call request received | "[Name] wants to do a quick call before meeting" | Immediate |
| Match available NOW | "☕ [Name] is available for Coffee right now in [Area]" | Immediate |

#### Tier 2: Engagement (Smart Timing)
| Trigger | Notification | Timing |
|---------|--------------|--------|
| Unread matches | "You have 3 matches waiting. [Name] is available tonight" | 6 PM local |
| Popular time approaching | "🔥 Peak time for Drinks in [Area] starts in 2 hours" | 5 PM Fri/Sat |
| Activity surge | "23 people just set availability for [Activity] tonight" | Real-time when threshold hit |
| Match's availability starting | "[Name] is available starting now" | When their time slot begins |

#### Tier 3: Re-engagement (Lapsed Users)
| Trigger | Notification | Timing |
|---------|--------------|--------|
| 3 days inactive | "Miss us? 12 new people in [Area] want [Their top activity]" | 6 PM |
| 7 days inactive | "People are meeting up without you. [X] activities happened this week" | Weekend morning |
| Match went inactive | "Looks like [Name] hasn't been active. Keep swiping?" | After 48 hours |

### 7.3 Time-Slot Specific Notifications

**The killer feature of FAST:** Notifications tied to real-time availability.

| Scenario | Notification | Why It Works |
|----------|--------------|--------------|
| Match becomes available | "🟢 [Name] is available NOW for Drinks" | Creates urgency, drives immediate action |
| Availability overlap | "You and [Name] are both free 7-9 PM. Message them!" | Removes scheduling friction |
| Peak time alert | "Tonight's the night! 34 people available for activities in [Area]" | Social proof + urgency |
| Upcoming availability | "Your availability starts in 1 hour. Ready to meet someone?" | Primes the user |

### 7.4 Notification Timing Rules

| Day | Best Times | Avoid |
|-----|------------|-------|
| Mon-Thu | 12-1 PM, 6-8 PM | Before 10 AM, after 10 PM |
| Friday | 12-1 PM, 4-7 PM | After 9 PM (they're out) |
| Saturday | 11 AM-1 PM, 4-6 PM | Morning (sleeping), late night |
| Sunday | 11 AM-2 PM, 5-7 PM | Evening (prep for Monday) |

### 7.5 Notification Caps

| Type | Daily Max | Weekly Max |
|------|-----------|------------|
| Match notifications | Unlimited | Unlimited |
| Message notifications | Unlimited | Unlimited |
| Engagement notifications | 2 | 8 |
| Re-engagement notifications | 1 | 3 |

### 7.6 Push vs. In-App Notifications

| Content | Push | In-App | SMS (backup) |
|---------|------|--------|--------------|
| New match | ✓ | ✓ | - |
| New message | ✓ | ✓ | After 1 hour unread |
| Availability reminder | ✓ | ✓ | - |
| Activity surge | ✓ | ✓ | - |
| Weekly digest | - | ✓ | - |

---

## 8. Core Features & User Flows

### 8.1 User Journey Overview
```
Welcome → Login/Signup → Profile Creation → Activity & Availability Setup → Discovery → Matching → Chat → Quick Alignment (optional) → Activity Together
```

**Key principle:** The journey leads to a shared activity, not a "date." Users are meeting to do something together, which removes pressure and creates natural conversation.

### 8.2 Authentication Flow

#### Welcome Screen
- Display FAST branding with login and signup options
- Clean, minimal interface with neon-dark theme

#### Phone Authentication
- Phone number input → "Send OTP" button
- OTP verification screen
- **Prototype behavior:** Auto-fill dummy OTP to proceed

### 8.3 Profile Creation (Onboarding)

#### Step 1: Basic Information
- **Name:** Text input
- **Age:** Modern control (slider, segmented control, or picker sheet—not old-school steppers)

#### Step 2: Photos
- "Add Photos" opens a **dedicated photo management page**
- User must add **4 photos**
- Return to main profile flow after completion

#### Step 3: Bio Builder (No Manual Typing)
- "Create Bio" opens a **dedicated page** with ~22 quick questions
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
| Height | Under 5'0" / 5'0"–5'4" / 5'5"–5'8" / 5'9"–6'0" / Over 6'0" |
| Food preferences | Vegetarian / Non-vegetarian / Vegan / Eggetarian / Jain |
| Working style | 9-to-5 grinder / Startup hustle / Freelance / Flexible hours / Night owl |
| Ideal trip | Mountains / Beach / City exploration / Road trip / Staycation |
| Ideal life | Fast-paced city / Slow countryside / Travel nomad / Suburban balance / Haven't figured it out |
| Cooking | Love cooking / Survival mode / Ordering expert / Learning / Hate it |
| Friend circle | Tight-knit few / Large social circle / Mix of both / Mostly solo / Making new friends |
| Family oriented | Very close to family / Independent but connected / Figuring it out / Not really |
| Kids | Love kids / Maybe someday / Not for me / Haven't thought about it |
| Movie preferences | Mainstream blockbusters / Indie films / Documentaries / Foreign cinema / All of the above |
| Neurodivergent | ADHD / OCD / Anxiety / On the spectrum / Prefer not to say / None |
| Therapy | Currently in therapy / Have been before / Open to it / Not my thing / Prefer not to say |

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

### 8.4 Discovery & Matching

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

### 8.5 Matches Screen

#### Display Requirements
- Show **name** prominently
- Show **shared activity** (e.g., "Both want: Pottery, Coffee")
- Show **availability as time range** (e.g., "6–8 PM", "7–9 PM")
- Shared activity + availability slot are the key decision factors for who to message first

### 8.6 Chat Screen

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

### 8.7 Time & Calendar

#### Availability Selection
- Remove "now" from time slot options
- Calendar picker for **next 7 days**
- Time ranges (not single times)

### 8.8 Time-Based Urgency & FOMO Mechanics

These features leverage FAST's unique time-slot mechanic to create urgency and drive action.

#### Expiring Availability Windows
- When a user's availability window is ending: "⏰ [Name]'s availability ends in 30 minutes"
- Creates urgency to message/meet before the window closes
- Match cards show countdown for users available "right now"

#### "Available Now" Priority
- Profiles of users currently in their availability window get **priority placement**
- Visual indicator: Pulsing green dot + "Available now until 9 PM"
- These profiles appear first in discovery feed

#### "Tonight's Last Call"
- At 8 PM: Show banner "Last chance for tonight! 12 people still available"
- Creates end-of-day urgency for users who haven't made plans
- Tap to see profiles available for remainder of evening

#### Activity Countdown
- When viewing a profile: "Both available for Drinks in 2 hours"
- Shows how soon the overlap window begins
- Creates anticipation and prompts early messaging

#### "Peak Time" Alerts
- Friday/Saturday 5-7 PM: "🔥 Peak time starting! 47 people setting availability now"
- Push notification drives users to set their own availability
- In-app banner shows real-time counter

#### Missed Opportunity Nudges
- If user was matched but didn't message, and the match's availability passed:
- "You missed [Name]'s availability window. They're available again Saturday"
- Creates regret and drives faster action on future matches

#### Weekly FOMO Summary
- Sunday evening: "This week on FAST: 234 activities happened in Indiranagar"
- Shows what user missed by not being active
- "Set your availability for next week?"

### 8.9 Viral Feature Screens

#### 8.9.1 Waitlist Screen (Pre-Launch)
**Entry Point:** New user in unlaunched area

**Screen Elements:**
- "FAST is coming to [Area]"
- Your position: "#247 in line"
- "Share to move up"
- Pre-written share message with unique referral link
- Progress bar showing how close area is to launch
- "Get early access: Invite 3 friends"

**Actions:**
- Share to WhatsApp/Instagram/Twitter
- Copy referral link
- See friends who've joined

#### 8.9.2 Activity Heatmap Screen
**Entry Point:** Discovery screen header tap or dedicated tab

**Screen Elements:**
- Map view of current city/area
- Heat overlay showing activity concentration
- List view toggle:
  - "🔥 Drinks — 47 people tonight"
  - "☕ Coffee — 23 people this weekend"
  - "🎨 Pottery — 8 people this week"
- Tap activity → Filter discovery to that activity

**Social Proof Elements:**
- Real-time counter updates
- "12 new people joined in last hour"
- Trending activity badge

#### 8.9.3 "Unlock More" Modal
**Trigger:** User runs out of profiles to swipe

**Screen Elements:**
- "Want to see more people for [Activity]?"
- "Invite 2 friends to unlock 20 more profiles"
- Friend invite buttons (WhatsApp, SMS, Copy Link)
- Alternative: "Share your availability to unlock"
- Skip option (subtle)

**Psychology:** Creates investment through referral, not frustration through paywall



#### 8.9.5 Neighborhood Leaderboard Screen
**Entry Point:** Profile tab or weekly notification

**Screen Elements:**
- "Most active neighborhoods this week"
- Ranked list:
  - "🥇 Indiranagar — 156 activities"
  - "🥈 Koramangala — 134 activities"
  - "🥉 HSR Layout — 98 activities"
- User's neighborhood highlighted
- "Your area: #4 — Help it climb! Set your availability"


---

## 9. Functional Requirements

### 9.1 Authentication
| ID | Requirement | Priority |
|----|-------------|----------|
| AUTH-01 | Support phone number + OTP login | P0 |
| AUTH-02 | Support both new signup and returning user login | P0 |
| AUTH-03 | Prototype: Auto-fill dummy OTP for testing | P0 |

### 9.2 Profile Management
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

### 9.3 Discovery
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

### 9.4 Matching & Chat
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

### 9.5 Calendar & Scheduling
| ID | Requirement | Priority |
|----|-------------|----------|
| CAL-01 | 7-day calendar picker for availability | P0 |
| CAL-02 | Time range selection (not single times) | P0 |
| CAL-03 | No "now" option in time slots | P0 |

### 9.6 Growth & Viral Features
| ID | Requirement | Priority |
|----|-------------|----------|
| GROW-01 | Waitlist system with position tracking | P0 |
| GROW-02 | Referral link generation (unique per user) | P0 |
| GROW-03 | "Move up the waitlist" mechanic via referrals | P0 |
| GROW-04 | Activity heatmap showing real-time user counts by activity | P0 |
| GROW-05 | "Unlock More" modal when swiping pool exhausted | P0 |
| GROW-06 | Post-activity feedback collection | P0 |
| GROW-07 | Shareable success story cards (privacy-safe) | P1 |
| GROW-08 | Neighborhood leaderboard | P1 |
| GROW-09 | User stats and badges system | P1 |
| GROW-10 | "Your Friends on FAST" contact sync (Phase 2) | P2 |
| GROW-11 | Pre-written share messages for WhatsApp/Instagram | P0 |
| GROW-12 | Early access rewards for referrers | P0 |

### 9.7 Urgency & FOMO
| ID | Requirement | Priority |
|----|-------------|----------|
| URG-01 | Expiring availability countdown on match cards | P0 |
| URG-02 | "Available Now" priority placement with pulsing indicator | P0 |
| URG-03 | "Tonight's Last Call" banner at 8 PM | P1 |
| URG-04 | Activity countdown showing time until overlap window | P1 |
| URG-05 | "Peak Time" alerts on Friday/Saturday evenings | P0 |
| URG-06 | Missed opportunity nudges for expired availability windows | P1 |
| URG-07 | Weekly FOMO summary notification | P1 |
| URG-08 | Real-time activity surge counters | P0 |

### 9.8 Notifications
| ID | Requirement | Priority |
|----|-------------|----------|
| NOTIF-01 | Push notification for new matches | P0 |
| NOTIF-02 | Push notification for new messages | P0 |
| NOTIF-03 | Push notification for call requests | P0 |
| NOTIF-04 | "Match available NOW" real-time notification | P0 |
| NOTIF-05 | Unread matches reminder (6 PM timing) | P1 |
| NOTIF-06 | Peak time approaching notification | P1 |
| NOTIF-07 | Activity surge notification (threshold: 15+ users) | P1 |
| NOTIF-08 | Match's availability starting notification | P0 |
| NOTIF-09 | Re-engagement notifications (3-day, 7-day inactive) | P1 |
| NOTIF-10 | Smart notification timing based on day of week | P1 |
| NOTIF-11 | Notification caps (daily/weekly limits per type) | P0 |
| NOTIF-12 | SMS fallback for unread messages (1 hour delay) | P2 |

### 9.9 Launch & Waitlist
| ID | Requirement | Priority |
|----|-------------|----------|
| LAUNCH-01 | Area-based waitlist with position display | P0 |
| LAUNCH-02 | Progress bar showing area's progress to launch | P0 |
| LAUNCH-03 | "Launch Night" simultaneous access release | P0 |
| LAUNCH-04 | Founding Member badge for early adopters | P1 |
| LAUNCH-05 | Women-first access queue | P0 |
| LAUNCH-06 | Neighborhood density tracking (500 minimum threshold) | P0 |
| LAUNCH-07 | "Area not live" fallback screen with waitlist CTA | P0 |

---

## 10. Design System & Brand Guidelines

### 10.1 Brand Identity

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

### 10.2 Color Palette

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

### 10.3 Typography

| Element | Size | Weight | Line Height |
|---------|------|--------|-------------|
| Display/H1 | 28–32px | Semibold | 130% |
| H2 | 20–22px | Semibold | 130% |
| Body | 15–16px | Regular | 150% |
| Caption/Meta | 12–13px | Medium | 140% |

### 10.4 Layout & Spacing

**Grid:** 8pt grid throughout

| Element | Specification |
|---------|---------------|
| Screen padding | 16px left/right |
| Section spacing | 24px between major blocks |
| Component spacing | 12–16px between related elements |
| Safe top padding | 16–24px (device dependent) |

### 10.5 Component Specifications

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

## 11. Appendix

### 11.1 Glossary
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
| Activity Heatmap | Real-time display showing user counts per activity, creating social proof and urgency |
| K-Factor | Viral coefficient measuring how many new users each existing user brings |
| Network Density | Number of active users per neighborhood; critical threshold for product value |
| Waitlist Mechanic | Pre-launch system that builds user density before opening an area |
| FOMO (Fear of Missing Out) | Psychological driver used in urgency features to prompt action |
| Launch Night | Coordinated release event where all waitlisted users get access simultaneously |
| Unlock More | Referral-gated feature that reveals additional profiles after friend invites |

### 11.2 Out of Scope (v1.0)
- Payment/subscription features
- Real location services (prototype uses hardcoded Bangalore areas)
- Real OTP verification
- Backend matching algorithm
- Profile verification
- Contact sync ("Your Friends on FAST")

### 11.3 Future Considerations
- Expand to other Tier 1 cities (Mumbai, Delhi NCR, Hyderabad)
- Add women-focused safety features
- Implement premium tiers
- Add group date features
- Integrate with calendar apps
- Contact sync for social proof ("3 friends on FAST")
- Cross-city matching for travelers
- Activity venue partnerships
- In-app activity booking

### 11.4 Sample User Journey

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
