---
name: 企业地产大亨 · Capital Club
description: A navy, gold and ivory club table for a Chinese-language company property game.
colors:
  stage: "#051734"
  stage-light: "#0b2a51"
  header: "#081d3f"
  navy: "#10294f"
  paper: "#f6f5eb"
  tile: "#fffef8"
  gold: "#f7c654"
  ink: "#0d2449"
  muted: "#53627a"
  danger: "#b33740"
  button: "#f9faf7"
  button-hover: "#e5eaf0"
  portfolio-card: "#fbfaf3"
  field: "#fffef7"
  focus: "#2185c5"
typography:
  display:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "32px"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "27px"
    fontWeight: 900
    lineHeight: 1.35
  body:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "14px"
    fontWeight: 400
  board-body:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "clamp(10px, calc(var(--board-size, 800px) / 66), 14px)"
  label:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "12px"
    fontWeight: 700
  wordmark:
    fontFamily: "Bruno, Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "10px"
    letterSpacing: "0.17em"
  dice-total:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "3.1em"
    fontWeight: 900
    lineHeight: 1
  primary-action:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "1.5em"
    fontWeight: 800
    lineHeight: 1.3
  turn:
    fontFamily: "Noto Sans SC, Microsoft YaHei, sans-serif"
    fontSize: "1.6em"
    fontWeight: 900
    lineHeight: 1.35
rounded:
  tile: "3px"
  ribbon: "4px"
  tab: "6px"
  compact: "8px"
  field: "9px"
  button: "10px"
  panel: "12px"
  compact-action: "13px"
  dialog: "16px"
  primary-action: "18px"
spacing:
  compact: "4px"
  tight: "5px"
  small: "7px"
  card: "8px"
  grid: "9px"
  control: "10px"
  panel: "12px"
  gutter: "14px"
  dialog: "22px"
components:
  button-primary:
    textColor: "#10264b"
    typography: "{typography.primary-action}"
    rounded: "{rounded.primary-action}"
    padding: "0.7em 0.5em"
  button-secondary:
    backgroundColor: "{colors.button}"
    textColor: "{colors.ink}"
    rounded: "{rounded.button}"
    padding: "10px 14px"
  button-secondary-hover:
    backgroundColor: "{colors.button-hover}"
  button-danger:
    backgroundColor: "#fff6f3"
    textColor: "{colors.danger}"
    rounded: "{rounded.button}"
    padding: "10px 14px"
  button-leave:
    backgroundColor: "transparent"
    textColor: "{colors.gold}"
    rounded: "{rounded.button}"
    padding: "10px 16px"
  field:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "10px 12px"
    height: "46px"
  panel-tab:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "{rounded.tab}"
    padding: "5px"
  panel-tab-selected:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.paper}"
  portfolio-card:
    backgroundColor: "{colors.portfolio-card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.panel}"
    padding: "10px"
  empty-portfolio:
    backgroundColor: "#eeeede"
    textColor: "{colors.muted}"
    rounded: "{rounded.button}"
    padding: "12px 8px"
---

# Design System: 企业地产大亨 · Capital Club

## Overview

**Creative North Star: "The Capital Club Table"**

The approved navy, gold and ivory world presents the game as a compact digital club table. A dark stage frames a warm reading surface; company marks, individual player colors and tactile dice supply the visual activity. Chinese text carries instructions and financial information, while the small English wordmark adds the club signature.

This document records the implemented `index.html`, rather than the proportions or sample data in the composition mockup. The approved portfolio-centered composition C is adapted to the product's true square board and logo cells. The detailed page composition belongs in `.impeccable/surfaces/index-html.md`.

**Key Characteristics:**

- A midnight stage, ivory surfaces and concentrated gold emphasis.
- Heavy Chinese headings and clearly ranked, tabular money values.
- Real company marks, illustrated special spaces and colored car pieces.
- Compact, softly rounded controls inside a strict square board.

## Colors

Warm paper and gold sit against deep navy; multicolor identity remains concentrated in company logos and player or property data.

### Primary

- **Club Gold** (`gold`): brand outline, header leave action, selection and the visual family of the main action gradient. The exact gradient stops remain component CSS in the sidecar.

### Secondary

- **Club Navy** (`navy`): structural dividers, selected mobile tabs and field caret.
- **Debt Red** (`danger`): negative balances and destructive controls. It is a state color, not a second decorative accent.

### Neutral

- **Midnight Stage** and **Stage Light** (`stage`, `stage-light`): the deep full-viewport backdrop and its restrained blue radial light.
- **Header Navy** (`header`): the compact top bar, slightly separated from the stage.
- **Club Paper** (`paper`): the center panel, lobby and property dialog.
- **Logo Ivory** (`tile`): company-cell base beneath contained brand marks.
- **Financial Ink** (`ink`): primary copy, balances and totals.
- **Slate Annotation** (`muted`): explanatory copy, metadata and supporting rents.
- **Control Chalk**, **Portfolio Cream** and **Field Ivory** (`button`, `portfolio-card`, `field`): small tonal distinctions between interactive surfaces.
- **Control Hover** (`button-hover`): the secondary button's hover fill.
- **Focus Blue** (`focus`): the visible keyboard outline, independent of decorative gold.

**The Identity Color Rule.** Keep real company marks multicolor. Player ownership and property-group colors come from game data; do not replace them with the club palette or use them as arbitrary page accents.

## Typography

**Display and Body Font:** Noto Sans SC, followed by Microsoft YaHei and sans-serif. The current HTML loads Noto Sans SC from Google Fonts; the fallback remains important when that request is unavailable.

**Wordmark Font:** Bruno, loaded from the local Bruno Ace SC font file (`assets/fonts/BrunoAceSC-Regular.ttf`), followed by the Chinese font stack.

**Character:** Bold, compact Chinese type keeps the board legible and decisive. The English wordmark is small and widely tracked. Financial figures use tabular numerals inherited from the body.

### Hierarchy

- **Display:** the lobby story heading uses the display role; its weight is the browser's bold heading weight (700).
- **Title:** the lobby form title uses the title role. The desktop Chinese brand is also bold (900), with its own tighter tracking and line height (1.25).
- **Body:** the page starts at the body role. Inside the board, the board-body role scales with the fitted square; secondary copy is generally a relative fraction of that size.
- **Label:** field labels use the label role; game metadata and compact actions also use small, strong text.
- **Wordmark:** the English brand uses the wordmark role, with uppercase text supplied by the markup.
- **Dice Total:** the dice-total role makes the sum the dominant result. At the mobile breakpoint it becomes a fixed size (25px).
- **Primary Action and Turn:** their relative roles put the next action and current-turn statement above supporting information. The short-desktop breakpoint uses fixed sizes (15px and 16px); mobile reduces both to compact text (12px).

**The Sum Rule.** The visible dice result and activity text report the total points. The two dice may show individual pip faces, but do not add a visible arithmetic equation.

## Layout

The page locks to the viewport with a flex column. Its desktop header is fixed in the layout (68px); the remaining space contains a centered square board and a compact footer. `fitBoard()` takes the smaller available shell dimension, sets equal width and height, and reserves an outside gutter of half a cell for the price ribbons. Equal grid tracks and square tile geometry preserve the logo cells in both modes.

The two board modes use 10 or 15 tracks per side, producing the required 36- or 56-space perimeter. The center occupies the tracks between the perimeter cells. The implementation uses proportional center padding (3.3%), a roster/action split (1.08fr / 1fr) and four-column owned-property cards. The portfolio does not stretch into spare space: activity follows it directly in the center's vertical flow. The center scrolls when its content grows, while the desktop activity feed has its own height limit (7em). These are surface composition details, not a requirement for every future screen.

The roster uses two equal columns with whole rows, showing at most two rows at once. Its row height is fixed on desktop (72px); a scrollbar gutter remains stable, and the active player's row is brought into view when it falls outside the visible roster. The heading states the player count and offers a scrolling cue when more than four players are present.

The first compact breakpoint (1100px) reduces the header brand and hides the English wordmark. A separate short-desktop query (width at least 701px and height at most 800px) tightens center padding (2.5%), roster rows (46px), dice, primary action and portfolio cards. It keeps the two-column roster and four-column portfolio, using smaller whole rows rather than clipping player content. The activity feed is bounded more tightly (4.8em).

At the mobile breakpoint (700px), the header is two rows (76px), the board remains square, and the center switches between 对局, 地产 and 记录 tabs. Only the selected section is shown; the center scrolls internally. Roster rows become compact (42px), still with a two-row viewport; the connection annotation is hidden to protect the count. The actions sit alongside the dice, and the portfolio becomes two columns. The mobile lobby collapses to one column and hides the large story copy and car illustration.

**The Square Rule.** Preserve equal logo-cell width and height, the real perimeter topology, outside price tags and all routine game controls within the inner square. The leave-room action stays in the header outside the board.

## Elevation & Depth

The system combines tonal layering with a few deliberate shadows. Paper panels separate by fill and fine borders. The board frame, lobby, property dialog and toast lift from the stage; the gold action has a restrained contact shadow. Dice use actual CSS faces and perspective rather than a flat pictogram, while car pieces float above their tile.

### Shadow Vocabulary

- **Board Frame** (`0 12px 30px #00000055`): anchors the board to the stage.
- **Gold Game Action** (`0 4px 7px #6a471b35,inset 0 -3px 3px #bd7c2d40`): combines a contact shadow and shaded lower edge on the central action.
- **Gold Form Action** (`0 3px 5px #5a411f26`): gives primary actions outside the central action stack a smaller tactile edge.
- **Lobby** (`0 22px 55px #020a243d`): separates the entry card from its overlay.
- **Property Dialog** (`0 18px 65px #020a243d`): gives the compact inspection surface clear priority.
- **Toast** (`0 5px 18px #020a2429`): temporary feedback above the game.

Motion is short for controls (160–200ms). A rolling die tumbles in alternating cycles (270ms); car pieces float gently (1.5s) and advance along the board in timed steps (155ms). The reduced-motion media query removes animations and transitions and centers each pawn without its floating transform.

## Shapes

The form language pairs an uncompromising square board with gently rounded controls. Cells are almost square-cornered; price ribbons have small corners. Cards use the panel radius; the dominant central action is rounder, using the primary-action radius. The lobby and dialogs use the dialog radius. The central action tightens to the compact-action radius on short desktops and the compact radius on mobile.

Fine, generally single-pixel borders separate warm surfaces. The center uses a stronger navy edge (2px). Ownership increases the company cell's colored border (3px) and adds inset/outer outlines, so ownership remains visible around the contained company mark. Company logos retain `object-fit: contain`; illustrated car pieces use the shipped raster with player-specific hue rotation.

## Components

### Buttons

Confident and compact, with the next game action clearly dominant. Primary game actions use a strong warm gold gradient, a gold-brown border, rounded corners and a shaded lower edge. Their labels change with roll, purchase, upgrade or auction state. The central action's typography, radius and padding are captured by the primary-action role and component above; short desktops use compact padding (9px), and mobile uses narrower padding (9px 5px). Primary form controls retain the smaller standard button radius and softer gold treatment. Secondary actions use a pale fill; within the action stack they become transparent and smaller. Danger controls use the red state color on a pale warm surface. The leave-room action is a gold outline on the dark header.

Hover changes the fill, active buttons move down slightly (1px), and disabled buttons lose opacity (0.5) and their shadow, including the stronger central action. All focusable controls receive the global blue outline (3px) with an offset (3px).

### Fields

Ivory fields use the field radius, a muted blue-gray border, the field height and inset padding captured above. Hover strengthens the border. Focus uses the global outline. The four-digit room field centers its value in large, tracked numerals; the room-code display uses a dark blue block and large gold digits.

### Cards / Containers

Player cards use warm neutral surfaces and compact car avatars; the active player becomes yellow with a darker gold border. Names truncate to one line, and cash stays visually strong. Fixed whole-row heights protect both lines of the player card and allow the active row to follow the turn.

Owned-property cards use Portfolio Cream, a real contained company mark, group-color strip, price, current rent and upgrade stars. Desktop logos scale between compact and prominent sizes (`clamp(40px, calc(var(--board-size, 800px) / 12), 90px)`); prices have strong relative size (1.4em), with company names and rent text supporting them (0.9em). The short-desktop query uses fixed logo and price sizes (42px and 16px); mobile uses smaller values (35px and 12px). Hover warms the card's fill and border. The empty portfolio uses centered instructions on a quiet inset surface.

### Navigation

The mobile center tabs appear only at the mobile breakpoint. A selected tab uses Club Navy and Club Paper, expressed through `aria-pressed`; inactive tabs use Slate Annotation. Tabs remain sticky at the top of the scrolling center panel. Their three labels correspond directly to game, properties and activity.

### Company Cells and Price Ribbons

Company cells are keyboard-accessible inspection targets as well as click and right-click targets. The mark fills the cell without being cropped. Number, actual purchase price and current rent sit in the outside ribbon. The top and bottom ribbons read upright; side ribbons rotate toward their corresponding edge. State and money come from the game rather than decorative sample content.

### Dice, Cars and Property Inspection

Two small ivory cubes use inline pip SVGs on six CSS faces. The large adjacent number is the sum. The shipped car (`assets/plates/player-car.png`) is shared by lobby art, player avatars and moving pieces, with hue variants identifying players. Special cells use inline scene illustrations.

Property inspection opens a closable, centered paper dialog with a dim stage backdrop, contained logo, two summary stats and a two-column rent list. The company name leads the header; a muted property identifier appears below it (11px, with a 6px top gap). The active rent row uses pale gold to show the current upgrade level without repeating the same level sentence in the explanatory note. The dialog is bounded to the viewport and scrolls internally, allowing temporary coverage of the center without changing board geometry.

## Do's and Don'ts

### Do:

- **Do** keep the board and logo cells square in both player modes.
- **Do** keep price and current-rent ribbons outside their corresponding company cells.
- **Do** preserve real company logos, dollar values and individual ownership colors.
- **Do** use the gold action, strong total and active-player state to make the next move clear.
- **Do** use the three center tabs on narrow screens and honor reduced motion.

### Don't:

- **Don't** copy mockup company data, sample prices or rectangular logo geometry into the game.
- **Don't** move routine controls outside the inner square or the leave-room control into it.
- **Don't** crop company marks, replace them with decorative monochrome marks or put price text over them.
- **Don't** introduce a visible dice arithmetic equation or unrelated decorative statistics.
