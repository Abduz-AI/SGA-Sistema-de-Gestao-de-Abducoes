---
name: Orbital Command & Telemetry
colors:
  surface: '#0f131d'
  surface-dim: '#0f131d'
  surface-bright: '#353944'
  surface-container-lowest: '#0a0e18'
  surface-container-low: '#171b26'
  surface-container: '#1c1f2a'
  surface-container-high: '#262a35'
  surface-container-highest: '#313540'
  on-surface: '#dfe2f1'
  on-surface-variant: '#bcc9cd'
  inverse-surface: '#dfe2f1'
  inverse-on-surface: '#2c303b'
  outline: '#869397'
  outline-variant: '#3d494c'
  surface-tint: '#4cd7f6'
  primary: '#4cd7f6'
  on-primary: '#003640'
  primary-container: '#06b6d4'
  on-primary-container: '#00424f'
  inverse-primary: '#00687a'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb0cd'
  on-tertiary: '#640039'
  tertiary-container: '#ff79b4'
  on-tertiary-container: '#780047'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#acedff'
  primary-fixed-dim: '#4cd7f6'
  on-primary-fixed: '#001f26'
  on-primary-fixed-variant: '#004e5c'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffd9e4'
  tertiary-fixed-dim: '#ffb0cd'
  on-tertiary-fixed: '#3e0022'
  on-tertiary-fixed-variant: '#8c0053'
  background: '#0f131d'
  on-background: '#dfe2f1'
  surface-variant: '#313540'
typography:
  headline-xl:
    fontFamily: Space Grotesk
    fontSize: 40px
    fontWeight: '700'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Space Grotesk
    fontSize: 30px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Space Grotesk
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Space Grotesk
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: 0em
  headline-md:
    fontFamily: Space Grotesk
    fontSize: 22px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: 0em
  headline-sm:
    fontFamily: Space Grotesk
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: 0.01em
  body-lg:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Geist
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-lg:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 18px
    letterSpacing: 0.04em
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.06em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.08em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-mobile: 0.75rem
  margin: 2rem
  margin-mobile: 1rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2.5rem
---

## Brand & Style

The design system establishes a high-precision, military-grade science fiction telemetry and tactical command interface tailored for interplanetary resource management and biological specimen tracking. It blends the austere utilitarianism of aerospace orbital control consoles with bioluminescent data visualizations.

### Brand Personality & Emotional Impact
- **Sovereign & Classified:** Evokes the disciplined atmosphere of an orbital tactical operations center—clinical, hyper-focused, and authoritative.
- **Biotechnical Precision:** Balancing void-dark structures with electric bioluminescent indicators to convey advanced alien-monitoring telemetry without visual noise.
- **Mission-Critical Clarity:** Zero decorative fluff. Every pixel, border, and status pip delivers situational awareness for high-stress coordination across Gestores, Supervisores, Pesquisadores, and Cientistas.

### Design Style: Tactical Sci-Fi Functionalism
Drawing from technical HUDs, aerospace heads-up displays, and tactical operations software:
- **Surface Architecture:** Layered deep-void charcoals and space navies serving as high-contrast canvases for bioluminescent emissions.
- **Telemetry Glyphs & Reticles:** Hairline coordinate indicators, telemetry bracket marks, and mono-spaced readouts for classification levels, time-to-containment, and vitals.
- **Dense Data Cartography:** High-information density compact grids optimized for mission logs, biological extraction stages, and fleet allocation states.

## Colors

The palette is rooted in an abyss-grade dark spectrum, calibrated to protect operator night-vision and reduce cognitive fatigue in low-light command environments, while leveraging bioluminescent chromatic anchors for tactical routing.

### Palette Architecture
- **Base Canvas & Void Layers:**
  - `Canvas / Absolute Void`: `#0B0F19` (Foundation background)
  - `Surface 1 / Command Deck`: `#111827` (Card, sheet, and structural pane fills)
  - `Surface 2 / Module Deck`: `#1F2937` (Interactive surfaces, inputs, hover states)
  - `Surface Hairline / Structural Border`: `rgba(55, 65, 81, 0.7)` or `#374151`
- **Primary / Telemetry Cyan (`#06B6D4` / `#22D3EE`):** The primary signal frequency for interactive actions, system navigations, tactical waypoints, and operational data streams.
- **Secondary / Bioluminescent Specimen Emerald (`#10B981`):** Biological telemetry, active atmospheric stabilization, verified extractions, and confirmed lifeforms.
- **Tertiary / Xenobiotic Magenta (`#EC4899`):** Anomaly flags, neural uplink states, and classified research alerts.
- **Status & Threat Matrix:**
  - `Pendente (Standby / Queue)`: Sky Slate (`#94A3B8` / `#64748B`)
  - `Em Andamento (Active Beam / Transmission)`: Xenon Cyan (`#06B6D4`)
  - `Adiada (Suspended / Cloaked)`: Warning Amber (`#F59E0B`)
  - `Concluída (Secured / Archived)`: Bio Emerald (`#10B981`)
  - `Cancelada / Breach (Aborted / Hostile)`: Critical Flare (`#EF4444`)

### Application Rules
- Never use pure `#FFFFFF` text. Body text operates at `#E2E8F0` (90% contrast against `#0B0F19`), and supporting technical metadata sits at `#94A3B8`.
- Limit glowing cyan and bio-emerald highlights to interactive triggers, status nodes, and critical chart telemetry to preserve scanability.

## Typography

The typographical system enforces strict functional delineation across three specialized type engines:

1. **Space Grotesk (Command & Headlines):** Modern geometric architecture engineered for tactical headers, sector codes, and top-level operational summaries. 
2. **Geist (Body & Analytical Readouts):** High-legibility neutral sans-serif that renders long incident manifests, biological extraction logs, and personnel directives with zero optical distraction.
3. **JetBrains Mono (Telemetry, Badges & Hardware Data):** Rigid tabular numbers and fixed-width parameters for GPS coordinates, biological subject IDs (`SUB-8819-AX`), clearance indicators, and elapsed abduction timers.

### Hierarchy & Treatment Rules
- All classification tags, status indicators, and coordinates (`label-sm`, `label-md`) must be styled in uppercase with letter-spacing tracking between `+0.04em` and `+0.08em`.
- Numerical statistics and telemetry metrics must always use tabular figures to prevent jitter during real-time data syncs.

## Layout & Spacing

The interface implements a fluid, high-density modular layout structured around a disciplined 8px/4px base grid. It is built mobile-first to support rapid tactical hand-held terminals (~390px viewport width) while scaling seamlessly into multi-monitor command center matrices.

### Form Factor Adaptations
- **Handheld Terminal (Mobile: 360px – 480px, Target: 390px):**
  - Margins: `1rem` (16px), Gutters: `0.75rem` (12px).
  - Single column tactical stack. Critical telemetry chips (battery, cloaking status, mission timer) dock into a sticky glass-void top app bar (56px tall).
  - Bottom command dock houses rapid operational toggles within comfortable thumb reach (minimum tap target: 44px).
- **Console Matrix (Tablet & Desktop: 768px – 1440px+):**
  - Margins: `2rem` (32px), Gutters: `1rem` (16px).
  - Multi-column distribution: 12-column grid splitting tactical map/telemetry canvas (8 columns) and specimen ledger / log manifests (4 columns).

### Spatial Density
Components leverage compact spacing tokens (`space-xs` and `space-sm`) for internal card metadata, reserving `space-lg` and `space-xl` strictly for structural separation between mission modules.

## Elevation & Depth

Visual hierarchy is maintained through high-contrast structural surfaces, low-opacity borders, and bioluminescent photon-bleed rather than muddy Drop Shadows. The UI resembles dark flight avionics layered over physical tactical glass.

### Surface Tiers
- **Tier 0 (Sub-Orbital Canvas):** Solid `#0B0F19`. System bedrock.
- **Tier 1 (Tactical Pods & Manifest Decks):** `#111827` overlaid with a sharp 1px border of `rgba(31, 41, 55, 0.8)`.
- **Tier 2 (Floating Inspections & Interactive Menus):** `#1F2937` with `border: 1px solid rgba(6, 182, 212, 0.25)` and a subtle ambient atmospheric glow: `0 8px 24px -4px rgba(0, 0, 0, 0.75), 0 0 16px -2px rgba(6, 182, 212, 0.12)`.
- **Tier 3 (Active Threat / Critical Overlays):** `#111827` enclosed by a 1px border in alert amber or magenta with `0 0 20px -2px rgba(239, 68, 68, 0.2)`.

### Technical Accents
- **Reticle Notches & Corner Anchors:** Tactical cards use 1px corner tick marks (or pseudo-elements simulating sensor brackets) to enforce the sci-fi telemetry atmosphere.
- **Backdrop Filters:** Translucent surfaces (such as navigation docks and inspection bottom sheets) use `backdrop-filter: blur(12px)` over a 85% opacity `#0B0F19` backdrop.

## Shapes

The design system adopts a disciplined, low-radius geometry (Level 1: Soft / Technical Precision). Curves are restrained to project aerospace engineering and military hardware durability, avoiding generic bubble aesthetics.

### Geometry Specifications
- **Base Components (Inputs, Buttons, Chips):** `0.25rem` (4px). Provides a clean corner that feels engineered and calibrated.
- **Panels & Telemetry Cards (`rounded-lg`):** `0.5rem` (8px). Maintains structure while keeping high corner tension.
- **Modals & Drawer Sheets (`rounded-xl`):** `0.75rem` (12px). Applied strictly to top corners of mobile command sheets.
- **Facet Accentuation:** Critical action nodes and high-priority cards may incorporate 45-degree chamfered corners (using angled clip-paths or SVGs) on the top-right corner to indicate classified or tactical modules.

## Components

### 1. Action Triggers & Tactical Buttons
- **Primary Operation (Cyan Vector):** Background `#06B6D4`, text `#0B0F19` (JetBrains Mono, bold, uppercase), hover background `#22D3EE`. Accented with a faint laser pulse on focus.
- **Secondary / Containment (Bio Emerald):** Background `rgba(16, 185, 129, 0.15)`, text `#10B981`, border `1px solid rgba(16, 185, 129, 0.4)`.
- **Ghost Tactical:** Transparent background, text `#94A3B8`, border `1px solid #1F2937`, hover text `#06B6D4`, hover border `#06B6D4`.
- **Height & Touch Standards:** `44px` on mobile with minimum 16px horizontal padding.

### 2. Status Badges (Telemetry Indicators)
Strictly formatted using `label-sm` with a fixed pulsing dot indicator (6px circle):
- **Pendente:** Background `rgba(100, 116, 139, 0.15)`, text `#94A3B8`, dot `#64748B`.
- **Em Andamento:** Background `rgba(6, 182, 212, 0.15)`, text `#22D3EE`, dot `#06B6D4` with CSS ping-pulse animation.
- **Adiada:** Background `rgba(245, 158, 11, 0.15)`, text `#FBBF24`, dot `#F59E0B`.
- **Concluída:** Background `rgba(16, 185, 129, 0.15)`, text `#34D399`, dot `#10B981`.
- **Cancelada:** Background `rgba(239, 68, 68, 0.15)`, text `#F87171`, dot `#EF4444`.

### 3. Telemetry Manifest Cards (High-Density)
- Constructed with `#111827`, bordered by `#1F2937`.
- **Header Line:** Sub-sector identification tag (`SUB-SEC 04-B`) in `label-sm` muted grey, accompanied by the primary Status Badge.
- **Core Section:** Subject codename in `Space Grotesk` (`body-lg`, bold), followed by coordinates and species classification in `JetBrains Mono`.
- **Footer Telemetry Grid:** Two or three mini columns displaying vitals, extraction beam stability (e.g. `98.4%`), and assigned operative clearance (e.g. `CIENTISTA-N4`).

### 4. Input Fields & Data Selectors
- Background `#111827`, default border `1px solid #374151`, text `#E2E8F0`, placeholder `#4B5563`.
- Active focus state: `border-color: #06B6D4`, subtle outer glow `0 0 0 2px rgba(6, 182, 212, 0.2)`.
- Numeric input fields feature monospace tabular formatting with integrated unit suffix chips (`LY`, `SEC`, `RAD`).

### 5. Checkboxes, Radios & Switches
- **Checkboxes:** 18x18px squared box, `roundedness: 0.125rem` (2px), border `1px solid #4B5563`. Checked state fills `#06B6D4` with an angular dark vector checkmark `#0B0F19`.
- **Toggles / Switches:** Aerospace slider style. Unchecked: track `#1F2937`, thumb `#64748B`. Checked: track `rgba(6, 182, 212, 0.3)`, thumb `#06B6D4`.

### 6. Role Clearance Banners & Context Controls
Dedicated status ribbons tuned to user security tiers:
- **Gestor:** Tactical Navy & Cyan header accents for system-wide dispatch and fleet allocation.
- **Supervisor:** Amber/Gold accents for approval queues and containment risk authorization.
- **Pesquisador & Cientista:** Bioluminescent Emerald and Magenta telemetry monitors showcasing gene-sequencing progress, biomonitor charts, and extraction field diagnostics.