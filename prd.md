# FAST — Instant Dating (India)
## Product Requirements Document

**Version:** 1.0
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
FAST is a dating app designed for **India's "instant" culture**—quick commerce, reels, low attention spans. Instead of endless chatting, it makes **intent + availability + activity + expectations** visible upfront, so people can move from match → meeting with minimal friction.

### 1.2 Core Value Proposition
**"Less talking, more meeting (without the awkwardness)."**

FAST is especially helpful for:
- **Busy professionals** who lack time for endless back-and-forth
- **Introverts** who struggle with performative chat dynamics

### 1.3 Key Differentiators
| Traditional Dating Apps | FAST |
|------------------------|------|
| Endless chatting before meeting | Intent-first, availability-led discovery |
| Manual bio writing | Auto-generated introductions from quick questions |
| Ambiguous scheduling | Clear time slots visible on profiles |
| Ghosting cycles | Structured, low-pressure interactions |

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
| **Intent confusion** | Unclear what the other person is looking for |
| **Time wastage** | Investment in chats that lead nowhere |

### 2.2 How FAST Solves These Problems
| Solution | Implementation |
|----------|----------------|
| **Intent-first** | Users declare what they're looking for upfront |
| **Clear expectations** | Bill preferences, activity types visible on profile |
| **Auto introductions & quick replies** | No typing required to start conversations |
| **Small talk made easy** | Pre-built conversation starters and quick responses |
| **Time-based matching** | Availability slots shown prominently |
| **Availability-led discovery** | Match with people free at the same time |
| **Introvert-friendly flow** | Structured interactions reduce social anxiety |
| **Quick alignment** | See compatibility before investing time |

---

## 3. Target Users & Personas

### 3.1 Primary Market
Urban India (Tier 1 cities), starting with Bangalore

### 3.2 Jobs To Be Done
> "Help me quickly find a compatible match and set up a low-effort meeting time without awkward planning or endless chatting."

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
1. Reduce time from match to first meeting
2. Increase meeting conversion rate (matches that become dates)
3. Decrease ghosting rate through structured interactions
4. Create an introvert-friendly dating experience

### 4.2 Key Performance Indicators (KPIs)
| Metric | Description |
|--------|-------------|
| Match-to-Date Conversion | % of matches that result in scheduled meetings |
| Time-to-Meeting | Average hours from match to confirmed date |
| User Retention (D7/D30) | Users returning after 7 and 30 days |
| Chat Engagement | Messages sent per match |
| Completion Rate | % of users completing full onboarding |

---

## 5. Core Features & User Flows

### 5.1 User Journey Overview
```
Welcome → Login/Signup → Profile Creation → Preferences → Discovery → Matching → Chat → Date
```

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

#### Step 5: Pre-Meeting Preferences
- Options include: 5-minute voice call / 5-minute video call

#### Step 6: Activity Selection
- Coffee, Movie, Drinks, Dinner, Comedy show, Walk, Museum, Live music, Board games, Dessert, Mental health talk, Books/cafe, Fitness date

#### Step 7: Area Selection
- User types area name
- **Bottom sheet** displays:
  - Typed area + distance from current location (e.g., "Indiranagar — 2 km")
  - 3 nearby area suggestions (e.g., Indiranagar, Koramangala, HSR)
- Use Bangalore areas only for prototype

#### Onboarding Completion
- Full-screen success message: *"We wish you the best for your date today. Let the search begin."*
- Modern illustration/animation in neon-dark theme

### 5.4 Discovery & Matching

#### Profile Cards
- Generate **100+ fake profiles** with varied:
  - Availability times
  - Interests
  - Activity preferences
  - Personality answers
- Each profile displays **4 photos**
- **Photo navigation:** Tap to advance to next photo (Tinder-style)

#### Interaction Model
- **Like button** and **Unlike button** (thumbs/tick/cross style)
- **Unlike animation:** Card flies left (trash-like motion)
- **Like animation:** Card flies right with golden glow accent
- After like: Show popup *"Send your intro to {Name}"* for 5 seconds
- **Match popup:** Display for 1 out of every 3 likes
- Do NOT auto-navigate to chat after like

### 5.5 Matches Screen

#### Display Requirements
- Show **name** prominently
- Show **availability as time range** (e.g., "6–8 PM", "7–9 PM")
- Availability slot is the key decision factor

### 5.6 Chat Screen

#### Header
- Display: **Name, Age, Availability slot**
- Profile photo tap → Opens full profile

#### Quick Actions
- "Send introduction" as a **chat quick-action chip**
- Sends the **auto-generated intro** from Bio Builder
- Mix with other tappable quick message options

#### Communication Options
- Voice call button
- Video call button
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
| PROF-05 | Pre-meeting preference selection | P1 |
| PROF-06 | Activity type selection (13 options) | P0 |
| PROF-07 | Area selection with location-aware suggestions | P0 |

### 6.3 Discovery
| ID | Requirement | Priority |
|----|-------------|----------|
| DISC-01 | Generate 100+ fake profiles for prototype | P0 |
| DISC-02 | Profile cards with 4 photos, tap-to-navigate | P0 |
| DISC-03 | Like/Unlike buttons (not swipe) | P0 |
| DISC-04 | Card animations (left for unlike, right+glow for like) | P1 |
| DISC-05 | "Send intro" popup after like (5 seconds) | P0 |
| DISC-06 | Match popup for 1 in 3 likes | P0 |

### 6.4 Matching & Chat
| ID | Requirement | Priority |
|----|-------------|----------|
| CHAT-01 | Match list showing name + availability range | P0 |
| CHAT-02 | Chat header with name, age, availability | P0 |
| CHAT-03 | Quick-action chips including "Send introduction" | P0 |
| CHAT-04 | Voice and video call buttons | P1 |
| CHAT-05 | On-screen keyboard UI | P2 |

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
| Availability-led discovery | Matching algorithm that prioritizes users with overlapping free time |
| Bio Builder | Feature that generates user bios from quick questionnaire responses |
| Intent-first | Design philosophy where users declare dating intentions upfront |
| Journey mapping | Visual breakdown of user's end-to-end experience (steps, thoughts, emotions, pain points, opportunities) |

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

---

*Document maintained by FAST Product Team*
