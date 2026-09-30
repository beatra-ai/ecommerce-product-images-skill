# Ecommerce Product Images Skill

[English](./README.md) | 简体中文

基于真实商品照片和已确认的 SKU 信息，一次规划并做出主图、卖点图、场景图、尺寸图和包装清单图，在 Claude Code、Codex 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 基于真实商品照片和已确认 SKU 信息，一次规划并制作主图、卖点图、场景图、尺寸展示和包装清单图。 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Codex、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="虚构品牌 NORTHLOOP 750 ml 哑光鼠尾草绿保温瓶的四张商品图组（白底主图、瓶盖与瓶颈细节、书桌生活场景、开箱图），均以同一张商品原图为参考生成。由 Beatra AI 生成。"></p>

*虚构品牌 NORTHLOOP 750 ml 哑光鼠尾草绿保温瓶的四张商品图组（白底主图、瓶盖与瓶颈细节、书桌生活场景、开箱图），均以同一张商品原图为参考生成。由 Beatra AI 生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ecommerce-listing-image-set`](skills/ecommerce-listing-image-set) | [SKILL.md](skills/ecommerce-listing-image-set/SKILL.md) | 0.2.3 |

本仓库由 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ecommerce-listing-image-set) 自动发布，问题请到那里反馈。

## 安装

使用 [`skills`](https://skills.sh) CLI：

```bash
npx skills add beatra-ai/ecommerce-product-images-skill
```

使用 GitHub CLI：

```bash
gh skill install beatra-ai/ecommerce-product-images-skill ecommerce-listing-image-set
```

也可以克隆本仓库，把 `skills/ecommerce-listing-image-set` 复制到 `~/.claude/skills/`（Claude Code）、`~/.agents/skills/`（Codex）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/ecommerce-product-images-skill 安装 ecommerce-listing-image-set skill（目录 skills/ecommerce-listing-image-set），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

## 效果示例

<p align="center"><img src="assets/demo-2.webp" width="800" alt="厨房桌上一只虚构品牌 NORTHLOOP 保温瓶的商品原图（这张原图本身也是为演示 AI 生成的），与据此生成的白底主图并排，瓶形、颜色和标签文字保持一致。由 Beatra AI 生成。"></p>

*厨房桌上一只虚构品牌 NORTHLOOP 保温瓶的商品原图（这张原图本身也是为演示 AI 生成的），与据此生成的白底主图并排，瓶形、颜色和标签文字保持一致。由 Beatra AI 生成。*

提示词：

```text
[before] Casual smartphone photo taken by a small online seller of their own product: one insulated stainless steel water bottle standing upright on a light oak kitchen table next to a window. The bottle has a matte sage green powder-coated body, a straight cylindrical shape with softly rounded shoulders, a brushed stainless steel neck ring, and a matte sage green screw cap with a short brushed steel carry loop on top. On the front of the body, printed in small white bold sans-serif capital letters, is the exact word "NORTHLOOP", and directly below it in smaller white capitals the exact text "750 ml". Nothing else is written anywhere on the bottle. The bottle is shown front-on at a slight angle, a little off center, with a kitchen wall softly out of focus behind it. Plain daylight from the window, slightly flat phone-camera colors, mild noise, honest amateur product snapshot. Photorealistic, no people, no other text or logos anywhere. ||| [after] Create slot 1, the clean product hero for a marketplace listing. Image 1 is the exact verified SKU. Preserve its matte sage green body, straight cylindrical shape with softly rounded shoulders, brushed stainless steel neck ring, matte sage green screw cap with brushed steel carry loop, and the small white printed text "NORTHLOOP" with "750 ml" directly below it, exactly as they appear in image 1, with no other text on the bottle. Show the single bottle upright, centered, front-on at eye level with the text facing the camera, on a pure white seamless background with a soft contact shadow, the bottle filling about three quarters of the frame height. Soft diffused daylight from the upper left, gentle natural shadows, a calm muted palette of sage, warm white, and light oak, crisp photorealistic product focus, the bottle as the clear focal point of the frame.
```

## 你能得到什么

- **从主图到详情图整套规划** — 覆盖主图、卖点、细节、场景、尺寸或比例与包装内容，避免多张图重复同一信息。
- **一个 SKU，一套视觉方向** — 每张图里都是同一件商品，颜色、材质、图案、比例和品牌表现保持一致。

## 适用场景

- **平台新品上架** — 为 Amazon、Etsy 等平台准备从主图到细节图的有序上架序列。
- **Shopify 店铺商品图** — 用统一套图展示商品本身、核心利益、尺寸、使用场景和包装内容。
- **存量商品图更新** — 以当前商品信息和照片为依据，替换风格不一致的旧图。

## 常见问题

### 套图可以包含哪些图片？

可根据上架需要选择主图、卖点图、细节图、场景图、尺寸或比例展示图，以及包装清单图。

### 必须提供已确认的商品信息吗？

是的。规划套图前应确认具体是哪款商品，以及规格、可见细节、尺寸和包装内容。

### 可以只精修其中一张吗？

可以。可对选中的图片做聚焦修改，同时以已采用的商品和视觉方向为依据。

## 更新

安装后的 skill 每天最多检查一次新版本，替换前先校验官方归档，任何一步失败都不会动你已安装的版本。
随时可以关闭，见 skill 内的 `references/automatic-updates-and-safety.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。
