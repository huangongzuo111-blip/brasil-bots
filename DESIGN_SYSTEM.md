# 9 个 Bot 的统一视觉系统 —— 设计理念 + 出图指令

> 给 GPT / DALL·E / Midjourney 用。每条 prompt 可直接复制。

---

## 一、先回答两个问题

### ① 要不要统一画风？**要。**

你现在 9 个头像是各不相同的风格（自己做的、临时生成的）。它们在**目录页里并排出现**，不统一会显得像"从网上随便捡的"。

**统一的价值不在于"好看"，而在于：**

```
9 个风格各异的头像  →  看起来像 9 个不同的人做的
9 个风格统一的头像  →  看起来像一个品牌的产品线   ← 这才是你要的
```

你在做的是**产品矩阵**，统一视觉是"矩阵"最便宜的证明方式。

### ② 背景用「巴西风景」还是「科技感」？**两个都别直接用。**

这是关键判断，理由很具体：

**❌ 巴西风景照（基督像 / 海滩 / 雨林）**

| 问题 | 说明 |
|---|---|
| **40px 下糊成一团** | 头像在 Telegram 聊天列表里只有约 40×40，风景照在这个尺寸下**只是一坨彩色噪点** |
| **9 个分不清** | 都放风景 → 缩略图长得一模一样 → 用户认不出哪个是哪个 |
| **"旅游感"错位** | 你的产品是**工具**（找工作/比价/看新闻），不是旅游宣传。基督像传达的是"度假"，不是"帮你找工作" |

**❌ 纯科技感（渐变色块 / 光效 / 电路板）**

| 问题 | 说明 |
|---|---|
| **谁都能用** | 所有科技产品都长这样 → **没有辨识度** |
| **看不出功能** | 用户不知道哪个是找工作的、哪个是看球的 |
| **容易显廉价** | "深蓝渐变 + 发光线条"已经是最常见的 AI 生成套路 |

### ✅ 我的建议：**「统一容器 + 独立符号」**

```
统一的部分：深色底 + 粗线条扁平风格 + 单一符号居中 + 无文字
不同的部分：符号（每个 bot 一个）+ 主色（每个 bot 一个）
```

**为什么这个方案对：**

- **40px 下能认出来** —— 一个粗壮符号，缩多小都清晰
- **并排时是一套** —— 同样的底、同样的风格、同样的构图
- **每个有辨识度** —— 符号不同、颜色不同，一眼分得清

**巴西元素怎么放？** 不要用风景照，用**颜色**：

- 巴西国旗的 **绿 `#00A86B` + 黄 `#FFD60A`** 作为**点缀色**（不是主色）
- 这样既有巴西辨识度，又不会把头像变成明信片

---

## 二、统一的风格锚点（每条 prompt 都带）

```
minimal flat vector icon, square 1:1, one bold geometric symbol centered,
thick chunky shapes with confident line weight, solid dark charcoal
background (#0b0d11 to #161a21 subtle gradient), solid flat fills only,
no gradients on the symbol, no text, no letters, no numbers, no 3d,
no shadows, no glow, no realism, extremely high contrast,
simple enough to stay readable at 40x40 pixels, brand icon, clean crisp edges
```

**negative prompt（Midjourney 用 `--no`）：**

```
--no text, letters, words, numbers, watermark, 3d, realistic, photo,
gradient mesh, glow, shadow, clutter, multiple symbols, frame, border
```

**通用后缀（所有 9 条都加）：**

```
consistency series: same art style, same background treatment, same
line weight, same composition as a matching icon set
```

---

## 三、9 个 Bot 的符号与配色

| # | Bot | 符号（画什么） | 主色 | 寓意 |
|---|---|---|---|---|
| 1 | **Tribunal do Crush** | 破碎的心 + 法槌 | 玫红 `#FF4D8D` | 感情审判 |
| 2 | **Notícias Agora** | 报纸 + 闪电 | 天蓝 `#3EA6FF` | 即时新闻 |
| 3 | **Radar BR Viral** | 雷达波 + 火焰 | 橙红 `#FF6B35` | 热点追踪 |
| 4 | **Brasil Sem Filtro** | 对话气泡 + 感叹号 | 绿 `#00A86B` | 民生发声 |
| 5 | **Empregos Brasil** | 公文包 | 靛蓝 `#5B8DEF` | 找工作 |
| 6 | **Ofertas BR Hoje** | 价签 + 下降箭头 | 青绿 `#2EC4B6` | 比价省钱 |
| 7 | **Radardo Esporte** | 哨子 + 球 | 草绿 `#4CAF50` | 体育资讯 |
| 8 | **Futebol em Foco** | 足球 + 靶心 | 深绿 `#00A86B` 偏深 | 足球聚焦 |
| 9 | **Game na Veia** | 游戏手柄 | 紫 `#9B5DE5` | 游戏内容 |

**⚠️ 4 和 8 都用绿，要区分开**：4 用**明亮的绿**（国旗绿）+ 黄色点缀；8 用**深墨绿**。或者把 8 换成**橙黄**（球场灯光感）。

---

## 四、9 条可直接复制的 Prompt

> 每条都已经包含统一风格锚点。一次生成 4 张挑最好的。

### 1. Tribunal do Crush
```
minimal flat vector icon, square 1:1, a broken heart split down the middle
with a small judge's gavel crossing the crack, hot pink (#FF4D8D) symbol
on solid dark charcoal background (#0b0d11), thick chunky geometric shapes,
confident line weight, solid flat fills, no gradients, no text, no letters,
no 3d, no shadow, no glow, extremely high contrast, readable at 40x40 pixels,
brand icon, clean crisp edges, consistency series same art style
```
`--no text, letters, 3d, realistic, photo, gradient, glow, shadow`

### 2. Notícias Agora
```
minimal flat vector icon, square 1:1, a folded newspaper shape with a single
lightning bolt through it, sky blue (#3EA6FF) symbol on solid dark charcoal
background (#0b0d11), thick chunky geometric shapes, confident line weight,
solid flat fills, no gradients, no text, no letters, no 3d, no shadow,
no glow, extremely high contrast, readable at 40x40 pixels, brand icon,
clean crisp edges, consistency series same art style
```

### 3. Radar BR Viral
```
minimal flat vector icon, square 1:1, concentric radar waves with a small
flame at the center, orange-red (#FF6B35) symbol on solid dark charcoal
background (#0b0d11), thick chunky geometric shapes, confident line weight,
solid flat fills, no gradients, no text, no letters, no 3d, no shadow,
no glow, extremely high contrast, readable at 40x40 pixels, brand icon,
consistency series same art style
```

### 4. Brasil Sem Filtro
```
minimal flat vector icon, square 1:1, a bold speech bubble with an
exclamation mark inside, Brazilian flag green (#00A86B) symbol with a tiny
yellow (#FFD60A) accent on solid dark charcoal background (#0b0d11),
thick chunky geometric shapes, solid flat fills, no gradients, no text,
no letters, no 3d, no shadow, extremely high contrast, readable at 40x40
pixels, brand icon, consistency series same art style
```

### 5. Empregos Brasil
```
minimal flat vector icon, square 1:1, a simple briefcase, indigo blue
(#5B8DEF) symbol on solid dark charcoal background (#0b0d11), thick chunky
geometric shapes, confident line weight, solid flat fills, no gradients,
no text, no letters, no 3d, no shadow, no glow, extremely high contrast,
readable at 40x40 pixels, brand icon, consistency series same art style
```

### 6. Ofertas BR Hoje
```
minimal flat vector icon, square 1:1, a price tag with a downward arrow
beside it, teal green (#2EC4B6) symbol on solid dark charcoal background
(#0b0d11), thick chunky geometric shapes, confident line weight, solid flat
fills, no gradients, no text, no letters, no 3d, no shadow, no glow,
extremely high contrast, readable at 40x40 pixels, brand icon,
consistency series same art style
```

### 7. Radardo Esporte
```
minimal flat vector icon, square 1:1, a referee whistle, grass green
(#4CAF50) symbol on solid dark charcoal background (#0b0d11), thick chunky
geometric shapes, confident line weight, solid flat fills, no gradients,
no text, no letters, no 3d, no shadow, no glow, extremely high contrast,
readable at 40x40 pixels, brand icon, consistency series same art style
```

### 8. Futebol em Foco
```
minimal flat vector icon, square 1:1, a soccer ball inside a target reticle,
deep forest green (#00734A) symbol on solid dark charcoal background
(#0b0d11), thick chunky geometric shapes, confident line weight, solid flat
fills, no gradients, no text, no letters, no 3d, no shadow, no glow,
extremely high contrast, readable at 40x40 pixels, brand icon,
consistency series same art style
```

### 9. Game na Veia
```
minimal flat vector icon, square 1:1, a simple game controller, purple
(#9B5DE5) symbol on solid dark charcoal background (#0b0d11), thick chunky
geometric shapes, confident line weight, solid flat fills, no gradients,
no text, no letters, no 3d, no shadow, no glow, extremely high contrast,
readable at 40x40 pixels, brand icon, consistency series same art style
```

---

## 五、验收标准（做完必须自测）

**把 9 张图排在一起，然后：**

- [ ] **缩到 40×40** —— 每张还能认出是什么吗？（认不出就重做，别将就）
- [ ] **转成黑白** —— 还能区分出 9 个不同的符号吗？（检验形状差异，不是只靠颜色）
- [ ] **并排看** —— 像一套吗？（底座颜色、线条粗细、构图比例要一致）
- [ ] **有没有文字** —— 有文字的一律重做
- [ ] **深色/浅色主题下** —— 深色底的在 Telegram 浅色主题里会不会"糊掉"？

**最有用的一步**：把 9 张缩到 40px **拼成一张图**再看。大图上最好看的，往往小图里最糊。

---

## 六、目录页（Mini App）的背景怎么办

你说的"打开有背景"，我建议**不要用照片**，用**渐变 + 光晕**：

| 方案 | 评价 |
|---|---|
| **巴西风景照片** | ❌ 文件大（加载慢）、文字压图上看不清、跟"工具产品"气质不符 |
| **纯深色** | ⚠️ 安全但平淡 |
| **✅ 深色渐变 + 巴西绿黄的微妙光晕** | 有氛围、加载快、文字清晰、呼应巴西但不俗气 |

**做法**（我已经在用的思路，可以加强）：

```css
background:
  radial-gradient(120% 90% at 80% 0%, rgba(255,77,141,.22), transparent 55%),
  radial-gradient(100% 80% at 15% 10%, rgba(0,168,107,.18), transparent 60%),
  linear-gradient(180deg, #151018 0%, #0b0d11 100%);
```

想要更"巴西"，把第二个光晕换成**绿 + 黄**：

```css
  radial-gradient(100% 80% at 15% 10%, rgba(0,168,107,.20), transparent 60%),
  radial-gradient(90% 70% at 90% 20%, rgba(255,214,10,.14), transparent 60%),
```

**如果你还是想要图**：只在**顶部放一条 120px 高的巴西风景图**（下面完全纯色），文字不要压在图上。这样既有氛围，又不影响可读性和加载速度。

---

## 七、做完之后

头像做好后，替换文件即可（我会帮你处理）：

```bash
# 目录页用的头像（新增的）
~/brasil-bots-pwa/avatars/<BotUsername>.jpg

# 每个 bot 自己的头像（去 BotFather /setuserpic）
```

**而且头像要同时用于两处**：
1. **BotFather 的 `/setuserpic`** —— 用户在**聊天列表**里看到的
2. **目录页的 `avatars/`** —— 用户在**目录页**里看到的

**两处用同一张**，用户才能把"聊天列表里的那个"和"目录页里的那个"对上。
