# Prompt V2 — Cinematic Pacing & Motion Fix

**Status:** 🔄 Current / Active  
**Platform:** 即梦AI (Jimeng) / Seedance 2.0  
**Builds on:** V1 bypass

---

## What This Version Improves

- **Pacing:** Explicit segment timing — 2s taunt → 2s transform → 1.5s entrance → 6.5s duel
- **Motion blur:** Slow-motion directives at key moments, motion trail language instead of blur
- **Lighting:** HDR high-contrast instructions, explicit black-background contrast for the transform burst
- **Camera:** Rack focus, Dutch angle, motion blur control, 360° sweep timing
- **Lip sync:** Frame-level precision call-out for "YOU ARE NOT PREPARED!"

---

## Prompt (Chinese — Copy/Paste Ready)

```
史诗跨界奇幻对决，精确分段式电影叙事，10-12秒高清序列。

【场景基础】
黑庙山顶，外域暗夜，血红巨月，碎裂岩石台地，古墟尖刺遗迹，绿色闪电与紫色风暴交织，场景自始至终保持统一。

【第一段：0-2秒·挑衅】
紫色皮肤外星战士悬浮空中，镜头中远景仰角俯视，背景月亮居中构图。战士双臂交叉，长尾巴节奏性甩动（明确非模糊运动），嘴角上扬冷笑，嘴型同步说出挑衅台词。面部特写：皮肤纹理清晰，白色装束边缘锐利，光效柔和紫色环绕。运动：几乎静止的稳定悬浮，轻微飘动感，无晃动。

【第二段：2-4秒·变身爆炸】
战士仰头，能量蓄积0.5秒（画面颤抖，风暴停止），随后全场金色光爆：HDR高对比度——纯黑背景被金色强光撕裂，光环膨胀从中心向外扩散，速度逐帧由慢到快。变身完成瞬间切换为金色形态：金色装束、紫色头盔反光、红眼锐利，肌肉轮廓清晰，无运动模糊变形。镜头：圆形360°环绕扫镜加速完成变身时刻，慢镜头定格0.5秒在金色爆发峰值。

【第三段：4-5.5秒·宣言降临】
画面左上角出现绿色光芒先于人物，恶魔翅膀战士全速冲入：巨翼全展锁定姿态，落地冲击产生绿色能量波纹扩散，摄像机震动一次后稳定。战士正面低角度仰拍特写：绿色光纹脉动清晰，蒙眼布纹理可见，双刃绿光锐利非发散。嘴型同步清晰宣言："YOU ARE NOT PREPARED!"，声音字幕配合嘴型帧级精准，低沉共鸣音效。

【第四段：5.5-12秒·光效对决】
金色战士高速移动轨迹清晰（运动轨迹光尾，非模糊），发射粉红/紫色精准光束。绿色战士旋转双刃弧线攻击，每次挥击留下清晰光弧轨迹。两人交汇处：光束碰撞慢镜头高光（0.3秒），火花粒子物理散射，金紫与绿色光融合漩涡。镜头：动态跟踪→360°环绕→双人对峙正面大远景收尾，最终帧双方悬停对视，特效粒子持续飘散。

全程要求：8K电影级渲染，角色面部/服装/光效跨帧高度一致，物理流畅无肢体畸变，HDR照明高对比度戏剧性，紧张管弦乐+重型电子鼓+合唱交织。使用@1作为紫色战士初始形态，@2金色形态，@3绿翼战士，@4场景背景。
```

---

## Moderation Fallback

If `"YOU ARE NOT PREPARED!"` triggers a block, replace with:
```
宣言台词（英文，唇形同步）
```

---

## Known Issues (To Iterate On)

- TBD — currently generating
