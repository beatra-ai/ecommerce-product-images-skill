# Ecommerce Product Images Skill

English | [简体中文](./README.zh-CN.md)

Turn real product photos and confirmed SKU facts into a matching ecommerce image set: a hero image, feature visuals, lifestyle scenes, size views, and in-box images, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn verified SKU facts and product photos into a cohesive ecommerce image set with a hero image, feature visuals, lifestyle scenes, size views, and in-box images. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="A four-image listing set for a fictional NORTHLOOP 750 ml insulated bottle in matte sage (white-background hero, cap-and-neck detail, desk lifestyle scene, and in-box view), each made from the same source product photo. AI-generated with Beatra."></p>

*A four-image listing set for a fictional NORTHLOOP 750 ml insulated bottle in matte sage (white-background hero, cap-and-neck detail, desk lifestyle scene, and in-box view), each made from the same source product photo. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ecommerce-listing-image-set`](skills/ecommerce-listing-image-set) | [SKILL.md](skills/ecommerce-listing-image-set/SKILL.md) | 0.2.7 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ecommerce-listing-image-set). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/ecommerce-product-images-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/ecommerce-product-images-skill ecommerce-listing-image-set
```

Or clone this repository and copy `skills/ecommerce-listing-image-set` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ecommerce-listing-image-set skill from https://github.com/beatra-ai/ecommerce-product-images-skill (folder skills/ecommerce-listing-image-set), then follow its SKILL.md to connect my Beatra account.
```

## Examples

<p align="center"><img src="assets/demo-2.webp" width="800" alt="The source photo of a fictional NORTHLOOP bottle on a kitchen table (itself AI-generated for this demo) beside the white-background hero made from it, with shape, color, and label text unchanged. AI-generated with Beatra."></p>

*The source photo of a fictional NORTHLOOP bottle on a kitchen table (itself AI-generated for this demo) beside the white-background hero made from it, with shape, color, and label text unchanged. AI-generated with Beatra.*

Prompt:

```text
[before] Casual smartphone photo taken by a small online seller of their own product: one insulated stainless steel water bottle standing upright on a light oak kitchen table next to a window. The bottle has a matte sage green powder-coated body, a straight cylindrical shape with softly rounded shoulders, a brushed stainless steel neck ring, and a matte sage green screw cap with a short brushed steel carry loop on top. On the front of the body, printed in small white bold sans-serif capital letters, is the exact word "NORTHLOOP", and directly below it in smaller white capitals the exact text "750 ml". Nothing else is written anywhere on the bottle. The bottle is shown front-on at a slight angle, a little off center, with a kitchen wall softly out of focus behind it. Plain daylight from the window, slightly flat phone-camera colors, mild noise, honest amateur product snapshot. Photorealistic, no people, no other text or logos anywhere. ||| [after] Create slot 1, the clean product hero for a marketplace listing. Image 1 is the exact verified SKU. Preserve its matte sage green body, straight cylindrical shape with softly rounded shoulders, brushed stainless steel neck ring, matte sage green screw cap with brushed steel carry loop, and the small white printed text "NORTHLOOP" with "750 ml" directly below it, exactly as they appear in image 1, with no other text on the bottle. Show the single bottle upright, centered, front-on at eye level with the text facing the camera, on a pure white seamless background with a soft contact shadow, the bottle filling about three quarters of the frame height. Soft diffused daylight from the upper left, gentle natural shadows, a calm muted palette of sage, warm white, and light oak, crisp photorealistic product focus, the bottle as the clear focal point of the frame.
```

## Specs

As of 2026-10-16. Live list: https://docs.beatra.ai/en/docs/models

- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); up to 4 images per request; canvas up to 16777216 pixels
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); up to 4 images per request; canvas up to 4194304 pixels

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Image to image 10; Image editing 6 (as of 2026-10-16), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Codex, OpenClaw.

## What you get

- **A complete gallery plan** — Cover the hero, key features, product details, lifestyle context, size or fit, and included items without repeating the same message.
- **One SKU, one visual direction** — Make every image show the same product, with color, materials, graphics, proportions, and brand treatment kept consistent.

## Use cases

- **Marketplace launches** — Prepare a structured hero-to-detail sequence for Amazon, Etsy, and other marketplace listings.
- **Shopify product galleries** — Show the product, benefits, scale, use context, and package contents in a cohesive storefront set.
- **Catalog refreshes** — Replace inconsistent legacy images with a coordinated gallery anchored to current product facts and photos.

## FAQ

### Which images can be included?

A set can include a hero, feature, detail, lifestyle, size or fit, and packaging or in-box views selected for the listing.

### Do I need verified product information?

Yes. The exact product, specifications, visible details, dimensions, and included items should be confirmed before the gallery is planned.

### Can one image be refined without changing the set?

Yes. A selected image can receive a focused edit while the accepted product and visual direction remain the reference.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update ecommerce-listing-image-set` or `gh skill update ecommerce-listing-image-set`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai
- Docs — https://docs.beatra.ai
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
