# Vaulta Web Design Reference

Use this file when designing the Vaulta webpage. All values extracted directly from the iOS app source.

---

## Brand Identity

- **App name:** VAULTA (always uppercase)
- **Premium tier:** VAULTA PRO
- **Tagline:** "Keep your real life private."
- **Tone:** Premium, dark, privacy-first, minimal, trustworthy
- **No light mode** — dark only, always

---

## Color Palette

### Backgrounds
| Name | Hex | Use |
|------|-----|-----|
| Main BG | `#0D0A17` | Page background |
| Deep BG | `#0A0812` | Cards, modals, sections |

### Brand Purple (primary accent)
| Name | Hex | Use |
|------|-----|-----|
| vaultAccent | `#9454FA` | Primary brand color, CTAs |
| vaultAccentDark | `#6E2ED1` | Hover states, shadows |
| vaultAccentLight | `#AE6DFF` | Highlights, borders |
| Paywall purple | `#8C61FF` | Secondary purple |
| Light purple | `#B88FFF` | Subtle accents |

### Feature Colors (icons, badges, highlights)
| Name | Hex | Use |
|------|-----|-----|
| Blue | `#619EFF` | Storage, cloud features |
| Purple | `#B870FF` | Decoy vault feature |
| Red | `#FF6161` | Alerts, danger, break-in |
| Orange | `#FF9E38` | App icons, warnings |
| Cyan | `#47D1EB` | iCloud sync feature |
| Green | `#38D97A` | Success, checkmarks |

### CTA Gold Gradient
- Start: `#FFEB48` → End: `#FF8A1F`
- Use for premium/upgrade call-to-action buttons

---

## Typography

Web font stack: `system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`

App uses SF Pro Rounded for headings — closest web equivalent: add `letter-spacing: -0.02em` on headings for similar feel.

### Scale
| Role | Size | Weight |
|------|------|--------|
| Page title / H1 | 28px | 700 |
| Section title / H2 | 22px | 700 |
| Subheading / H3 | 18px | 600 |
| Body | 16px | 400 |
| Secondary text | 13px | 400 |
| Caption / legal | 11px | 400 |

### Colors
- Primary text: `#FFFFFF`
- Secondary text: `rgba(255, 255, 255, 0.6)`
- Tertiary / placeholder: `rgba(255, 255, 255, 0.35)`

---

## Spacing & Sizing

### Corner Radius
| Use | Value |
|-----|-------|
| Primary cards, buttons | `14px` |
| Secondary elements, inputs | `12px` |
| Grid items, small chips | `10px` |
| Pill buttons | `9999px` (full round) |

### Padding
| Context | Value |
|---------|-------|
| Card inner padding | `14px` |
| Section spacing | `12px` |
| Compact / inline | `8px` |

### Gaps
| Context | Value |
|---------|-------|
| Media grid | `3px` |
| Card grid | `8px` |
| Section stacking | `12–14px` |

---

## Visual Effects

### Glass Cards
```css
background: rgba(255, 255, 255, 0.05);
backdrop-filter: blur(20px);
-webkit-backdrop-filter: blur(20px);
border: 1px solid rgba(255, 255, 255, 0.08);
border-radius: 14px;
```

### Page Background Glow
```css
background: radial-gradient(ellipse at 70% 0%, rgba(148, 84, 250, 0.15) 0%, transparent 60%),
            radial-gradient(ellipse at 30% 100%, rgba(110, 46, 209, 0.12) 0%, transparent 60%),
            #0D0A17;
```

### Card Shadow
```css
box-shadow: 0 2px 12px rgba(0, 0, 0, 0.4);
```

### Button Press Animation
```css
transition: transform 0.15s ease-out;
/* on :active */
transform: scale(0.97);
```

### Spring-like Hover/Transition
```css
transition: all 0.28s cubic-bezier(0.34, 1.56, 0.64, 1);
```

---

## Component Patterns

### Primary CTA Button
- Background: `#9454FA` solid or gold gradient `#FFEB48 → #FF8A1F` for upgrade
- Text: white, 17px, semibold
- Radius: `14px` or pill
- Padding: `16px 24px`

### Feature Row (used in paywall)
Layout: `[colored icon circle] [title + subtitle]`
- Icon circle: 32–36px, colored fill from feature colors table
- Title: 15px, semibold, white
- Subtitle: 13px, `rgba(255,255,255,0.6)`

### Settings / List Row
- Background: glass card
- Separator: `rgba(255,255,255,0.06)`
- Leading icon: colored circle or SF symbol equivalent
- Chevron right: `rgba(255,255,255,0.3)`

### Badge / Chip
- Background: `rgba(148, 84, 250, 0.25)`
- Border: `rgba(148, 84, 250, 0.4)`
- Text: `#AE6DFF`, 11px, semibold
- Radius: `6px`

---

## Page Layout Notes

- Max content width: `1100px`, centered
- Mobile-first, heavy use on iPhone → design for `390px` width baseline
- Navigation: minimal, dark, no heavy borders
- Hero: large headline + tagline + single CTA + subtle background glow
- Feature sections: 3-column grid on desktop, stacked on mobile
- Pricing: one card (free) + one card (Pro, highlighted with purple glow)

---

## Do / Don't

| Do | Don't |
|----|-------|
| Dark background always | Light mode / white backgrounds |
| Purple as primary accent | Multiple competing accent colors |
| Subtle glass cards | Heavy opaque boxes |
| Tight spacing, clean layout | Cluttered or busy layouts |
| Minimal copy, direct language | Long paragraphs or marketing fluff |
| Spring/elastic micro-animations | Heavy page transitions |
