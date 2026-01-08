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

## Part 2: Mobile App Foundation

### 2.1 Navigation Architecture

**The Three-Tab Structure:**

```
┌─────────────────────────────────┐
│     [Screen Content]            │
│                                 │
│                                 │
│                                 │
│                                 │
├─────────────────────────────────┤
│  🔍      💬        👤          │
│ Explore  Matches  Profile       │
└─────────────────────────────────┘
```

**Tab Bar Specifications:**
- Height: 80px (includes safe area)
- Background: Dark surface with subtle top border
- Active tab: Neon icon + neon text
- Inactive tab: Muted gray icon + text
- Icons: 24px, outlined style when inactive, filled when active
- Tab labels: 11px, medium weight
- Badge on Matches tab when unread messages
- Haptic feedback on tab switch

**Tab Behavior:**
- Tap active tab scrolls to top
- Switching tabs saves scroll position
- Tab bar hidden when keyboard is visible
- Tab bar persists across all main screens

---

### 2.2 Status Bar

**iOS:**
- Light content (white text/icons on dark bg)
- Height: 44px on standard devices, 59px on notched devices
- Status bar area uses app background color
- No custom status bar content—let system handle time, battery, signal

**Android:**
- Light content
- Height: 24dp
- Status bar color matches app background
- Edge-to-edge content with proper window insets

---

### 2.3 Header Patterns

#### Pattern A: Standard Navigation Header
```
┌─────────────────────────────────┐
│ ←    Screen Title            ︙ │
└─────────────────────────────────┘
```
- Height: 56px
- Left: Back button (44px tap target)
- Center: Screen title (18px, semibold)
- Right: Context menu (optional)
- Sticky: Stays at top while scrolling

#### Pattern B: Large Title Header (iOS-style)
```
┌─────────────────────────────────┐
│ ←                              ︙│
│                                 │
│ Screen Title                    │
│                                 │
└─────────────────────────────────┘
```
- Height: 96px (collapses to 56px on scroll)
- Title: 32px bold, fades and shrinks on scroll
- Smooth collapse animation with content
- Used on: Profile, Matches, Discovery

#### Pattern C: Contextual Header (Discovery)
```
┌─────────────────────────────────┐
│  🍺 Drinks  │  7-9 PM Today   ⚙️│
└─────────────────────────────────┘
```
- Height: 56px
- Shows current filter state
- Tappable sections to modify
- Settings icon on right
- Sticky at top

#### Pattern D: Modal Header
```
┌─────────────────────────────────┐
│        ╍╍╍╍╍╍                   │
│                                 │
│  ←    Modal Title          Done │
└─────────────────────────────────┘
```
- Handle bar: 36px width, 5px height, centered
- Height: 56px
- Left: Cancel/Back
- Right: Done/Save
- Title: 18px, semibold, centered

---

### 2.4 Loading States

#### Skeleton Screens
Instead of spinners, show content placeholders:

```
┌─────────────────────────────────┐
│  ┌───────────────────────────┐  │
│  │▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓│  │
│  │▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓│  │
│  │▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓│  │
│  ├───────────────────────────┤  │
│  │                           │  │
│  │ ▓▓▓▓▓▓▓  ▓▓               │  │
│  │ ▓▓▓▓▓▓▓▓▓▓▓▓              │  │
│  └───────────────────────────┘  │
└─────────────────────────────────┘
```

**Skeleton Guidelines:**
- Use for profile cards, matches list, chat history
- Shimmer animation: subtle left-to-right gradient sweep
- Match exact dimensions of real content
- Duration: 0.8s per shimmer cycle
- Background: Surface color at 30% opacity
- Never show skeleton + spinner together

#### Inline Loaders
For actions within existing content:

```
[  Sending...  ⊙  ]  - Small spinner next to text
```

- 16px spinner, neon color
- Always paired with action text
- Replaces button content during action

#### Full-Screen Loader
Only for critical operations (login, initial load):

```
┌─────────────────────────────────┐
│                                 │
│                                 │
│          [FAST Logo]            │
│                                 │
│            ⊙                    │
│       Setting things up         │
│                                 │
│                                 │
└─────────────────────────────────┘
```

---

### 2.5 Error States

#### Inline Error
```
┌─────────────────────────────────┐
│  ┌───────────────────────────┐  │
│  │ ⚠ Couldn't load profiles  │  │
│  │   [Tap to retry]          │  │
│  └───────────────────────────┘  │
└─────────────────────────────────┘
```

#### Full-Screen Error
```
┌─────────────────────────────────┐
│                                 │
│     [Illustration: Broken       │
│      coffee cup]                │
│                                 │
│     Something went wrong        │
│                                 │
│     We couldn't load this.      │
│     Check your connection.      │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Try again            │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

#### Network Error Toast
```
┌─────────────────────────────────┐
│  ⚠  No internet connection      │
└─────────────────────────────────┘
```
- Appears at top, persists until connection restored
- Yellow/orange background
- Dismissible but reappears if still offline

---

### 2.6 Bottom Sheets

**Usage:** Contextual actions, filters, selections

```
┌─────────────────────────────────┐
│        ╍╍╍╍╍╍                   │
│                                 │
│     Filter by activity          │
│                                 │
│  ○ Drinks                       │
│  ○ Coffee                       │
│  ○ Dinner                       │
│  ○ Pottery                      │
│                                 │
│  ┌───────────────────────────┐  │
│  │      Apply                │  │
│  └───────────────────────────┘  │
│                                 │
└─────────────────────────────────┘
```

**Behavior:**
- Slides up from bottom
- Handle bar at top (36px × 5px)
- Drag down to dismiss
- Tap outside to dismiss
- Background dimmed at 60%
- Supports 3 sizes: Compact (40%), Medium (60%), Large (90%)
- Smooth spring animation (0.35s)

---

### 2.7 Pull to Refresh

**Discovery & Matches screens:**

```
┌─────────────────────────────────┐
│            ↻                    │  ← Pull indicator
│       Pull to refresh           │
│                                 │
│  [Content begins...]            │
└─────────────────────────────────┘
```

**States:**
1. **Idle**: Hidden
2. **Pulling**: Circular indicator rotates with pull distance
3. **Ready**: Haptic tick, indicator fully visible
4. **Refreshing**: Animated spinner, content stays in place
5. **Done**: Success checkmark (0.3s), then fade out

**Threshold**: 80px pull distance to trigger

---

### 2.8 Action Sheets

**Usage:** Destructive actions, profile options

```
┌─────────────────────────────────┐
│                                 │
│  ╍╍╍╍╍╍                         │
│                                 │
│  Report this profile            │
│  Block this user                │
│  ────────────────────           │
│  Cancel                         │
│                                 │
└─────────────────────────────────┘
```

**Specifications:**
- Slides up from bottom
- Destructive actions in red
- Cancel button separated by divider
- Tappable backdrop to dismiss
- Haptic feedback on selection

---

### 2.9 Safe Area Handling

**Notched Devices (iPhone X+):**
```
┌───────────[notch]──────────────┐
│ ← Safe area begins (59px)      │
│                                 │
│     [Content area]              │
│                                 │
│     [Tab bar 80px]              │
└─────────────────────────────────┘
         ▔▔▔▔▔ (34px)  ← Home indicator
```

**Critical Rules:**
- Never place interactive elements in top notch area
- Bottom tab bar includes 34px bottom padding on notched devices
- Modal sheets account for home indicator
- Full-screen images can bleed into safe area
- Text/buttons stay within safe area

---

### 2.10 Keyboard Behavior

**Input Fields:**
```
┌─────────────────────────────────┐
│  Message input field            │
│  ┌───────────────────────────┐  │
│  │ Type message...           │  │
│  └───────────────────────────┘  │
├─────────────────────────────────┤
│     [System Keyboard]           │
└─────────────────────────────────┘
```

**Behavior:**
- Content scrolls up when keyboard appears
- Input field sticks above keyboard
- Tab bar hides when keyboard visible
- Dismiss keyboard: tap outside, swipe down, or send
- "Done" button on keyboard for single-line inputs
- Return key label changes contextually: "Send", "Done", "Next"

---

### 2.11 Toast Notifications

**Success:**
```
┌─────────────────────────────────┐
│  ✓ Message sent                 │
└─────────────────────────────────┘
```

**Info:**
```
┌─────────────────────────────────┐
│  ℹ Your profile was updated     │
└─────────────────────────────────┘
```

**Warning:**
```
┌─────────────────────────────────┐
│  ⚠ Check your connection        │
└─────────────────────────────────┘
```

**Specifications:**
- Appears from top (below status bar)
- Auto-dismiss after 3s
- Swipe up to dismiss early
- Max width: Screen width - 32px
- Corner radius: 12px
- Padding: 16px
- Icon + text, left-aligned
- Drop shadow for elevation

---

### 2.12 Badge Indicators

**Tab Bar Badge:**
```
│  💬        │
│ Matches  3 │  ← Red badge
```

**Profile Photo Badge:**
```
┌─────────┐
│ [Photo] │ 🟢  ← Online/Available indicator
└─────────┘
```

**Badge Specs:**
- Minimum size: 20px × 20px
- Background: Neon or red (depending on type)
- Text: White, 11px, bold
- Max two digits shown (99+)
- Positioned top-right with -4px offset

---

### 2.13 Haptic Feedback Map

| Action | Haptic Type | When |
|--------|-------------|------|
| Like swipe | Medium impact | At swipe threshold |
| Unlike swipe | Light impact | At swipe threshold |
| Match | Heavy impact + 2 ticks | On match popup |
| Send message | Light impact | On send |
| Tab switch | Selection | On tap |
| Pull-to-refresh ready | Selection | At threshold |
| Toggle activity | Selection | On tap |
| Age slider | Light tick | Per year |
| Photo advance | Light impact | Per swipe |
| Error | Notification | On error toast |
| Success | Success | On success toast |

---

## Part 3: The Emotional Journey Map

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

## Part 4: Screen-by-Screen Design Specifications

### 4.1 Welcome & Onboarding

#### Screen 1: Welcome Screen

**Layout:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│                                 │
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
│                                 │
│  ┌───────────────────────────┐  │
│  │      Get Started          │  │
│  └───────────────────────────┘  │
│                                 │
│      Already have account?      │
│           Log in                │
│                                 │
└─────────────────────────────────┘
           ▔▔▔▔▔  ← Home indicator
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
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│  ←                              │ ← Header (56px)
├─────────────────────────────────┤
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
           ▔▔▔▔▔
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
│    🔄 Regenerate  •  Edit answers│
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
- "🔄 Regenerate" link generates a new bio variation with same answers
- "Edit answers" link to go back and change responses
- Both links are muted color, separated by bullet point
- "Looks good" is the primary CTA

**Regenerate Behavior:**
- Tap "🔄 Regenerate" to get a new bio variation without changing answers
- Brief loading animation (0.5s) while generating
- New bio smoothly fades in to replace old one
- Users can regenerate unlimited times until they find a version they love
- Each regeneration uses the same answer data but varies phrasing, order, and tone

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
│         Skip this step          │
│                                 │
└─────────────────────────────────┘
```

**Design Notes:**
- Three large cards, each ~80px height
- Visual icon + clear label
- Single select (tap auto-advances)
- Selected card gets neon treatment
- Copy is warm: "No wrong answer here"
- **"Skip this step"** is muted text link at bottom
- Tapping skip advances to next screen without setting preference
- Skipped preference won't be displayed on user's profile

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

### 4.2 Discovery & Swiping

#### Discovery Screen with Full Mobile Chrome

**Layout:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│  🍺 Drinks  │  7-9 PM Today   ⚙️│ ← Contextual header
├─────────────────────────────────┤
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
├─────────────────────────────────┤
│  🔍         💬  2      👤       │ ← Tab bar with badge
│ Explore     Matches   Profile   │
└─────────────────────────────────┘
           ▔▔▔▔▔
```

**Contextual Header Notes:**
- 56px height, sticky at top
- Left section: 🍺 Drinks (tappable - opens activity selector bottom sheet)
- Right section: 7-9 PM Today (tappable - opens availability selector bottom sheet)
- Settings icon far right (opens preferences)
- Neon accent on active filter
- Divider between sections

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

### 4.3 Matches Screen

**Layout:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│ ←                              ︙│ ← Large title header
│                                 │
│ Matches                         │
│                                 │
├─────────────────────────────────┤ ← Collapses on scroll
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
├─────────────────────────────────┤
│  🔍         💬  2      👤       │ ← Tab bar
│ Explore     Matches   Profile   │
└─────────────────────────────────┘
           ▔▔▔▔▔
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

### 4.4 Chat Screen

**Layout:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│  ←   Priya, 26                 ︙│ ← Header (tappable)
│       🍺 Drinks • 7-9 PM Today  │
├─────────────────────────────────┤
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
│  ┌───────────────────────────┐  │ ← Quick replies
│  │ Are you up for meeting?  │  │
│  └───────────────────────────┘  │
│  ┌───────────────────────────┐  │
│  │ Yes, that time works!    │  │
│  └───────────────────────────┘  │
│                                 │
├─────────────────────────────────┤
│  Type a message...      📞  📹  │ ← Input bar (sticky)
└─────────────────────────────────┘
           ▔▔▔▔▔
```

**With Keyboard Open:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│  ←   Priya, 26                 ︙│ ← Header
│       🍺 Drinks • 7-9 PM Today  │
├─────────────────────────────────┤
│  [Scrollable message area]      │
│                                 │
│      ┌─────────────────────┐    │
│      │ Right? There's a   │    │
│      │ new place in       │    │
│      │ Indiranagar!       │    │
│      └─────────────────────┘    │
│                                 │
├─────────────────────────────────┤
│  Should we meet there?   📞  📹 │ ← Input with text
│                              ↑  │ ← Send button
├─────────────────────────────────┤
│     [System Keyboard]           │
│                                 │
│  Q W E R T Y U I O P            │
│   A S D F G H J K L             │
│    Z X C V B N M               │
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

### 4.5 Profile & Settings

**Layout:**
```
┌─────────────────────────────────┐ ← Status bar
│ 9:41        ⚡ 5G       █▌▌▌ 87% │
├─────────────────────────────────┤
│                                ︙│ ← Large title header
│                                 │
│ Your Profile                    │
│                                 │
├─────────────────────────────────┤ ← Collapses on scroll
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
├─────────────────────────────────┤
│  🔍         💬         👤       │ ← Tab bar
│ Explore     Matches   Profile   │
└─────────────────────────────────┘
           ▔▔▔▔▔
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

## Part 5: Mobile Interaction Patterns

### 5.1 Gesture Dictionary

#### Discovery Card Gestures

| Gesture | Threshold | Effect | Visual Feedback |
|---------|-----------|--------|-----------------|
| Swipe right | >100px horizontal | Like + send intro | Card tilts right, neon glow, flies off |
| Swipe left | >100px horizontal | Unlike | Card tilts left, red tint, flies off |
| Tap card | Single tap | Expand profile | Modal slides up |
| Tap photo area | While expanded | Advance photo | Crossfade + dot indicator |
| Swipe down | >80px vertical | Dismiss expanded view | Modal slides down |

#### Chat Gestures

| Gesture | Effect |
|---------|--------|
| Long press message | Copy / Delete options |
| Tap input field | Show keyboard + quick replies |
| Tap outside keyboard | Dismiss keyboard |
| Swipe down on messages | Pull to load earlier messages |

#### General Navigation

| Gesture | Effect |
|---------|--------|
| Swipe from left edge | Go back (iOS) |
| Swipe down on modal | Dismiss modal |
| Tap active tab | Scroll to top |
| Pull down to refresh | Reload content (Discovery, Matches) |
| Long press tab | Haptic + quick action menu |

---

### 5.2 Haptic Feedback Choreography

**Why Haptics Matter:**
Haptics turn a visual app into a *felt* experience. Done right, they create emotional punctuation—moments of delight that compound trust.

| Action | Haptic Type | Timing | Why |
|--------|-------------|--------|-----|
| Like swipe | Medium impact | At 100px threshold | Confirms action committed |
| Unlike swipe | Light impact | At 100px threshold | Subtle acknowledgment |
| Match | Heavy impact + 2 ticks | On popup appear | Celebration moment |
| Send message | Light impact | On send | Satisfying completion |
| Quick reply tap | Selection | On tap | Button press feel |
| Tab switch | Selection | On tap | Navigation confirmation |
| Pull-to-refresh ready | Selection | At 80px threshold | "Ready to release" signal |
| Activity toggle | Selection | On tap | Toggle confirmation |
| Age slider | Light tick | Per year increment | Physical dial feeling |
| Photo advance | Light impact | On swipe | Page turn feel |
| Error | Notification | On error toast | Alert attention |
| Success | Success | On success toast | Positive reinforcement |
| Long press begins | Medium impact | After 0.5s | Context menu ready |
| Bottom sheet snap | Light impact | On snap point | Physical drawer feel |

**Haptic Philosophy:**
- Reward positive actions with satisfying feedback
- Keep error haptics distinct but not jarring
- Match haptic intensity to action importance
- Never use haptics for passive events (scrolling, viewing)

---

### 5.3 Animation Timing & Easing

**The Physics of Trust:**
Animations shouldn't feel like animations—they should feel like physics. Real objects have weight and momentum.

| Transition | Animation Curve | Duration | Why |
|------------|----------------|----------|-----|
| Screen push | Ease-in-out | 300ms | Natural page flip |
| Modal appear | Spring (0.8, 0.6) | ~350ms | Bouncy entrance |
| Modal dismiss | Ease-in | 200ms | Quick exit |
| Card swipe | Velocity-based decay | Variable | Realistic throw |
| Bottom sheet | Spring (0.9, 0.8) | ~300ms | Drawer feel |
| Toast appear | Ease-out | 200ms | Gentle entry |
| Toast dismiss | Ease-in | 150ms | Quick exit |
| Tab switch | Ease-in-out | 250ms | Smooth transition |
| Button press | Ease-out | 100ms | Snappy response |
| Skeleton shimmer | Linear | 800ms loop | Smooth sweep |
| Like/unlike overlay | Ease-out | 200ms | Quick flash |
| Photo crossfade | Ease-in-out | 250ms | Smooth blend |
| Header collapse | Ease-out | 300ms | Smooth scroll |
| Keyboard appear | System default | ~250ms | Native feel |

**Animation Principles:**
1. **Entrances are bold, exits are quick** - Coming in should feel significant, leaving should be efficient
2. **Spring for delight** - Use spring animations for moments of celebration (match, success)
3. **Ease for efficiency** - Use ease curves for utilitarian actions (navigation, dismiss)
4. **Respect velocity** - Swipe actions should maintain user's gesture velocity
5. **Never block interaction** - Animations should never prevent the next action

---

### 5.4 Touch Target Sizing

**Finger-Friendly Minimum Sizes:**

| Element | Minimum Size | Recommended Size | Notes |
|---------|--------------|------------------|-------|
| Primary button | 44px height | 52px height | Full-width comfortable |
| Tab bar icon | 44×44px tap area | 24×24px icon inside | Spacing creates target |
| Back button | 44×44px | Entire left header zone | Easy thumb reach |
| Card action buttons | 48×48px | Circular, good spacing | Bottom of cards |
| List row | 56px height | 68px for important rows | Full-width tappable |
| Settings row | 52px height | — | With >12px between rows |
| Quick reply button | 44px height | Auto width with padding | Scrollable horizontal |
| Close/dismiss button | 44×44px | Top-right modal corner | Easy one-hand reach |
| Photo dots | 8px visible | 24×24px tap area | Invisible padding |
| Activity pills | 36px height | — | Tap to filter |
| Message bubble | 36px min height | Variable with content | Long-press enabled |

**Thumb Zone Heatmap:**
```
┌─────────────────────────────────┐
│ 🥶 Hard    🥶 Hard              │ ← Top corners: hardest to reach
│                                 │
│                                 │
│         😊 Comfortable          │ ← Center: easy
│                                 │
│                                 │
│ 🔥 Easy    🔥 Easy    🔥 Easy   │ ← Bottom: easiest (thumb natural position)
└─────────────────────────────────┘
```

**Design Implications:**
- Primary CTAs at bottom (Get Started, Continue, Send)
- Navigation at bottom (Tab bar)
- Back button large and left-aligned
- Destructive actions at top (harder to reach = less accidental)
- Quick replies near input (bottom zone)

---

### 5.5 Loading State Transitions

**The Three-Act Structure:**

**Act 1: Anticipation (0-300ms)**
- Show skeleton immediately
- No blank screens, ever
- Skeleton matches exact layout

**Act 2: Loading (300ms-2s)**
- Shimmer animation active
- User can still scroll skeleton content
- Cancel actions remain available

**Act 3: Resolution (<100ms)**
- Crossfade from skeleton to real content
- Maintain scroll position
- No jarring jumps or shifts

**Examples:**

**Discovery Loading:**
```
Frame 1 (0ms):        Frame 2 (500ms):      Frame 3 (1200ms):
┌──────────┐          ┌──────────┐          ┌──────────┐
│ ▓▓▓▓▓▓▓▓ │   →      │ ░▓▓▓▓▓▓▓ │   →      │ [Photo]  │
│ ▓▓▓▓▓▓▓▓ │          │ ▓░▓▓▓▓▓▓ │          │ Priya, 26│
│ ▓▓ ▓▓    │          │ ▓▓░▓ ▓▓  │          │ 🍺 Drinks│
└──────────┘          └──────────┘          └──────────┘
  Skeleton              Shimmering            Real content
```

**Message Sending:**
```
Tap Send → Light haptic
Message bubble appears with:
  • Slightly reduced opacity (80%)
  • Small spinner on right
  • "Sending..." below (muted)

On success (< 2s):
  • Fade to full opacity
  • Spinner → checkmark
  • "Sent" replaces text (then fades)

On failure:
  • Red outline appears
  • "⚠ Tap to retry" appears
  • Error haptic fires
```

---

### 5.6 Empty State Illustrations

**Why Illustrations Matter:**
Empty states are emotional moments—potential frustration points. Great illustrations turn "nothing here" into "something's coming."

**Style Guide:**
- Loose, hand-drawn aesthetic (matches brand)
- Single color accent (neon) + dark background
- Simple, not detailed—suggests possibility, not finality
- Objects related to activities (coffee cups, pottery, tickets)
- Never show sad faces or negative imagery

**Common Empty States:**

| Screen | Illustration | Copy | CTA |
|--------|--------------|------|-----|
| No matches | Two empty coffee cups side-by-side | "No matches yet" | "Start Exploring" |
| No messages | Chat bubble with sparkles | "Start a conversation" | "Send a message" |
| Out of profiles | Empty bar stools | "You've seen everyone" | "Try Coffee instead" or "Invite friends" |
| No availability | Clock with moon | "No one's free right now" | "Show me" or "Notify me" |
| Network error | Broken coffee cup | "Something went wrong" | "Try again" |
| Loading failed | Unplugged power cord | "Couldn't load this" | "Retry" |

---

### 5.7 Notification Patterns

**Push Notifications:**

| Trigger | Timing | Message | Action |
|---------|--------|---------|--------|
| New match | Immediate | "🎉 You matched with Priya!" | Open chat |
| New message | Immediate | "Priya: Hey! Love that you..." | Open chat |
| Peak time | 6-7 PM | "🔥 Peak time in Indiranagar! 52 people available." | Open discovery |
| Availability ending | 30 min before | "⏰ Your availability ends in 30 minutes" | Extend time |
| Match expiring | 24h after match | "Your match with Priya expires soon. Say hi?" | Open chat |
| Activity reminder | 1h before | "📍 Meeting Priya for drinks at 8 PM" | View details |

**In-App Badges:**

```
Tab Bar Badge:
│  💬  3  │  ← 3 unread messages
│ Matches │

Activity Badge:
[Photo] 🟢  ← Available now indicator

Quick Reply Badge:
┌──────────────────┐
│ New suggestion ✨ │  ← AI-generated quick reply
└──────────────────┘
```

---

## Part 6: Trust & Safety Design

### 6.1 Verification Indicators

**Quick Alignment Call Badge:**
After completing a video call, show on profile:
```
✓ Video verified
```

### 6.2 Report Flow

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

### 6.3 Safety During Activities

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

## Part 7: Empty States

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

## Part 8: Accessibility Considerations

### 8.1 Color Contrast

| Element | Contrast Ratio | Pass |
|---------|---------------|------|
| Body text on dark | 12.5:1 | AAA |
| Muted text on dark | 5.2:1 | AA |
| Neon on dark | 7.8:1 | AAA |

### 8.2 Touch Targets

- All interactive elements: minimum 44px × 44px
- Buttons: 48-52px height
- Cards: Full width, minimum 80px height

### 8.3 Motion Sensitivity

- Respect "Reduce Motion" system setting
- When enabled:
  - Replace slide transitions with fades
  - Disable swipe animations
  - Remove confetti effects
  - Use static indicators instead of pulsing

### 8.4 Screen Reader Labels

Every interactive element must have:
- Descriptive label (e.g., "Like profile" not just "Heart icon")
- State information (e.g., "Selected" for chosen activity)
- Helpful hints (e.g., "Swipe right to like, left to pass")

---

## Part 9: Performance Targets

| Metric | Target |
|--------|--------|
| Time to first paint | <1.5s |
| Time to interactive | <3s |
| Profile card render | <100ms |
| Image lazy load threshold | 2 cards ahead |
| Animation frame rate | 60fps |
| Touch response latency | <100ms |

---

## Part 10: Mobile Color System & Visual Design

### 10.1 Color Palette for Mobile

**Dark Mode Primary (Default):**
```
Background:       #0A0A0A (Pure black for OLED)
Surface:          #1A1A1A (Cards, modals)
Surface Elevated: #242424 (Active states, headers)
Border:           #2A2A2A (Dividers, card edges)
```

**Neon Accent System:**
```
Primary Neon:     #00FF9D (Main actions, selections)
Neon Glow:        rgba(0, 255, 157, 0.2) (Backgrounds, highlights)
Neon Border:      rgba(0, 255, 157, 0.4) (Active borders)
```

**Text Hierarchy:**
```
Primary Text:     #FFFFFF (Headlines, body)
Secondary Text:   #A0A0A0 (Subtitles, metadata)
Tertiary Text:    #6A6A6A (Hints, placeholders)
Disabled Text:    #404040 (Inactive elements)
```

**Semantic Colors:**
```
Success:          #00FF9D (Match, sent message)
Warning:          #FFB800 (Expiring soon, low activity)
Error:            #FF3B3B (Failed action, report)
Info:             #0099FF (Tips, notifications)
```

**Availability Indicators:**
```
Available Now:    #00FF9D (Green dot)
Later Today:      #FFB800 (Yellow dot)
This Week:        #0099FF (Blue dot)
Offline:          #404040 (Gray dot)
```

---

### 10.2 Typography for Mobile Screens

**Font Stack:**
```
Primary: -apple-system, SF Pro Display, Roboto, sans-serif
Fallback: System default
```

**Scale:**
```
Display:    32px, bold (Profile names, large titles)
Title 1:    28px, bold (Section headers)
Title 2:    24px, semibold (Card names)
Title 3:    20px, semibold (Modal headers)
Headline:   18px, semibold (Standard headers)
Body:       16px, regular (Main content, messages)
Subhead:    14px, medium (Metadata, labels)
Caption:    12px, regular (Timestamps, hints)
Micro:      11px, medium (Tab labels, badges)
```

**Line Heights:**
```
Display:    1.2 (Tight, for impact)
Headlines:  1.3 (Balanced)
Body:       1.5 (Comfortable reading)
Captions:   1.4 (Slightly tighter)
```

**Letter Spacing:**
```
Display:    -1.5% (Optical balance)
Headlines:  -1% (Slightly tight)
Body:       0% (Standard)
Captions:   0.5% (Slightly loose)
Tab labels: 2% (All caps, needs space)
```

---

### 10.3 Elevation & Shadows (Mobile)

**Why Elevation Matters on Mobile:**
Depth cues help users understand interactive hierarchy without relying solely on color.

**Elevation Levels:**

```
Level 0 (Base):
  box-shadow: none
  Use for: Background, flush content

Level 1 (Raised):
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.5)
  Use for: Cards, input fields

Level 2 (Floating):
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.6)
  Use for: Bottom sheets, action menus

Level 3 (Modal):
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.7)
  Use for: Modals, expanded profiles

Level 4 (Overlay):
  box-shadow: 0 16px 48px rgba(0, 0, 0, 0.8)
  Use for: Match popup, full-screen overlays
```

**Neon Glow (Special):**
```
box-shadow: 0 0 20px rgba(0, 255, 157, 0.3)
Use for: Like button, active states, success moments
```

---

### 10.4 Spacing System (8px Grid)

**Base Unit: 8px**

All spacing must be multiples of 8px for pixel-perfect alignment across devices.

```
4px   (0.5x):  Tight spacing (icon to text)
8px   (1x):    Compact padding (button text)
12px  (1.5x):  Small gaps (pill spacing)
16px  (2x):    Standard padding (card content)
24px  (3x):    Section spacing (between groups)
32px  (4x):    Large spacing (between major sections)
40px  (5x):    Extra large (onboarding spacing)
48px  (6x):    Major spacing (screen top/bottom)
```

**Component-Specific:**
```
Card padding:           16px all sides
List item padding:      16px horizontal, 12px vertical
Button padding:         16px horizontal, 14px vertical
Modal padding:          24px all sides
Screen edge margin:     16px (mobile), 20px (tablet)
Between cards:          12px vertical
Section dividers:       24px vertical
```

---

### 10.5 Border Radius (Rounded Corners)

**Why Rounded Corners Matter:**
Softness = approachability. Sharp corners feel corporate. Rounded feels human.

```
Small:      4px   (Pills, badges, tags)
Medium:     8px   (Buttons, inputs)
Standard:   12px  (Cards, toasts)
Large:      18px  (Profile cards, photos)
Extra:      24px  (Bottom sheets, modals)
Circular:   50%   (Avatar, action buttons, dots)
```

**Special Cases:**
```
Tab bar:             0px top corners (flush to screen edge)
Bottom sheet:        24px top corners only
Photo thumbnails:    12px
Match popup:         24px all corners
Chat bubbles:        18px (with 4px on sender corner)
```

---

### 10.6 Iconography Guidelines

**Icon Style:**
- Outlined (not filled) for inactive states
- Filled for active/selected states
- 24×24px standard size
- 2px stroke weight
- Rounded line caps
- Neon color for active, muted gray for inactive

**Icon Library:**
```
Navigation:
  🔍  Search/Explore (outlined magnifying glass)
  💬  Matches (outlined chat bubble)
  👤  Profile (outlined person)

Actions:
  ←   Back (arrow)
  ✕   Close (X)
  ✓   Confirm (checkmark)
  ♡   Like (outlined heart)
  ⚙️   Settings (gear)
  ︙   More options (vertical dots)

Communication:
  📞  Voice call
  📹  Video call
  ↑   Send message

States:
  🟢  Available (filled circle)
  ⚠   Warning (triangle)
  ⊙   Loading (circle spinner)
  ↻   Refresh (circular arrow)
```

---

### 10.7 Image Treatment

**Profile Photos:**
- Aspect ratio: 4:5 (portrait)
- Minimum resolution: 800×1000px
- Compression: High quality JPEG or WebP
- Loading: Progressive (blur-up technique)
- Fallback: Neon gradient with initials

**Photo Grid:**
```
┌─────────┬─────────┐
│         │         │
│  Main   │  Photo  │
│  Photo  │    2    │
│         │         │
├─────────┼─────────┤
│         │         │
│ Photo 3 │ Photo 4 │
│         │         │
└─────────┴─────────┘
```

**Image States:**
```
Loading:    Blur-up from 20px thumbnail
Loaded:     Sharp, full quality
Error:      Neon outline + placeholder icon
Tap:        Subtle scale (0.98) for feedback
```

---

### 10.8 Motion Design Language

**The Three Speeds:**

**Fast (100-150ms):** Immediate response
- Button press
- Toggle switch
- Checkbox
- Icon state change

**Medium (200-300ms):** Standard transition
- Screen navigation
- Modal appear/dismiss
- Toast notification
- Tab switch

**Slow (350-500ms):** Dramatic moment
- Match popup
- Bottom sheet expansion
- Profile card expand
- Celebration animation

**Animation Curves Explained:**
```
Ease-out (Fast start, slow end):
  Use for: Elements entering screen
  Feel: "Arriving with purpose, settling gently"

Ease-in (Slow start, fast end):
  Use for: Elements leaving screen
  Feel: "Departing quickly, efficiently"

Ease-in-out (Slow both ends):
  Use for: Elements moving on screen
  Feel: "Smooth, natural motion"

Spring (Bouncy):
  Use for: Delightful moments
  Feel: "Playful, energetic, human"
```

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

## Final Word: Building for the 11-Star Mobile Experience

This isn't just a design system—it's a commitment to craft.

Every screen, every animation, every haptic tick is an opportunity to either build or erode trust. Users won't remember your clever copy or your beautiful gradients. They'll remember how the app *felt*.

**The mobile medium demands obsession:**
- A button that's 42px instead of 44px isn't "close enough"—it's a broken promise to thumbs
- A skeleton loader isn't optional polish—it's the difference between anxiety and confidence
- A haptic tick isn't a nice-to-have—it's the punctuation that turns interaction into conversation

**Remember the human truth:**
People aren't swiping on profiles. They're swiping on possibilities. They're not chatting with matches. They're working up the courage to meet someone real.

**Every pixel matters because every pixel either:**
1. Helps someone show up to a pottery class tonight and meet someone great
2. Adds friction that keeps them home, alone, scrolling

**The standard isn't "good enough"—it's:**
- Does this feel like an iOS/Android app that Apple/Google would be proud to feature?
- Would I trust this enough to meet a stranger?
- Does this respect my time, my attention, my hope?

**This design system is a living document.**

Every decision should be questioned against the 11-star experience: *Does this help someone meet someone new through a shared activity?* If not, reconsider.

Every component should be tested against real thumbs on real devices in real lighting conditions with real network speeds.

Every interaction should feel so natural that users don't think about the app—they think about the person they're about to meet.

**Build for 10-star. Dream of 11-star.**

The details aren't the details. The details *are* the design.

Now go build something people love.

— *In the spirit of obsessive craft*
