# Prompt V3 — Character Consistency & Visual Epicness

**Status:** 🧪 Experimental  
**Platform:** 即梦AI (Jimeng) / Seedance 2.0  
**Builds on:** V2 pacing

---

## What This Version Improves

- **Character fidelity:** Face anchoring, costume detail lock, cross-frame consistency triggers
- **Anti-artifact language:** Explicit zero-distortion, zero-face-drift directives
- **Rendering style:** Anime cinematic cues referencing Dragon Ball Super: Broly battle sequences
- **Energy FX layering:** Core/mid/edge energy gradient instructions to prevent flat glow blobs
- Trades some timing granularity for deeper character description

---

## Prompt (Chinese — Copy/Paste Ready)

```
超高保真动漫电影风格·跨界奇幻对决·10-12秒·角色一致性优先版本

【视觉风格锚定】
融合现代动漫电影渲染（参考《龙珠超：布罗利》战斗序列）与西方奇幻史诗美学，超现实战斗光效，8K材质细节，物理准确流体动力学，零肢体畸变，零面部漂移。

【角色A·紫色皮肤外星战士·@1·@2参考锁定】
初始形态：紫色光滑皮肤无瑕疵，白色分段式装束每块护甲边缘清晰，长尾巴末端呈粉紫色渐变，面部特征精准——高颧骨、细长红眼、自信薄唇微扬。悬浮姿态：双臂交叉，身体轻微前倾45°，尾巴弧线自然垂曳。
金色变身形态（@2锁定）：全身金色包裹发光，紫色头盔反射金光，红眼在金色中更加锐利，肌肉轮廓膨胀但比例保持初始形态一致，绝对不改变脸部结构，金色光环呈同心圆向外扩散。

【角色B·绿翼蒙眼战士·@3参考锁定】
黑色紫灰色皮肤，绿色光纹沿脊骨和手臂清晰分布，大型恶魔翅膀膜面纹理可见（翅膀骨架清晰，非模糊块面），长角从头顶弧形向上，蒙眼布有布料折皱细节，双手巨型光刃：绿色能量刃边缘锐利分层，刃心明亮/外缘渐暗。宣言嘴型："YOU ARE NOT PREPARED!"——嘴型逐字精准，蒙眼布不遮嘴部。

【叙事节奏与镜头】
0-2s：战士A中远景悬浮挑衅，镜头稳定低仰角，月亮背景居中，台词嘴型同步，光效稳定柔和紫色氛围光。
2-4s：变身启动——能量蓄积静场0.3s，金色光爆从中心点向外膨胀，镜头快速环绕180°捕捉变身，峰值慢镜头0.5s定格，金光填满画面后收缩聚焦角色轮廓。
4-5.5s：战士B从高空急速俯冲入场，翅膀产生风压扭曲背景粒子，落地绿色冲击波圆形扩散，正面仰拍宣言特写，唇形同步。
5.5-12s：双人高速攻防，光束对撞慢镜头×2次（各0.4s），旋转全景镜头×1次，最终收尾：双方悬停，金紫与绿光交相辉映，粒子飘散，史诗合唱音乐峰值。

【技术抗畸变指令】
高速动作段：运动轨迹用光尾残影表达，非运动模糊；角色在每个镜头切换后面部服装重新锚定；物理骨骼动画流畅，翅膀扇动有膜面弹性形变；能量光效分层（核心白色/中层饱和色/外缘渐变透明），非单色发光球体。

使用@1紫色初始形态，@2金色形态，@3绿翼战士，@4场景背景。戏剧性管弦乐+电子战鼓+史诗合唱。
```

---

## Moderation Fallback

If `"YOU ARE NOT PREPARED!"` triggers a block, replace with:
```
宣言台词（英文，唇形同步）
```

---

## Notes

- Higher ambition than V2 — may need multiple retries
- If generation quality still degrades, simplify the duel segment (reduce to 1 slow-mo collision instead of 2)
- The anime rendering style anchor (`《龙珠超：布罗利》`) may itself trigger moderation — remove if needed and replace with `现代动漫电影渲染风格`
