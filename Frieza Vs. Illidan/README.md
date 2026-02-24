# Frieza vs Illidan — Seedance 2.0 / 即梦AI Experiment

A documented experiment using ByteDance's **Seedance 2.0** video generation model via the **即梦AI (Jimeng)** platform to generate a cinematic crossover battle between two iconic characters from different franchises.

---

## 🎯 Goal

Generate a 10–12 second cinematic sequence:
1. Purple alien warrior taunts (arms crossed, smirk, floating)
2. Golden transformation with energy explosion
3. Demon-winged blindfolded warrior enters with the line **"YOU ARE NOT PREPARED!"**
4. Epic light/energy duel showdown

---

## 🖼️ Reference Images

| Slot | Description | File |
|------|-------------|------|
| @1 | Purple-skin warrior — base/taunt form | `reference1.jpg` |
| @2 | Golden transformation form with aura | `reference2.jpg` |
| @3 | Blindfolded demon-wing warrior entrance | `reference3.jpg` |
| @4 | Black Temple summit / stormy background | `reference4.jpg` |

---

## 🚧 Content Moderation Issues

Platform: **即梦AI** (Jimeng, China) — paid membership tier with custom prompts + image references.

**Error received after 10+ rejections:**
```
你输入的文字不符合平台规则，请修改后重试
```

**Blocked triggers identified:**
- `Frieza` / `弗利萨`
- `Illidan` / `伊利丹`
- `Dragon Ball` / `龙珠`
- `魔兽世界` / `World of Warcraft`
- Any recognizable IP name combined with a reference image

**Bypass strategy:** Replace all IP names with generic descriptors that match the uploaded reference images contextually. The platform allows generation when character identity is implied visually rather than named explicitly.

---

## 📁 Prompt Files

| File | Status | Description |
|------|--------|-------------|
| `prompt_v1_bypass.md` | ✅ First success (rough quality) | Minimal generic descriptors, proof of concept |
| `prompt_v2_pacing.md` | 🔄 Current / Active | Fixed pacing, motion blur, HDR lighting, camera work |
| `prompt_v3_consistency.md` | 🧪 Experimental | Character fidelity focus, anti-artifact directives |

---

## 📊 Results Log

| Attempt | Prompt | Result | Notes |
|---------|--------|--------|-------|
| 1–10 | Named IP versions | ❌ Rejected | Moderation block |
| 11 | V1 generic bypass | ✅ Generated | Blurry motion, weak lighting, rushed pacing |
| Active | V2 pacing fix | 🔄 In progress | — |

---

## 🧠 Prompting Strategy — English Breakdown

### Why This Approach Works

The core insight is that Seedance 2.0 (and most video diffusion models) respond better to **concrete visual instructions** than to abstract intent. The prompts are effective for a few specific reasons:

**1. Segmented timing beats open-ended description**
Instead of saying "first this happens, then that happens," V2 explicitly stamps each beat with a timestamp (`0-2s`, `2-4s`, etc.). This forces the model to treat the clip as a structured sequence rather than a loose montage. Video models have a tendency to collapse multi-step narratives into a single moment — timestamping fights that.

**2. Camera language is load-bearing**
Phrases like "low-angle upshot," "360° orbit," "rack focus," and "single camera shake then stabilize" do two things: they anchor the model to cinematography conventions it learned from real film/anime data, and they give it a clear spatial logic for where to place elements in the frame. Without camera instructions, the model just picks something arbitrary and often inconsistent shot to shot.

**3. Motion described as light trails, not blur**
A key V2 fix: instead of saying "fast movement," the prompt says "motion trail light tail, not motion blur" (运动轨迹光尾，非模糊). This is important because video diffusion models interpret "fast movement" as temporal blur — which looks bad. Describing speed as a *visual artifact* (light trail) redirects the model toward anime-style action lines, which look intentional rather than broken.

**4. Visual descriptors as IP proxies**
The moderation bypass works because the model doesn't need the character's name to recognize them — it has the reference image. The text prompt only needs to describe what the image *shows* (purple skin, white segmented armor, long tail) not *who it is*. The image slot does the identity work; the text handles motion, lighting, and sequence logic. Separating these two jobs is what makes the bypass viable.

**5. Anti-artifact language**
V3 introduces explicit negative constraints: "zero limb distortion," "zero face drift," "face and costume re-anchored after every cut." These don't guarantee results but they shift the model's probability distribution away from the failure modes that are most common in long multi-character sequences. Think of it as telling the model what *not* to do, which is just as important as describing what to do.

**6. Energy FX layering**
Rather than saying "green glowing sword," V3 specifies a three-layer structure: bright core / saturated mid / transparent fade edge. This matters because flat single-color glow is a default model shortcut — giving it a layered description pushes it toward the more complex, anime-quality energy rendering seen in the reference images.

---

### Prompt Version Summary (English)

**V1 — Proof of Concept:** Minimal generic descriptors just to get past moderation. No timing structure, no camera language. Result was rough but proved the bypass worked.

**V2 — Pacing & Motion Fix (Current):** Added explicit timestamp segments, slow-motion directives at key beats, HDR contrast language for the transformation burst, and camera work instructions throughout. Fixed the rushed/blurry feel from V1.

**V3 — Character Consistency (Experimental):** Doubled down on per-character physical description to reduce face drift and costume inconsistency across frames. Added anti-artifact negative constraints and anime cinematic style anchoring. Higher ceiling but more likely to need retries.

---

## 💡 Tips & Lessons Learned

- Submit images in exact @1→@4 order every time — order matters for slot mapping
- English phrases like `"YOU ARE NOT PREPARED!"` can sometimes trigger moderation; fallback: replace with `宣言台词（英文，唇形同步）`
- Two-character high-speed sequences degrade generation quality fast — simplify motion if quality tanks
- Seedance 2.0 handles single-character clips well; multi-character + high action is at the edge of its capability
- HDR contrast instructions help but the model still struggles with consistent lighting across a 10–12s window
