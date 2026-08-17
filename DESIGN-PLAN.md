# Design plan — MB Hospitality & Management

## Direction
Editorial hospitality rather than a generic dark luxury template. The visual rhythm alternates near-black and porcelain sections. Gold is reserved for hairlines, menu-leader dots, focus states and restrained calls to action. The layout uses an asymmetric 12-column grid and keeps long text blocks left-aligned.

## Tokens
- Ink: `#0B0B0C`
- Ink soft: `#16161A`
- Porcelain: `#F5F3EE`
- Porcelain 2: `#EAE6DD`
- Gold: `#C9A24A`
- Gold light: `#E7CE93`
- Bronze: `#8A6A2F`
- Slate: `#7A7A80`
- Max content width: 1280px
- Radius: 2px

## Typography
The CSS is structured for Marcellus / Inter Tight / Archivo. The delivery ZIP intentionally does not redistribute font binaries; it uses system fallbacks until licensed WOFF2 files are added. See README.

## Homepage wireframe
```text
┌────────────────────────────────────────────────────────────────────┐
│ logo     About  Services⌄  Industries⌄  Process  Ref  Contact  LANG│
├────────────────────────────────────────────────────────────────────┤
│ eyebrow                                                            │
│ SERVICE, DER SICH RECHNET.                                         │
│ Standards, die im Alltag halten.                                   │
│ supporting copy              [initial call]  → services            │
│ ~~~~~~~~~~~~~~~~~ gold hairline ~~~~~~~~~~~~~~~~~                  │
├────────────────────────────────────────────────────────────────────┤
│         positioning statement (offset 8/12)                        │
├────────────────────────────────────────────────────────────────────┤
│ services  │ Hospitality Consulting ......... Analysis & operations │
│           │ Staff Training .................. Real-shift training   │
│           │ F&B Management .................. Concept / numbers     │
├────────────────────────────────────────────────────────────────────┤
│ Hotels              Restaurants                Bars                │
├────────────────────────────────────────────────────────────────────┤
│ sticky 01   │ Analyse                                               │
│             │ Konzept                                               │
│             │ Umsetzung                                             │
│             │ Begleitung                                            │
├────────────────────────────────────────────────────────────────────┤
│ portrait placeholder │ founder biography                           │
├────────────────────────────────────────────────────────────────────┤
│ honest references empty state                                      │
├────────────────────────────────────────────────────────────────────┤
│ native FAQ                                                          │
├────────────────────────────────────────────────────────────────────┤
│ CTA + dense footer                                                  │
└────────────────────────────────────────────────────────────────────┘
```

## Hero copy variants
1. **Recommended:** “Service, der sich rechnet. Standards, die im Alltag halten.” It connects commercial discipline and operational reality without making an unsupported claim.
2. “Gastlichkeit braucht Standards, die eine volle Schicht tragen.” More operational, slightly less business-oriented.
3. “Gute Abläufe bleiben unsichtbar. Ihre Wirkung nicht.” More editorial, but more slogan-like than option 1.

## Signature element
The dotted menu-leader line is borrowed from fine-dining menus and becomes the recurring navigation motif for services and deliverables. It draws from left to right on entry, with a 60ms stagger. A fork-and-hairline placeholder logo uses the same visual language.
