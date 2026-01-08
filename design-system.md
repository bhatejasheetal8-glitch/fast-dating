# FAST Design System & Screen Specifications
## A Brian Chesky-Inspired Design Review

**Version:** 1.0
**Last Updated:** January 2026
**Design Philosophy:** Obsessive craft, emotional journeys, trust-first

---

## Part 1: Design Philosophy

### The Fundamental Human Truth

Before we design a single screen, we must understand the human truth we're solving for:

> **People don't hate dating. They hate the performance theater of dating.**

Traditional dating apps create anxiety because every interaction feels like an audition. FAST's genius insight is reframing the entire experience around *doing things together*—not evaluating each other.

This isn't a feature. It's the soul of the product.

### The 11-Star Experience Framework

**What does each star level look like for FAST?**

| Star | Experience |
|------|------------|
| **1-star** | You download the app. It's confusing. You delete it. |
| **3-star** | You set up a profile. You see some people. Nothing happens. |
| **5-star** | You match with someone. You meet for coffee. It's fine. |
| **7-star** | You match with someone who shares your exact vibe. The conversation flows. You meet within 24 hours. Great time. |
| **10-star** | The app feels like a thoughtful friend. It shows you someone perfect for pottery tonight. You meet, laugh for 3 hours, and plan to meet again. |
| **11-star** | You open the app, and it already knows you need a low-key evening. It suggests a specific person, a specific activity, a specific venue. You show up—they're already there, smiling. The pottery class has your name on a reserved wheel. You leave thinking "how did this app know?" |

**Our job:** Build toward 10-star. Let 11-star be the north star.

### Three Non-Negotiable Principles

**1. Every screen earns the next tap.**
Users should *want* to continue, not feel obligated. If any screen feels like homework, we've failed.

**2. Trust is built in micro-moments.**
Every detail either builds or erodes trust. Profile photos that feel real. Copy that sounds human. Transitions that feel responsive. Trust compounds.

**3. The activity is the hero, not the date.**
Every visual, every word should reinforce: "You're here to do something fun with someone new." Not: "You're here to find a partner."

---

## Part 2: The Emotional Journey Map

### The User's Emotional Arc

```
HOPE → CURIOSITY → MOMENTUM → ANTICIPATION → CONNECTION → DELIGHT
```

Each phase has specific emotional needs:

| Phase | Emotion | Design Goal |
|-------|---------|-------------|
| **Download** | Hope + Skepticism | "This feels different" |
| **Onboarding** | Curiosity + Impatience | "This is quick and actually fun" |
| **First Swipe** | Momentum | "I want to keep going" |
| **First Match** | Anticipation | "This could actually happen" |
| **First Chat** | Nervous Energy | "This feels natural, not forced" |
| **First Activity** | Connection | "I'm glad I did this" |
| **Post-Activity** | Delight + Gratitude | "I want to tell someone about this" |

---

## Part 3: Screen-by-Screen Design Specifications

### 3.1 Welcome & Onboarding

#### Screen 1: Welcome Screen

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│         [FAST Logo]             │
│      with subtle neon glow      │
│                                 │
│                                 │
│    "Less talking.               │
│     More meeting."              │
│                                 │
│                                 │
│    [Illustration: Two people    │
│     at pottery wheel, laughing] │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Get Started          │  │
│  └───────────────────────────┘  │
│                                 │
│      Already have account?      │
│           Log in                │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Logo should have the *lightest* possible glow—like a neon sign seen from a block away
- Illustration style: Loose, hand-drawn feeling. Not corporate. Not overly polished.
- The two people should be *doing the activity*, not looking at each other romantically
- "Get Started" button: Full-width, 52px height, neon background with 8% glow
- "Log in" is understated—text link, muted color

**Copy Philosophy:**
The tagline "Less talking. More meeting." does the heavy lifting. It's not about *finding* someone—it's about *doing* something with someone. This distinction matters.

---

#### Screen 2: Phone Number Entry

**Layout:**
```
┌─────────────────────────────────┐
│  ←                              │
│                                 │
│     What's your number?         │
│                                 │
│     We'll text you a code.      │
│     No spam, ever.              │
│                                 │
│  ┌───────────────────────────┐  │
│  │ +91 │ 98765 43210         │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Send Code            │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
│    By continuing, you agree     │
│    to our Terms & Privacy       │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Large, clear input field with +91 prefix pre-selected
- Input field gets neon focus ring (2px, 20% glow)
- "No spam, ever." is the trust-builder. Small text, big promise.
- Button remains muted until valid number entered, then transitions to full neon
- Back arrow is 24px, muted color, generous tap target (44px)

**Micro-interaction:**
When user starts typing, the heading subtly shifts up to make room for the keyboard. No jarring jumps.

---

#### Screen 3: OTP Verification

**Layout:**
```
┌─────────────────────────────────┐
│  ←                              │
│                                 │
│     Enter the code              │
│                                 │
│     Sent to +91 98765 43210     │
│                                 │
│     ┌───┐ ┌───┐ ┌───┐ ┌───┐    │
│     │ 4 │ │ 2 │ │ 0 │ │ _ │    │
│     └───┘ └───┘ └───┘ └───┘    │
│                                 │
│                                 │
│     Resend code in 0:24         │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
│       [Numeric Keyboard]        │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- 4 individual boxes, 56px each, 12px gap
- Each box fills with slight scale animation (1.0 → 1.05 → 1.0)
- Current box has neon border, others have muted border
- Auto-advance to next box on entry
- Auto-submit when 4th digit entered
- "Resend code" is muted text, becomes tappable link at 0:00

**Success State:**
All boxes get green checkmark overlay, brief haptic, then auto-navigate to next screen.

---

#### Screen 4: Name Entry

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    1 of 7    │
│                                 │
│     What should we              │
│     call you?                   │
│                                 │
│     This is how you'll appear   │
│     to others.                  │
│                                 │
│  ┌───────────────────────────┐  │
│  │ Priya                     │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Continue             │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Progress indicator "1 of 7" is subtle, top-right, muted color
- NOT a progress bar—progress bars create anxiety. Simple fraction is calmer.
- Input field: 52px height, left-aligned text, 18px font
- Placeholder text: "Your first name" in muted color
- Explanation text is conversational, not formal

**Important:** No last name required. First name only. Less friction, more privacy.

---

#### Screen 5: Age Selection

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    2 of 7    │
│                                 │
│     How old are you?            │
│                                 │
│     We'll show you people       │
│     in a similar age range.     │
│                                 │
│                                 │
│         ┌─────────────┐         │
│         │             │         │
│         │     26      │         │
│         │             │         │
│         └─────────────┘         │
│                                 │
│    ─────────●───────────────    │
│    18                      40   │
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Continue             │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Large, centered age display (48px font, bold)
- Horizontal slider below with neon thumb
- Slider track: muted color, filled portion in neon
- Slider has subtle haptic feedback at each year
- Min 18, Max adjustable (default 40)
- Age display updates in real-time as slider moves

**Why slider, not picker:**
Sliders feel playful. Pickers feel like forms. We want this to feel light.

---

#### Screen 6: Photo Upload

**Layout (Empty State):**
```
┌─────────────────────────────────┐
│  ←                    3 of 7    │
│                                 │
│     Show yourself               │
│                                 │
│     Add 4 photos. Real ones.    │
│     No sunglasses. No groups.   │
│                                 │
│  ┌─────────┐  ┌─────────┐       │
│  │         │  │         │       │
│  │    +    │  │    +    │       │
│  │         │  │         │       │
│  │  Main   │  │         │       │
│  └─────────┘  └─────────┘       │
│                                 │
│  ┌─────────┐  ┌─────────┐       │
│  │         │  │         │       │
│  │    +    │  │    +    │       │
│  │         │  │         │       │
│  │         │  │         │       │
│  └─────────┘  └─────────┘       │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Continue (0/4)       │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- 2x2 grid, each cell ~160px square
- First cell labeled "Main"—this is the primary photo
- Empty cells have dashed neon border, + icon centered
- Tap opens photo picker (camera roll priority)
- Continue button shows progress (0/4, 1/4, etc.)
- Button disabled until 4 photos added

**Filled State:**
- Photos fill cells edge-to-edge with 18px radius
- Small X button appears on tap (top-right corner)
- Drag to reorder enabled
- First photo has subtle "Main" badge

**Photo Guidelines Tooltip:**
On first tap of any cell, show brief tooltip:
"Tips for great photos: Clear face, good lighting, just you"

---

#### Screen 7: Intro Information

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    4 of 7    │
│                                 │
│     Tell us about yourself      │
│                                 │
│     This gets shared when       │
│     you match.                  │
│                                 │
│  Height                         │
│  ┌───────────────────────────┐  │
│  │ 5'7"                      │  │
│  └───────────────────────────┘  │
│                                 │
│  Job / Study                    │
│  ┌───────────────────────────┐  │
│  │ Product Designer          │  │
│  └───────────────────────────┘  │
│                                 │
│  Personality Type (optional)    │
│  ┌───────────────────────────┐  │
│  │ INFJ / Ambivert           │  │
│  └───────────────────────────┘  │
│                                 │
│  Smoking                        │
│  ○ Non-smoker  ○ Socially  ○ Yes│
│                                 │
│  Pets                           │
│  ○ No pets  ○ Have pets  ○ Love │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Continue             │  │
│  └───────────────────────────┘  │
└─────────────────────────────────┘
```

**Design Notes:**
- Single scrollable screen with all intro fields
- Height: Dropdown picker (feet/inches or cm)
- Job/Study: Free text input, 50 char limit
- Personality: Optional, free text, 30 char limit
- Smoking: Radio buttons, single select
- Pets: Radio buttons, single select
- All fields except personality are required
- Button disabled until required fields filled

**Why This Matters:**
This factual information auto-sends when you match. It answers the basic questions ("Who is this person?") so the bio can focus on personality and vibe.

---

#### Screen 8: Bio Builder

**Layout (Question View):**
```
┌─────────────────────────────────┐
│  ←                    5 of 7    │
│                                 │
│     Now let's build your bio    │
│                                 │
│     Answer a few quick ones.    │
│     We'll write the vibe.       │
│                                 │
│     ━━━━━━━━━━○───────────      │
│     Question 3 of 12            │
│                                 │
│                                 │
│     What's your weekend vibe?   │
│                                 │
│  ┌───────────────────────────┐  │
│  │  🏠  Home reset           │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  🌳  Outdoors             │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  ☕  Cafe hopping          │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  🎉  Party                │  │
│  └───────────────────────────┘  │
│                                 │
│         Skip this one           │
└─────────────────────────────────┘
```

**Design Notes:**
- Progress bar with current position indicator
- Question in larger font (20px, semibold)
- Options as full-width cards, 56px height
- Emoji + text format for visual scanning
- Selected option gets neon border + fill at 15%
- Auto-advance 0.3s after selection
- "Skip this one" is muted text link at bottom

**Transition:**
Cards slide left, new question slides in from right. Quick, not dramatic.

**Question Flow (Priority Order):**
1. Weekend vibe
2. Coffee vs Chai
3. Pet preference
4. Social battery
5. Ideal date activity
6. Music mood
7. Food preference
8. Work style
9. Communication style
10. Fitness
11. Ideal trip
12. Movie type

**Why 12, not 22:**
Chesky principle: "If you can't onboard in 90 seconds, you've lost." 12 questions × 3 seconds = 36 seconds for bio section. Acceptable.

**The Distinction:**
- **Intro (Screen 7):** Facts. What someone needs to know. Auto-sends on match.
- **Bio (Screen 8):** Vibe. How you show up. Replaces the pick-up line.

---

#### Screen 9: Bio Preview

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    5 of 7    │
│                                 │
│     Here's your bio             │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │  Coffee over chai, always.│  │
│  │  Weekends are for cafe    │  │
│  │  hopping and discovering  │  │
│  │  new playlists. Ambivert  │  │
│  │  who recharges with close │  │
│  │  friends, not crowds.     │  │
│  │  Looking for someone to   │  │
│  │  try that new pottery     │  │
│  │  place with.              │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│         Edit answers            │
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Looks good           │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Generated bio in a card with subtle border
- Bio text: 16px, 150% line height, warm and natural tone
- "Edit answers" link to go back and change responses
- "Looks good" is the primary CTA

**Bio Generation Logic:**
- Take key answers and weave into 3-4 natural sentences
- Never use bullet points—sounds like a resume
- Always end with an activity-forward line
- Avoid "I am" statements; use active voice
- Focus on personality, preferences, and energy—not facts

---

#### Screen 10: Activity Selection

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    6 of 8    │
│                                 │
│     What do you want to do?     │
│                                 │
│     Pick activities you'd       │
│     actually do with someone.   │
│                                 │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌────┐ │
│  │ ☕  │ │ 🎬  │ │ 🍺  │ │ 🍽️ │ │
│  │Coff.│ │Movie│ │Drink│ │Dinn│ │
│  └─────┘ └─────┘ └─────┘ └────┘ │
│                                 │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌────┐ │
│  │ 🎤  │ │ 🚶  │ │ 🏛️  │ │ 🎵  │ │
│  │Comed│ │Walk │ │Museu│ │Live │ │
│  └─────┘ └─────┘ └─────┘ └────┘ │
│                                 │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌────┐ │
│  │ 🎲  │ │ 🍰  │ │ 💬  │ │ 📚  │ │
│  │Board│ │Desse│ │Talk │ │Books│ │
│  └─────┘ └─────┘ └─────┘ └────┘ │
│                                 │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌────┐ │
│  │ 💪  │ │ 🎨  │ │ 🍳  │ │ 🖼️  │ │
│  │Fitne│ │Potte│ │Cooki│ │Galle│ │
│  └─────┘ └─────┘ └─────┘ └────┘ │
│                                 │
│  ┌───────────────────────────┐  │
│  │   Continue (3 selected)   │  │
│  └───────────────────────────┘  │
└─────────────────────────────────┘
```

**Design Notes:**
- 4x4 grid of activity cards
- Each card: ~80px square, emoji + abbreviated label
- Unselected: muted border, dark background
- Selected: neon border, neon background at 15%, subtle scale (1.05)
- Tap toggles selection with satisfying haptic
- Minimum 1 activity required, no maximum
- Button shows count: "Continue (3 selected)"

**Activity Labels (Full):**
Coffee, Movie, Drinks, Dinner, Comedy show, Walk, Museum, Live music, Board games, Dessert, Mental health talk, Books/cafe, Fitness date, Pottery, Cooking class, Art gallery

---

#### Screen 11: Bill Preference

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    7 of 8    │
│                                 │
│     How do you like to          │
│     handle the bill?            │
│                                 │
│     No wrong answer here.       │
│     Just helps set expectations.│
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     ₹ ↔ ₹                 │  │
│  │     Split 50-50           │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     ₹ ⟳ ₹                 │  │
│  │     Take turns            │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     ₹ → You               │  │
│  │     My treat              │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Three large cards, each ~80px height
- Visual icon + clear label
- Single select (tap auto-advances)
- Selected card gets neon treatment
- Copy is warm: "No wrong answer here"

---

#### Screen 12: Quick Alignment Preference

**Layout:**
```
┌─────────────────────────────────┐
│  ←                    8 of 8    │
│                                 │
│     Want to vibe-check          │
│     before meeting?             │
│                                 │
│     A quick call helps you      │
│     know it's real.             │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     🎙️  Voice call         │  │
│  │     Quick 5-min chat      │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     📹  Video call         │  │
│  │     See each other first  │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     🤷  No preference      │  │
│  │     I'll go with the flow │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Same card format as bill preference
- Single select, auto-advance
- Subtext explains each option's benefit
- "No preference" is valid—not everyone needs this

---

#### Screen 13: Area Selection

**Layout:**
```
┌─────────────────────────────────┐
│  ←                              │
│                                 │
│     Where do you hang out?      │
│                                 │
│     We'll show you people       │
│     nearby.                     │
│                                 │
│  ┌───────────────────────────┐  │
│  │ 🔍  Indiranagar           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │  Indiranagar              │  │
│  │  📍 2 km away              │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  Koramangala              │  │
│  │  📍 4 km away              │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  HSR Layout               │  │
│  │  📍 6 km away              │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
│                                 │
│                                 │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Search input at top with icon
- Results appear as user types
- Each result shows area name + distance
- Tap to select → immediate navigation to next screen
- Distance is calculated from device location (or estimated)

---

#### Screen 14: Onboarding Complete

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│                                 │
│                                 │
│                                 │
│      [Illustration: Person      │
│       high-fiving, confetti,    │
│       pottery wheel in bg]      │
│                                 │
│                                 │
│     You're all set              │
│                                 │
│     Time to find someone        │
│     to do something with.       │
│                                 │
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Start exploring      │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Celebratory but not over-the-top
- Illustration should feel warm, not corporate
- Copy reinforces activity-first positioning
- Single CTA to enter the app
- Consider confetti animation on load (subtle, 1 second)

---

### 3.2 Discovery & Swiping

#### Session Setup (Discovery Header)

**Layout:**
```
┌─────────────────────────────────┐
│  🍺 Drinks    │  7-9 PM Today   │
│  ──────────────────────────────  │
│  ↓  Tap to change               │
└─────────────────────────────────┘
```

**Design Notes:**
- Persistent header on discovery screen
- Shows current activity filter + availability
- Tap either section to change
- Neon accent on the activity icon
- "Tap to change" is subtle hint for first-time users

---

#### Profile Card

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │                           │  │
│  │                           │  │
│  │      [PHOTO 1 of 4]       │  │
│  │                           │  │
│  │                           │  │
│  │   ● ○ ○ ○                 │  │
│  ├───────────────────────────┤  │
│  │                           │  │
│  │  Priya, 26                │  │
│  │  Indiranagar • 2 km       │  │
│  │                           │  │
│  │  ┌──────────────────────┐ │  │
│  │  │ 🍺 Drinks  ☕ Coffee  │ │  │
│  │  └──────────────────────┘ │  │
│  │                           │  │
│  │  🟢 Available 7-9 PM      │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│    ✗                       ♡    │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Photo takes 60% of card height
- Dot indicators for photo position (tap to advance)
- Name and age: large, bold (22px)
- Location: muted color, smaller
- Shared activities as pills with emoji
- Availability badge: green dot + time range
- Like/Unlike buttons at bottom (48px, circular)
- Unlike: muted gray, X icon
- Like: neon border, heart icon

**Card States:**
- **Default:** Full card visible, slight shadow
- **Swiping left:** Card tilts left, red tint overlay appears
- **Swiping right:** Card tilts right, neon glow appears
- **Released left:** Card flies off screen left
- **Released right:** Card flies off screen right with glow trail

---

#### Expanded Profile View

**Triggered by:** Tap on card (not swipe)

**Layout:**
```
┌─────────────────────────────────┐
│  ←                              │
│                                 │
│  ┌───────────────────────────┐  │
│  │      [PHOTO GALLERY]      │  │
│  │       ● ○ ○ ○             │  │
│  └───────────────────────────┘  │
│                                 │
│  Priya, 26                      │
│  Indiranagar • 2 km             │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  5'6" • Product Designer        │
│  Ambivert • Non-smoker          │
│  Has pets 🐕                    │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  "Coffee over chai, always.     │
│   Weekends are for cafe hopping │
│   and discovering new playlists.│
│   Looking for someone to try    │
│   that new pottery place with." │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  Wants to do:                   │
│  🍺 Drinks  ☕ Coffee  🎨 Pottery │
│                                 │
│  Available:                     │
│  🟢 Today 7-9 PM                │
│  🟢 Saturday 3-6 PM             │
│                                 │
│  Prefers:                       │
│  ₹ Split 50-50                  │
│  📹 Video call before meeting   │
│                                 │
│  ┌──────────┐    ┌──────────┐   │
│  │    ✗     │    │    ♡     │   │
│  │  Unlike  │    │   Like   │   │
│  └──────────┘    └──────────┘   │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Full-screen modal over discovery
- Scrollable content
- Photo gallery at top (swipeable)
- **Intro section** (factual): Height, job, personality type, smoking, pets - formatted as clean bullets
- Divider line separates intro from bio
- **Bio section** (vibe): In quotation marks for personality and energy
- Activities as pills
- Multiple availability slots shown
- Preferences displayed clearly
- Two-button layout at bottom (sticky)

**The Two-Part Profile:**
- **Intro:** Gets auto-sent on match. Answers "Who are you?" (facts)
- **Bio:** Shows on profile. Answers "What's your vibe?" (personality)

---

#### Match Popup

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│                                 │
│                                 │
│     [Overlapping photos:        │
│      Your photo + their photo]  │
│                                 │
│                                 │
│     It's a match!               │
│                                 │
│     You both want Drinks.       │
│     They're free 7-9 PM.        │
│                                 │
│     ✓ Intros exchanged          │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Message Priya        │  │
│  └───────────────────────────┘  │
│                                 │
│         Keep swiping            │
│                                 │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Full-screen overlay with celebration
- Photos overlap with subtle neon glow
- "It's a match!" in large font
- Shared activity + availability called out
- **"✓ Intros exchanged"** confirms both users received each other's factual info automatically
- Primary CTA: Message them
- Secondary: Keep swiping (text link)
- Consider subtle confetti animation

**What Happens on Match:**
When you match, both users automatically receive each other's intro (height, job, personality type, smoking status, pets). No action required. The chat opens with this context already shared.

---

#### "Intro Sent" Toast

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│  ┌───────────────────────────┐  │
│  │  ✓ Your intro was sent    │  │
│  │    to Priya               │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Appears at top of screen after like
- Slides down, holds 5 seconds, slides up
- Subtle neon border on left
- Checkmark icon in neon
- Tappable to dismiss

---

### 3.3 Matches Screen

**Layout:**
```
┌─────────────────────────────────┐
│            Matches              │
│  ──────────────────────────────  │
│                                 │
│  Available Now                  │
│                                 │
│  ┌─────────────────────────────┐│
│  │ [Photo] Priya               ││
│  │         🍺 Drinks           ││
│  │         🟢 Free until 9 PM  ││
│  │         "Hey! Your intro... ││
│  └─────────────────────────────┘│
│                                 │
│  This Week                      │
│                                 │
│  ┌─────────────────────────────┐│
│  │ [Photo] Rahul               ││
│  │         ☕ Coffee            ││
│  │         🕐 Sat 3-6 PM       ││
│  │         No messages yet     ││
│  └─────────────────────────────┘│
│                                 │
│  ┌─────────────────────────────┐│
│  │ [Photo] Sneha               ││
│  │         🎨 Pottery          ││
│  │         🕐 Sun 11 AM-2 PM   ││
│  │         "That pottery pla...││
│  └─────────────────────────────┘│
│                                 │
│  ──────────────────────────────  │
│                                 │
│  [Tab Bar: Explore | Matches | Profile] │
└─────────────────────────────────┘
```

**Design Notes:**
- Grouped by availability: "Available Now" vs "This Week"
- Each match card shows: photo, name, shared activity, availability, last message preview
- Green dot for "available now" matches
- Clock icon for future availability
- Tap to open chat
- Matches with unread messages: bold name, dot indicator

**Empty State:**
"No matches yet. Keep exploring—the right activity partner is out there."

---

### 3.4 Chat Screen

**Layout:**
```
┌─────────────────────────────────┐
│  ←   Priya, 26                  │
│       🍺 Drinks • 7-9 PM Today  │
│  ──────────────────────────────  │
│                                 │
│  ┌───────────────────────────┐  │
│  │  ✓ Priya's intro:         │  │
│  │  5'6" • Product Designer  │  │
│  │  Ambivert • Non-smoker    │  │
│  │  Has pets 🐕              │  │
│  └───────────────────────────┘  │
│                                 │
│          Their message          │
│    ┌─────────────────────┐      │
│    │ Hey! Love that you  │      │
│    │ picked pottery too. │      │
│    └─────────────────────┘      │
│                                 │
│                 Your message    │
│      ┌─────────────────────┐    │
│      │ Right? There's a   │    │
│      │ new place in       │    │
│      │ Indiranagar!       │    │
│      └─────────────────────┘    │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  ┌───────────────────────────┐  │
│  │ Are you up for meeting?  │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │ Yes, that time works!    │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │ Where should we meet?    │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌─────────────────────────────┐│
│  │  Type a message...    📞 📹 ││
│  └─────────────────────────────┘│
└─────────────────────────────────┘
```

**Design Notes:**
- Header: Back arrow, name/age, shared activity + availability badge
- Tap header to see full profile (where you can read their bio)
- **Their intro appears first** as auto-sent context card (gray background, checkmark icon)
- Intro shows factual information: height, job, personality type, smoking status, pets
- Message bubbles: theirs left (gray), yours right (neon at 20%)
- Quick replies appear above input field
- Quick replies scroll horizontally if > 3
- Tap quick reply → sends immediately
- Input field with placeholder + call icons
- 📞 = voice call, 📹 = video call

**Quick Reply Behavior:**
- Appear contextually based on conversation stage
- Stage 1 (no messages): "Are you up for meeting?" / "Tell me more about..."
- Stage 2 (after reply): "Yes, that time works!" / "Can we do later?"
- Stage 3 (planning): "Where should we meet?" / "How about..."

**The Auto-Send Mechanism:**
On match, both users' intros (factual info) appear at the top of the chat automatically. This replaces the awkward "opening line" dance. Users can start conversations knowing basic details, and can tap the header to see the full profile (including bio) anytime.

---

#### Quick Alignment Banner

**When both users prefer a call, show:**
```
┌─────────────────────────────────┐
│  📹  You both prefer a quick   │
│      call before meeting        │
│              [Schedule Call]    │
└─────────────────────────────────┘
```

**Design Notes:**
- Appears below header, above messages
- Dismissible (x button, subtle)
- "Schedule Call" is tappable link
- Tap → opens call request flow

---

#### Call Request Flow

**Sender sees:**
```
┌─────────────────────────────────┐
│                                 │
│     Requesting video call       │
│     with Priya...               │
│                                 │
│     [Cancel Request]            │
│                                 │
└─────────────────────────────────┘
```

**Receiver sees (in-chat notification):**
```
┌─────────────────────────────────┐
│                                 │
│  ┌───────────────────────────┐  │
│  │  📹  Priya wants to       │  │
│  │      video call           │  │
│  │                           │  │
│  │  [Decline]  [Accept]      │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

---

### 3.5 Profile & Settings

**Layout:**
```
┌─────────────────────────────────┐
│           Your Profile          │
│  ──────────────────────────────  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │      [Your Photo]         │  │
│  │                           │  │
│  │      Tushar, 28           │  │
│  │      Indiranagar          │  │
│  │                           │  │
│  │      [Edit Profile]       │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  Your Activities                │
│  ☕ Coffee  🍺 Drinks  🎨 Pottery │
│  [Edit]                         │
│                                 │
│  Your Availability              │
│  Today: 7-9 PM                  │
│  This week: Sat 3-6 PM          │
│  [Set Availability]             │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  Settings                       │
│  Distance preference    15 km > │
│  Bill preference    Split 50-50>│
│  Call preference    Video call >│
│  Notifications              On >│
│                                 │
│  ──────────────────────────────  │
│                                 │
│  Help & Support                 │
│  Log Out                        │
│                                 │
└─────────────────────────────────┘
```

---

### 3.6 Viral & Growth Screens

#### Waitlist Screen

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│        [FAST Logo]              │
│                                 │
│     FAST is coming to           │
│     Jayanagar                   │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │   You're #247 in line     │  │
│  │                           │  │
│  │   ━━━━━━━━━━━━━━━○─────   │  │
│  │   412 / 500 to launch     │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│     Share to move up faster     │
│                                 │
│  ┌───────────────────────────┐  │
│  │  📲  Share on WhatsApp    │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  📷  Share on Instagram   │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │  🔗  Copy Link            │  │
│  └───────────────────────────┘  │
│                                 │
│     Get 3 friends to join       │
│     = Guaranteed early access   │
│                                 │
│  ──────────────────────────────  │
│     0 friends joined so far     │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Position in line is prominent
- Progress bar shows area's progress to 500 threshold
- Share buttons are large, easy to tap
- Incentive is clear: 3 friends = early access
- Friend counter creates game mechanic

---

#### Activity Heatmap

**Layout:**
```
┌─────────────────────────────────┐
│  ←    What's happening          │
│  ──────────────────────────────  │
│                                 │
│  Tonight in Indiranagar         │
│                                 │
│  ┌───────────────────────────┐  │
│  │ 🍺  Drinks                │  │
│  │ 🔥 47 people available    │  │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━  │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │ ☕  Coffee                 │  │
│  │    23 people available    │  │
│  │ ━━━━━━━━━━━━━━━           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │ 🎬  Movie                 │  │
│  │    12 people available    │  │
│  │ ━━━━━━━━                  │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │ 🎨  Pottery               │  │
│  │    8 people available     │  │
│  │ ━━━━━                     │  │
│  └───────────────────────────┘  │
│                                 │
│     +4 more activities          │
│                                 │
│  ──────────────────────────────  │
│     🔄 Updated just now         │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Activity cards with count + visual bar
- Fire emoji for highest activity (social proof)
- Tap any card → filters discovery to that activity
- Real-time update indicator at bottom
- Numbers should feel dynamic (subtle animation on load)

---

#### "Unlock More" Modal

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │   You've seen everyone    │  │
│  │   available for Drinks    │  │
│  │   tonight                 │  │
│  │                           │  │
│  │   Invite friends to       │  │
│  │   unlock more people      │  │
│  │                           │  │
│  │  ┌─────────────────────┐  │  │
│  │  │ 📲 Invite 2 friends │  │  │
│  │  │    = 20 more        │  │  │
│  │  │    profiles         │  │  │
│  │  └─────────────────────┘  │  │
│  │                           │  │
│  │       Maybe later         │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│                                 │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Modal overlay with card
- Clear value proposition: 2 invites = 20 profiles
- Primary CTA is invite
- "Maybe later" is understated but accessible
- NOT a paywall—investment is social, not monetary

---

#### Post-Activity Feedback

**Layout:**
```
┌─────────────────────────────────┐
│                                 │
│     How was drinks with         │
│     Priya? 🍺                   │
│                                 │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     😊  Amazing!          │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     🙂  Good vibes        │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     😐  Meh               │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │     👎  Not great         │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│         Skip                    │
│                                 │
└─────────────────────────────────┘
```

**If positive (Amazing/Good vibes), follow with:**

```
┌─────────────────────────────────┐
│                                 │
│     That's great to hear!       │
│                                 │
│     Want to share the love?     │
│     Your friends might want     │
│     this too.                   │
│                                 │
│  ┌───────────────────────────┐  │
│  │                           │  │
│  │  "Just met someone great  │  │
│  │   on FAST. Way better     │  │
│  │   than endless texting."  │  │
│  │                           │  │
│  │      [Share ↗]            │  │
│  │                           │  │
│  └───────────────────────────┘  │
│                                 │
│         Not now                 │
│                                 │
└─────────────────────────────────┘
```

---

### 3.7 Urgency & FOMO Elements

#### "Available Now" Badge

```
┌────────────────────┐
│ 🟢 Free until 9 PM │
└────────────────────┘
```
- Pulsing green dot
- Appears on profile cards + matches list
- Creates urgency

---

#### Expiring Availability Warning

```
┌─────────────────────────────────┐
│  ⏰  Priya's availability ends  │
│      in 28 minutes              │
└─────────────────────────────────┘
```
- Appears in chat when time is running low
- Yellow/orange warning color
- Creates urgency to make plans

---

#### Tonight's Last Call Banner

```
┌─────────────────────────────────┐
│  🌙  Last call for tonight!    │
│      14 people still available │
│              [See who →]        │
└─────────────────────────────────┘
```
- Appears on discovery screen at 8 PM
- Tappable to see remaining profiles
- Creates end-of-day urgency

---

#### Peak Time Alert (Push Notification)

```
🔥 Peak time in Indiranagar!
52 people just set availability for tonight.
Set yours? →
```

---

## Part 4: Interaction Patterns

### 4.1 Swipe Gestures

| Gesture | Threshold | Effect |
|---------|-----------|--------|
| Swipe right | >100px horizontal | Like + send intro |
| Swipe left | >100px horizontal | Unlike |
| Tap | Anywhere on card | Expand profile |
| Swipe down | >50px vertical | Dismiss expanded view |

### 4.2 Haptic Feedback

| Action | Haptic Type |
|--------|-------------|
| Like | Medium impact |
| Unlike | Light impact |
| Match | Heavy impact + double pulse |
| Send message | Light impact |
| Quick reply tap | Selection tick |
| Age slider move | Light tick per year |
| Activity toggle | Selection tick |

### 4.3 Transitions

| Transition | Animation | Duration |
|------------|-----------|----------|
| Screen to screen | Slide left/right | 300ms |
| Modal open | Slide up + fade | 250ms |
| Modal close | Slide down + fade | 200ms |
| Card swipe | Physics-based throw | Velocity-dependent |
| Toast appear | Slide down | 200ms |
| Toast dismiss | Slide up | 150ms |

---

## Part 5: Trust & Safety Design

### 5.1 Verification Indicators

**Quick Alignment Call Badge:**
After completing a video call, show on profile:
```
✓ Video verified
```

### 5.2 Report Flow

Accessible from profile view or chat:
```
┌─────────────────────────────────┐
│     Report Priya                │
│  ──────────────────────────────  │
│                                 │
│  What's wrong?                  │
│                                 │
│  ○ Fake profile                 │
│  ○ Inappropriate messages       │
│  ○ Didn't show up               │
│  ○ Made me uncomfortable        │
│  ○ Other                        │
│                                 │
│  ──────────────────────────────  │
│                                 │
│  [Block & Report]               │
│                                 │
│        Cancel                   │
│                                 │
└─────────────────────────────────┘
```

### 5.3 Safety During Activities

In chat, after plans are confirmed:
```
┌─────────────────────────────────┐
│  📍  Meeting at Toit, 8:30 PM  │
│                                 │
│  Safety tips:                   │
│  • Meet in a public place       │
│  • Tell a friend where you're   │
│    going                        │
│  • Trust your instincts         │
│                                 │
│         [Got it]                │
└─────────────────────────────────┘
```

---

## Part 6: Empty States

### No Matches Yet

```
┌─────────────────────────────────┐
│                                 │
│     [Illustration: Two          │
│      empty coffee cups]         │
│                                 │
│     No matches yet              │
│                                 │
│     Keep swiping—your           │
│     activity partner is         │
│     out there.                  │
│                                 │
│     [Start Exploring]           │
│                                 │
└─────────────────────────────────┘
```

### No More Profiles in Area

```
┌─────────────────────────────────┐
│                                 │
│     [Illustration: Empty        │
│      bar stools]                │
│                                 │
│     You've seen everyone        │
│     for Drinks tonight          │
│                                 │
│     Try a different activity    │
│     or check back later.        │
│                                 │
│     [Try Coffee instead]        │
│     [Invite friends]            │
│                                 │
└─────────────────────────────────┘
```

### No One Available Now

```
┌─────────────────────────────────┐
│                                 │
│     [Illustration: Clock        │
│      with coffee cup]           │
│                                 │
│     No one's free right now     │
│                                 │
│     12 people are available     │
│     for Coffee this weekend.    │
│                                 │
│     [Show me]                   │
│     [Notify me when someone is] │
│                                 │
└─────────────────────────────────┘
```

---

## Part 7: Accessibility Considerations

### 7.1 Color Contrast

| Element | Contrast Ratio | Pass |
|---------|---------------|------|
| Body text on dark | 12.5:1 | AAA |
| Muted text on dark | 5.2:1 | AA |
| Neon on dark | 7.8:1 | AAA |

### 7.2 Touch Targets

- All interactive elements: minimum 44px × 44px
- Buttons: 48-52px height
- Cards: Full width, minimum 80px height

### 7.3 Motion Sensitivity

- Respect "Reduce Motion" system setting
- When enabled:
  - Replace slide transitions with fades
  - Disable swipe animations
  - Remove confetti effects
  - Use static indicators instead of pulsing

### 7.4 Screen Reader Labels

Every interactive element must have:
- Descriptive label (e.g., "Like profile" not just "Heart icon")
- State information (e.g., "Selected" for chosen activity)
- Helpful hints (e.g., "Swipe right to like, left to pass")

---

## Part 8: Performance Targets

| Metric | Target |
|--------|--------|
| Time to first paint | <1.5s |
| Time to interactive | <3s |
| Profile card render | <100ms |
| Image lazy load threshold | 2 cards ahead |
| Animation frame rate | 60fps |
| Touch response latency | <100ms |

---

## Appendix: Component Library

### A.1 Buttons

```
Primary:    [████████████████] - Neon fill, dark text
Secondary:  [────────────────] - Neon border, neon text
Tertiary:   [  Text link  ]   - Neon text, no border
Disabled:   [░░░░░░░░░░░░░░░░] - 40% opacity
```

### A.2 Input Fields

```
Default:    ┌────────────────────┐
            │ Placeholder...     │
            └────────────────────┘

Focused:    ╔════════════════════╗  (neon border)
            ║ User input         ║
            ╚════════════════════╝

Error:      ╔════════════════════╗  (red border)
            ║ Invalid input      ║
            ╚════════════════════╝
            Error message below
```

### A.3 Cards

```
Profile Card:   ┌──────────────────┐
                │                  │
                │  18-24px radius  │
                │  16-20px padding │
                │  Surface color   │
                │                  │
                └──────────────────┘

Selection Card: ┌──────────────────┐
(Selected)      │  ✓               │  (neon border)
                │  Option text     │
                └──────────────────┘
```

### A.4 Pills/Tags

```
Activity:   [🍺 Drinks]   - Emoji + text, rounded, small
Status:     [🟢 Free now] - Dot + text, rounded, small
Match:      [Both want ☕] - Text, neon background at 20%
```

---

*This design system is a living document. Every decision should be questioned against the 11-star experience: Does this help someone meet someone new through a shared activity? If not, reconsider.*
