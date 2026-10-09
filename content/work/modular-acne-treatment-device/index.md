---
title: "MODULAR ACNE TREATMENT DEVICE"
pubDate: "2025-12-31"
description: "LED-based modular acne treatment system allowing users to create custom shape configurations for conformity along anatomy contours."
---

*A modular phototherapy device that adapts to your body instead of forcing your body to fit the device. By snapping together solar-powered hexagonal modules, users compose treatment arrays that conform precisely to small facial crevices or larger zones like the back, with blue and red light calibrated for individual skin needs.*

**Role:** Engineer + designer (research, industrial design, electronics)\
**Duration:** 6 months\
**Context:** MSc Product Design Engineering & Manufacturing thesis, completed with First Class Distinction

![Final hexagonal module design assembled into a shoulder configuration](images/hex-hero.jpg)

### THE PROBLEM
Acne vulgaris is one of the most prevalent dermatological conditions worldwide, affecting adolescents and a significant proportion of adults. Yet home-use phototherapy devices remain fixed in form, assuming one shape fits every face. Rigid masks fail to conform to individual anatomy, leaving some areas undertreated or missed entirely, while handheld wands can't efficiently cover larger zones like the back. Available devices rarely accommodate the reality that treatment needs change, from spot-treating small crevices of the face to covering broad body areas, forcing users to buy separate products for each scenario.

Beyond fit, current devices are often disposable in nature and tethered to charging infrastructure, raising concerns about electronic waste and long-term sustainability. None deliver a treatment system that adapts to the user rather than the reverse. This project addresses that gap by combining hexagonal, snap-together modularity into a streamlined, solar-powered solution that reconfigures treatment geometry on demand, letting users compose small patches or large arrays from the same system while minimising environmental impact through recycled and repairable components.

### RESEARCH & CO-DESIGN WITH CLINICIANS

This project found its footing through biweekly design reviews with a dermatologist, who gathered patient reactions to each iteration. Those indirect voices, filtered through clinical expertise but grounded in real treatment experiences, kept every decision anchored in what actually matters to users.

#### PRIMARY USER RESEARCH

- **Online survey:** distributed via r/AcneTreatments (12 completed responses from 274 views)
- **Anonymous patient feedback:** gathered through an NHS dermatologist liaison at Ealing Hospital (6 participants)
- **Competitive analysis:** four market leaders: Shark Cryoglow, LUSTRE ClearSkin Solo, LightStim for Acne, Celluma PRO

#### KEY FINDINGS

| **Insight** | **Design Response** |
|---------|-----------------|
| 83.3% of users rated phototherapy as "most effective" but complained about limited body coverage | Modular system adaptable to face, back, chest, limbs |
| "Ease of use" emerged as #1 device selection criterion | Single-button operation, automatic 5-minute shutdown |
| 50% of users willing to pay £100–£199 | Target retail pricing aligned with mass-market affordability |
| Users wanted hands-free treatment to multitask during sessions | Temporary medical adhesive + self-supporting hex array |
| Sustainability concerns weren't captured in survey but surfaced in qualitative feedback | rPETG housing, solar charging, repairable modular architecture |

#### ITERATIVE CONCEPT DEVELOPMENT

Two initial concepts competed for selection:

1. **Wand design (Concept 1):** interchangeable heads, handheld operation
2. **Panel design (Concept 2):** flexible modular pads, potential for passive treatment

User feedback showed the panel approach scored higher on ergonomic design (4.33/5 vs 2.83/5) and treatment area coverage, but lacked a secure attachment mechanism. After two feedback cycles, the final hexagonal modular architecture emerged, balancing compactness, modularity and hands-free capability.

![Early concept iterations showing wand vs panel approaches](images/hex-iteration.jpg)

---

### THE DESIGN

#### MODULAR HEXAGONAL ARCHITECTURE

Each module is a 50 × 50 mm hexagon containing six LEDs. Modules snap together physically and electrically; bar-and-clasp joints with copper contact plates carry power and signal across the array. 

- Treatment of a cheek may only require one or two modules, treatment of the entire back may take twenty.
- The alternating bar-and-clasp system allows flexibility on curved anatomy while maintaining electrical continuity.

#### MATERIAL SELECTION

A systematic scoring matrix ranked materials against several criteria (impact resistance, UV resistance, skin safety, heat resistance, biodegradability, recyclability).

| **Material** | **Total Score** |
|----------|-------------|
| PETG | **23** |
| TPU | 21 |
| PHA | 21 |
| ABS | 17 |
| PLA | 15 |
| SLA resin | 10 |
\
PETG was chosen for its combination of durability, skin safety and recyclability. rPETG (recycled PETG) or bio-PETG variants were flagged for future production runs to enhance circularity.

The enclosure splits responsibilities:

- **Hard PETG shell:** structural integrity, houses electronics
- **Silicone-like diffuser:** skin-contact surface, disperses light evenly, conforms to anatomy

#### POWER BUDGET

| **Component** | **Current** | **Voltage** | **Power** |
|-----------|---------|---------|-------|
| Blue LEDs × 3 | 75mA | 3.2V | 240mW |
| Red LEDs × 3 | 75mA | 2.1V | 158mW |
| Status LED | 2mA | 2.0V | 4mW |
| ATtiny85 MCU | 1mA | 3.7V | 3.7mW |
| **Total** | **155mA** | **3.7V** | **~413mW** |

A 200mAh LiPo cell provides 12+ treatment sessions per charge. Each module also carries a 30 × 15mm monocrystalline solar panel (5.5V, ≥150mA) providing trickle-charge topping-up during ambient light exposure, extending autonomy for a device worn under natural light conditions.

#### TREATMENT PROTOCOL

- Dual-wavelength therapy: blue (415nm) targets C. acnes bacteria; red (630nm) reduces inflammation
- 5-minute automated session with green status LED confirmation
- Temporary medical adhesive secures the array for the treatment duration (~10 minutes to apply and remove)

<img src="/images/cad-exploded.png" alt="Exploded CAD assembly showing PCB, battery, LEDs and housing" width="auto" height="500">

---

### OUTCOMES + VALIDATION

- First Class Distinction awarded for the MSc thesis
- Final concept received 4.50/5 aesthetic appeal and 4.33/5 personal use suitability ratings from user testing cohort
- Demonstrated technical feasibility through complete CAD modelling in Onshape, component selection, power budgeting and BOM development (22.5g total weight per module)
- Created a roadmap for commercialisation identifying regulatory pathways (ISO 13485), thermal validation requirements and physical prototype testing

---

### REFLECTIONS

#### WHAT WENT WELL

- Co-design de-risked the product. NHS dermatologist involvement shaped everything from adhesive choice to treatment cycle length. Without that clinical lens, I might have optimised for engineering elegance over user reality.

- Iterative feedback killed bad ideas early. The wand concept looked elegant on paper but scored poorly on reachability (back treatment) and fatigue. Cutting it after round-one feedback saved months of work.

- Modularity solved a real problem. Fixed-form devices impose their limits on the user. Allowing users to build their own treatment geometry addressed the core frustration they voiced.

#### FURTHER WORK

- **No FEA structural validation:** Stress concentrations, drop-impact resilience and creep under load remain untested. For a medical device advancing toward ISO 13485, this becomes indispensable.
- **No physical prototype fabrication:** The CAD proves form and fit, but thermal performance, material ageing under LED exposure and adhesive reliability need bench testing.
- **Solar harvesting assumptions:** Indoor lighting produces milliwatts while six LEDs draw ~150mA. The panels are positioned as trickle-charge contributors rather than primary power sources; a more rigorous energy audit would clarify the autonomy window.

---

### TECHNICAL ARTIFACTS AVAILABLE

- Complete Onshape CAD models (main housing, top cover, PCB sub-assembly, full assembly constraints)
- Bill of Materials with component specifications and supplier references
- Material selection matrix with scored comparisons across six candidate polymers
- User research datasets (survey responses, Likert-scale feedback tables)
- Thesis full report (68 pages, available on request)