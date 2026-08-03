# Cardingenium 品牌设计规范 (Brand Guidelines)

> 本规范根据现有 Logo 素材整理，供网站设计 / 前端开发直接参考使用。

---

## 1. 品牌标志 (Logo)

### 1.1 图形标志 (Icon Mark)
Logo 图形由字母 **J / U / L**（心血管 Cardio 相关首字母的抽象笔画）交织构成一个 **心形轮廓**，象征"心脏医疗科技"的品牌定位。图形左半部为蓝色、右半部为红色，中间以渐变过渡衔接，寓意"血液循环 / 动静脉"的双色系统。

### 1.2 组合标志 (Combination Mark)
标准组合方式为：**图形 Icon（左）+ 中文/英文品牌名 Cardingenium（右）+ 副标语 Medical Technology（品牌名下方，字号更小）**。

### 1.3 配色变体（按优先级）
| 优先级 | 主标题颜色 | 副标语颜色 | 使用场景 |
|---|---|---|---|
| ⭐️ 首选 | 红色 Cardingenium / 蓝色 Medical Technology（双色版，见右上角"堆叠版"） | — | 首页 Hero、品牌主视觉 |
| 常规 A | 全红 | 全红 | 医疗/警示/CTA 相关场景 |
| 常规 B | 全蓝 | 全蓝 | 常规页面、Header/Footer |
| 常规 C | 蓝色主标题 + 黑色副标语 | — | 印刷物、名片 |
| 单色 | 全黑 | 全黑 | 传真、印章、纯黑白物料 |
| 反白 | 全白 | 全白 | 深色背景（图片/深色卡片）上使用 |

### 1.4 图形单色版本
- **渐变版**（蓝→红）：官方默认，用于彩色场景
- **纯蓝版**：用于蓝色主题页面 / favicon 备选
- **纯红版**：用于红色主题页面 / 警示或强调场景
- **纯黑版**：用于黑白印刷
- **纯白版**：用于深色背景

### 1.5 字母标 / 极简标 (Monogram)
存在一个进一步简化的字母图标版本（形似 "JUI工" 结构），可用于极小尺寸场景，如 Favicon、App 图标、社交媒体头像。**建议网站 favicon 直接使用此简化版或渐变心形图标的简化描边版**，以保证在 16×16 / 32×32 px 下依然清晰可辨。

### 1.6 安全间距与最小尺寸建议
- 图形标志四周应保留 **不小于图形宽度 25%** 的空白区域，不与其他元素、边框重叠。
- 组合标志最小可用宽度建议 **≥120px**（数字端）/ **≥25mm**（印刷端），小于此尺寸应改用纯图形标或极简字母标。

### 1.7 使用禁忌 (Don'ts)
- 禁止拉伸、扭曲图形比例
- 禁止改变红蓝渐变的方向或替换为品牌色以外的颜色（单色版本除外）
- 禁止在低对比度背景（如浅灰底用浅色 Logo）上使用彩色/白色版
- 禁止给图形标志额外添加阴影、描边、光效等效果
- 禁止将"Medical Technology"副标语单独使用而缺失主标志

---

## 2. 品牌色彩系统 (Color Palette)

### 2.1 标准色（官方指定）
| 名称 | HEX | RGB | 用途 |
|---|---|---|---|
| **Standard Red** | `#E3051C` | 227, 5, 28 | 主强调色 / CTA / 警示 |
| **Standard Blue** | `#0074DE` | 0, 116, 222 | 主品牌色 / 链接 / 信任感场景 |
| Black | `#000000` | 0, 0, 0 | 正文文字、单色物料 |
| White | `#FFFFFF` | 255, 255, 255 | 反白、留白背景 |

### 2.2 建议扩展色板（网页设计用，基于标准色推导）
为满足网站深浅色状态、层级、禁用态等需求，建议扩展如下（与官方红蓝保持同色相）：

```css
:root {
  /* 品牌主色 */
  --brand-red:        #E3051C;
  --brand-red-dark:    #B00415;   /* hover / active */
  --brand-red-light:   #FDE8EA;   /* 浅底、标签背景 */

  --brand-blue:        #0074DE;
  --brand-blue-dark:   #005AAD;   /* hover / active */
  --brand-blue-light:  #E6F2FD;   /* 浅底、标签背景 */

  /* 渐变（用于 Hero、图形标志还原） */
  --brand-gradient: linear-gradient(135deg, var(--brand-blue) 0%, var(--brand-red) 100%);

  /* 中性色 */
  --neutral-black:  #0A0A0A;
  --neutral-900:    #1A1A1A;
  --neutral-700:    #4A4A4A;
  --neutral-500:    #8A8A8A;
  --neutral-300:    #D8D8D8;
  --neutral-100:    #F4F4F4;   /* 与 Logo 参考图背景色一致 */
  --neutral-white:  #FFFFFF;

  /* 语义色（医疗场景常用） */
  --color-success:  #1AA260;
  --color-warning:  #F2A900;
  --color-error:    var(--brand-red);
  --color-info:     var(--brand-blue);
}
```

> 背景基准色建议使用与 Logo 参考图一致的浅灰 `#F4F4F4` 作为页面底色，避免纯白造成刺眼感，同时能让红蓝 Logo 更突出。

---

## 3. 字体系统 (Typography)

Logo 中的字体为 **粗体、圆润、几何感强的无衬线字体**，笔画粗细统一、字重较高。网页开发中原 Logo 字体通常无法直接用于正文（版权/授权限制），建议使用风格相近的开源/系统字体：

| 层级 | 建议字体（西文） | 建议字体（中文） | 说明 |
|---|---|---|---|
| Logo / 大标题 | **Poppins** (Bold/ExtraBold) 或 **Montserrat** (Bold) | 思源黑体 Heavy / 阿里巴巴普惠体 Heavy | 与 Logo 圆润几何感接近 |
| 正文标题 H1-H3 | Poppins SemiBold / Inter SemiBold | 思源黑体 Bold | |
| 正文 Body | Inter / system-ui | 思源黑体 Regular | 保证可读性与医疗行业的专业感 |

```css
:root {
  --font-display: "Poppins", "PingFang SC", "Source Han Sans CN", sans-serif;
  --font-body: "Inter", "PingFang SC", "Source Han Sans CN", sans-serif;
}
```

---

## 4. 网站设计应用建议 (Web Application Guidelines)

### 4.1 Header / Navigation
- Logo 使用 **蓝色版组合标志**（常规 B），保证在浅灰/白色导航栏中清晰可读
- 导航链接 hover 态使用 `--brand-blue`，避免使用红色（红色保留给 CTA，形成视觉优先级）

### 4.2 CTA 按钮
- 主要 CTA（预约、咨询、购买）使用 **红色系** `--brand-red`，hover 用 `--brand-red-dark`
- 次要 CTA / 链接按钮使用 **蓝色系** `--brand-blue`

### 4.3 Hero 区块
- 可使用图形标志的 **渐变版本** 作为大尺寸视觉元素或装饰性背景图形
- 背景建议浅灰 `#F4F4F4` 或白色，避免高饱和背景与红蓝 Logo 冲突

### 4.4 Favicon / 移动端图标
- 使用第 1.5 节的极简字母标或图形标志的简化描边版本，确保小尺寸下依然可辨识
- 建议提供 16×16、32×32、180×180 (Apple touch icon) 多尺寸版本

### 4.5 深色模式 / 深色背景区块
- 使用 **反白版组合标志**（全白）
- 深色背景建议使用中性黑 `--neutral-900`，避免纯黑 `#000` 造成对比过强

### 4.6 无障碍与对比度
- 正文文字避免直接使用标准红 `#E3051C` 作为大段文字颜色（与白底对比度约 4.2:1，接近临界值），大段正文建议使用 `--neutral-900`
- 标准蓝 `#0074DE` 与白色背景对比度约 4.6:1，可用于正文链接，但小字号建议加粗或使用 `--brand-blue-dark`

---

## 5. 快速交付给 Claude Code 的设计令牌 (Design Tokens)

以下 CSS 变量可直接复制到网站项目的全局样式文件中，作为 Claude Code 构建网站时的设计基础：

```css
:root {
  /* Colors */
  --brand-red: #E3051C;
  --brand-red-dark: #B00415;
  --brand-red-light: #FDE8EA;
  --brand-blue: #0074DE;
  --brand-blue-dark: #005AAD;
  --brand-blue-light: #E6F2FD;
  --brand-gradient: linear-gradient(135deg, #0074DE 0%, #E3051C 100%);

  --neutral-black: #0A0A0A;
  --neutral-900: #1A1A1A;
  --neutral-700: #4A4A4A;
  --neutral-500: #8A8A8A;
  --neutral-300: #D8D8D8;
  --neutral-100: #F4F4F4;
  --neutral-white: #FFFFFF;

  --color-success: #1AA260;
  --color-warning: #F2A900;
  --color-error: #E3051C;
  --color-info: #0074DE;

  /* Typography */
  --font-display: "Poppins", "PingFang SC", "Source Han Sans CN", sans-serif;
  --font-body: "Inter", "PingFang SC", "Source Han Sans CN", sans-serif;

  /* Radius / Spacing (建议，配合圆润 Logo 风格) */
  --radius-sm: 6px;
  --radius-md: 12px;
  --radius-lg: 20px;
}
```

---

## 6. 待补充事项（建议向设计团队/原设计师确认）

- [ ] Logo 使用的西文字体原始名称（若有授权字体文件，可用于官网标题）
- [ ] 图形标志的矢量源文件（SVG/AI），当前仅有位图参考，网页端建议统一切图为 SVG 以保证清晰度
- [ ] 是否有官方指定的辅助色（除红蓝黑白外的强调色，如按钮成功/失败状态色）
- [ ] Logo 在社交媒体（微信/微博/LinkedIn 等）头像位的专用裁切版本

---

*本文档基于现有 Logo 规范图整理推导而成，颜色数值取自图中标注的"Standard red: E3051C"与"Standard blue: 0074DE"，其余扩展色板、字体建议与网页应用规则为基于品牌视觉风格的专业建议，正式使用前建议与品牌负责人确认。*
