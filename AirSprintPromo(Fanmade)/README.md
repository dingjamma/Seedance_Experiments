# AirSprint Promo — Seedance 2.0 Experiment

A cinematic luxury promo video experiment for **AirSprint Private Aviation** using Seedance 2.0 / 即梦AI. Built entirely from AirSprint's publicly available assets. No internal data, no proprietary content.

> "Their most viewed YouTube video is scripted and terrible. Let's see if AI can do better."

---

## 🎯 Concept

A 15–18 second cinematic promo cut from 4 individually generated Seedance clips, stitched together in post. Inspired by NetJets and VistaJet-style luxury aviation advertising.

**Narrative arc:**
1. 🌙 Night tarmac — power and prestige at rest
2. ✈️ Daytime climb — freedom, departure, blue sky
3. 🛋️ Cabin interior — comfort, luxury, the experience
4. 🌅 Family arrival — emotion, warmth, the reason you fly

---

## 🖼️ Reference Images

| Slot | File | Description |
|------|------|-------------|
| @1 | `reference1.jpg` | Daytime flight — white & navy aircraft climbing, clear blue sky |
| @2 | `reference2.jpg` | Night tarmac — aircraft parked, dramatic ground lighting |
| @3 | `reference3.jpg` | Cabin interior wide — full seat layout, bright windows |
| @4 | `reference4.jpg` | Cabin interior detail — seating close-up, laptop, window light |
| @5 | `reference5.jpg` | Family arrival — tropical sunset, family walking off plane |

---

## 📁 Prompt Files

| File | Clip | Status |
|------|------|--------|
| `prompt_clip1_tarmac.md` | Night tarmac push-in | 🔄 Generating |
| `prompt_clip2_climb.md` | Daytime sky climb | 🔄 Generating |
| `prompt_clip3_cabin.md` | Cabin interior reveal | 🔄 Generating |
| `prompt_clip4_arrival.md` | Family golden hour arrival | 🔄 Generating |

---

## 🎬 Prompting Strategy — English Breakdown

Unlike the Frieza vs Illidan experiment, this project has **zero content moderation concerns** — private jets, families, and luxury travel are completely clean. This means prompts can be fully explicit with no bypass tricks needed.

### Why the prompts are structured this way

**1. One clip per scene, not one clip for everything**
Seedance degrades fast when you ask for multiple scene transitions in a single generation. Splitting into 4 separate clips — each with one clear visual objective — gives the model the best chance of producing something usable. The "editing" happens in post, not inside the AI.

**2. Camera movement is described as a physical action**
Rather than "cinematic shot," every prompt specifies exactly what the camera does: "slow low-angle push from tail to nose," "parallel tracking shot from left 45°," "dolly in from rear center of cabin." This anchors the model to real cinematography behavior from its training data rather than letting it freestyle something random.

**3. Lighting described in layers**
Each clip has explicit light source instructions — direction, color temperature, and what surface it hits. Night tarmac: hard ground uplights + cold engine glow. Cabin: warm ceiling strip + cold window natural light. Golden hour arrival: warm backlight rim + soft frontal fill. Layered lighting descriptions push the model toward professional-looking results instead of flat, even illumination.

**4. Emotion is a technical instruction**
The family arrival prompt explicitly states: "gentle camera movement, not action film pace, relaxed and joyful tone." Video models respond to mood language — it influences pacing, color grading tendencies, and motion speed even without explicit frame rate instructions.

**5. Negative constraints on every clip**
Every prompt ends with what NOT to do: no people (clips 1-3), no distortion, no motion blur, no flickering, no overexposure. These aren't guarantees but they shift the probability distribution away from the most common failure modes.

**6. Aircraft livery locked via reference + text**
The white and navy blue color scheme is described in text on every clip AND locked via the reference image slot. Double-specifying the livery reduces drift between clips, so when you cut them together the aircraft looks like the same plane throughout.

---

## ✂️ Post-Production Plan

Cut order in CapCut / DaVinci Resolve (free):

```
Clip 1 (night tarmac, 4-5s)
  → cross dissolve 0.5s
Clip 2 (blue sky climb, 3-4s)
  → cross dissolve 0.5s
Clip 3 (cabin reveal, 4-5s)
  → cross dissolve 0.5s
Clip 4 (family arrival, 4-5s)
```

**Music:** Ambient luxury — no lyrics, soft orchestral or piano + light percussion. Search "luxury aviation background music" on Pixabay or Epidemic Sound for royalty-free options.

**Optional text overlays:**
- Clip 2 end: *"Your time. Your schedule."*
- Clip 4 end: *"AirSprint Private Aviation"*

---

## 📊 Results Log

| Clip | Prompt | Result | Notes |
|------|--------|--------|-------|
| 1 — Night tarmac | v1 | 🔄 Pending | — |
| 2 — Daytime climb | v1 | 🔄 Pending | — |
| 3 — Cabin reveal | v1 | 🔄 Pending | — |
| 4 — Family arrival | v1 | 🔄 Pending | — |

---

## 💡 Tips & Lessons Learned

- No moderation issues on this project — describe everything explicitly, no bypass needed
- Submit reference images in exact @1→@5 slot order every time
- Cabin interior clips tend to be the most stable — low motion, controlled lighting
- The family/people clip (Clip 4) is highest risk for limb distortion — may need multiple retries
- If aircraft livery drifts between clips, add more explicit color description in text (`白色机鼻，深海军蓝机身，白色竖线分界`) 

---

*All assets sourced from AirSprint's public website and marketing materials. This is a personal AI experimentation project, not affiliated with or endorsed by AirSprint Private Aviation.*
