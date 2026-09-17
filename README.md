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

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ecommerce-listing-image-set`](skills/ecommerce-listing-image-set) | [SKILL.md](skills/ecommerce-listing-image-set/SKILL.md) | 0.1.9 |

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

## What you get

- **A complete gallery plan** — Cover the hero, key features, product details, lifestyle context, size or fit, and included items without repeating the same message.
- **One SKU, one visual direction** — Keep product identity, color, materials, graphics, proportions, and brand treatment coherent across the full set.

## Use cases

- **Marketplace launches** — Prepare a structured hero-to-detail sequence for Amazon, Etsy, and other marketplace listings.
- **Shopify product galleries** — Show the product, benefits, scale, use context, and package contents in a cohesive storefront set.
- **Catalog refreshes** — Replace inconsistent legacy images with a coordinated gallery anchored to current product facts and photos.

## FAQ

### Which images can be included?

A set can include a hero, feature, detail, lifestyle, size or fit, and packaging or in-box views selected for the listing.

### Do I need verified product information?

Yes. Product identity, specifications, visible details, dimensions, and included items should be confirmed before the gallery is planned.

### Can one image be refined without changing the set?

Yes. A selected image can receive a focused edit while the accepted product and visual direction remain the reference.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.
