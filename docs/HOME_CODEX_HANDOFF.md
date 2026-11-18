# Home Codex handoff: plumbing and purchase audit

Updated November 17, 2026 (America/Chicago).

## Start here

Danny wants to finish the whole-car plumbing and make sure every required fitting is on hand. Summit's main order was placed; do not treat its old cart or wishlist as an order record. This document preserves the audit and the remaining decisions so work can continue on the home computer.

Before editing, fetch and inspect `origin/main`, preserve other-agent changes, and read this document. The current primary schematic is `index.html`; the live site is https://dannydowns46.github.io/race-car-plumbing-atlas-site/ .

The November 17 audit initially used commit `1814ad95dc34196fc089bdf374707df9566f0dc7`. Before publishing this handoff, we incorporated remote commit `1e2514fa8f89b0c041b9fa6bbd26279045219cff`, which adds fuel vent circuits F10/F11. Earlier statements that tank vents were unspecified are superseded by that change. Their purchase status still needs evidence.

## Evidence and its limits

Purchase and receipt evidence confirms what was ordered; it does not establish that every item was delivered, retained, or physically fits. Original emails, invoices and customer addresses are not published in this public repository. Search the owner's connected Gmail using the references below if needed.

| Record | Evidence verified |
| --- | --- |
| Summit order 8143075, Nov 13, 2026; email subject `Confirmation & Order Status for your Order # 8143075` | Item SKUs and quantities in [the CSV](summit-order-8143075.csv). Two 25-foot rigid-tube coils were ordered, not one. |
| Dry Sump Solutions Receipt 1346, Aug 10, 2026, invoice 0001110, page 2 | DSS-TFK1: quantity 1 kit containing FOUR -12 ORB to -16 AN adapters and TWO -12 port plugs. Tank FR6D-1220 and breather 40FT-WM also listed. |
| Haltech order 11276315, confirmation dated Oct 24, 2026; warehouse reference SO1006819971 | HT-010910 fuel/oil pressure sensor, quantity 1, purchased; warehouse email lists it packed for shipment. Also lists two HT-010306 temperature sensors; their installation allocation is not established here. |
| Delta ABS order 1220, Oct 21, 2026 | Complete package includes two master-cylinder pressure sensors. The order lists no separate M10 bubble tees. |
| Owner's purchase confirmation in chat | EVIL ENERGY black aluminum 3/8 NPT internal-hex plugs, pack of 2: one for Mallory outlet #3, one spare. |

No purchase evidence was found for the outstanding items below in the checked Summit order or the targeted Gmail search. Do not interpret absence from these records as proof the owner cannot already have a part.

## Supplemental Summit purchase confirmed November 17

Owner provided an order screenshot showing **Ready to Ship**. The order number and placement date are not visible. These are ordered quantities, with delivery unconfirmed. See [supplemental order CSV](summit-supplemental-order-2026-11-17.csv).

| SKU | Qty on new screenshot | Allocation / open fit check |
| --- | ---: | --- |
| TIL-76-015 | 3 | Reservoir inlet adapters; final brake-master compatibility still requires confirmation |
| FRA-650205 | 2 | Brake-master hardline adapters; final mating outlet and allocation require verification |
| FRA-650302 | 1 | Clutch slave adapter; verify actual port and seat |
| SUM-220167B | 1 | F06 overflow-receiving hanger return adapter; verify bare port |
| FRA-229016-BL | 1 | Owner confirmed November 18: supplemental -16 90-degree hose end allocated to OIL5-4, oil strainer inlet. Four total ordered; current schematic uses three. |

The five visible lines total $114.05 before any tax or shipping. FRA-229016-BL cumulative ordered quantity is four (three in order 8143075, plus this one). The supplemental fitting is allocated to the oil strainer inlet (OIL5-4), confirmed November 18. This location already showed a 90-degree end. The schematic has three installation positions for this SKU, leaving one of the four ordered fittings without an installation allocation.

FRA-650205 is purchased, but the earlier assertion of direct fit at the master outlet needs verification of the actual mating interface. Preserve this fit check independently of purchasing status.

## Outstanding fittings

Quantities are installation requirements, not an instruction to buy every candidate immediately.

| Qty | Item / SKU | Installation location | Remaining action |
| ---: | --- | --- | --- |
| 2 | [Delta M10x1 DIN/ISO bubble tees](https://www.deltaabs.com/products/m10-bubble-tee) | B01/B03 pressure sensor branches before HCU | No purchase found. Sensors are included in the owned Delta kit; tees are separate. Support the tees on the chassis. Owner explicitly retained the Delta tees on November 17. OPS-UT10B-1 is not selected. |
| Up to 4 | [RUS-R40506](https://www.summitracing.com/parts/rus-r40506), candidate M10x1 banjo bolts | B07-B10, four C6 Z06 calipers | Not ordered. Inspect existing bolts; candidate grip/engagement remains unverified with new hose eyes and washers. |
| 1 if needed | 1/8 NPT male plug; [SUM-921015](https://www.summitracing.com/parts/sum-921015) was the listed eight-plug kit | OIL7 filter-mount probe/temperature port | Kit not ordered. Only needed if port is open and unused; verify whether a temperature sensor or existing plug occupies it. Owner's 3/8 NPT Mallory plugs are a different size. |

### Conditional additional pieces

- **F03 EVIL ENERGY fuel filter adapters: up to two.** Inspect exact owned filter and its supplied adapters. SUM-220165B is only applicable if its bare ports are confirmed -8 ORB. The THREE adapters on the Summit order are fully allocated: one at surge OUTLET2, one at Mallory upper inlet, one at Mallory bottom bypass. There are no two additional replacements allocated to the filter.
- **F09 Mallory vacuum reference:** original cap is missing. Confirm intended vacuum/boost reference setup and whether the original brass barb is present. Cap/hose/fitting choice remains unresolved; no finalized SKU.
- **OIL7 valve-cover vent/vacuum regulator:** hardware and interface remain unresolved; no final SKU.
- **Tank fill and drain connections:** still need confirmation on the actual tanks. Vent circuits are now specified below.
- **Supports:** fuel/brake hardline supports, coolant hardline isolators, and two sensor-tee supports need physical routing/fabrication confirmation. Do not confuse the owner's confirmed hose clamps with confirmation of every chassis support.
- **Submerged fuel plumbing:** DW100/DW200 pump barbs are listed as 5/16 inch; hanger internal barbs may be 3/8 inch. Three Dayco 80160 hoses were purchased, but any required size-transition fittings remain unresolved until inspected.

### Fuel vents added by the other agent: F10 / F11

Preserve these two independent vent paths. Each tank has an installed Speedway 458364 rollover valve with male -8 AN connection. Each route is:

`rollover valve -> straight -8 PTFE hose end -> -8 PTFE hose -> straight -8 PTFE hose end -> male/male -8 AN union -> female -8 AN / barb adapter -> remote breather filter`

The newer schematic selects:

| Total across both vents | Selection | Purchase status |
| --- | --- | --- |
| 2 rollover valves | Speedway 458364 | Recorded installed in remote update |
| 4 hose ends | EVIL ENERGY straight -8 PTFE ends; one four-pack | Selected; not in checked Summit order; verify separate purchase |
| 10 ft hose | EVIL ENERGY -8 PTFE, 10 mm ID; one shared roll | Selected; verify separate purchase and total routed length |
| 2 unions | EVIL ENERGY male -8 AN to male -8 AN; one two-pack | Selected; verify separate purchase |
| 2 filter kits | One red breather and female -8 AN/barb adapter per kit | Selected; verify separate purchase; adapters included with kits |

Exact Amazon IDs for the newly selected vent hose/filter kits were not recorded. Do not invent Summit SKUs or infer they were purchased merely because pictures were added. These vent parts are separate from the Summit fuel-supply hose inventory.

## Covered items and ownership corrections

- **HT-010910 fuel-pressure sensor is purchased.** Earlier ownership-unknown wording is superseded by the Haltech evidence. HT-039103 extension kit was ordered from Summit and includes the 18-inch hose, end adapters and clamps. Do not count its three schematic appearances as three kits.
- **DSS-TFK1 is purchased.** Allocate adapters to tank bottom outlet (OIL1), active tank return from XRP strainer (OIL5), tank vent (OIL6), breather inlet (OIL6). Allocate one -12 ORB plug to unused tank return and one to unused breather port (OIL7). Bare tank ports are -12 ORB; hose-side adapters present male -16 AN.
- **Cooling pump and thermostat:** water pump already has a 90-degree end accepting bare -16 hose. Thermostat has an installed 90-degree MALE -16 AN elbow and still requires its ordered straight female hose end. FRA-220116-BL order quantity 5 = three cooling + two oil suction. Do not reinstate removed SFL-SF92216BLK.
- **Main tank hanger plugs:** SUM-220228B-8 quantity 3 ordered, one for OUTLET2 on each hanger plus RETURN on the hanger not receiving surge overflow. Verify bare -8 ORB ports. SUM-220840B female -8 AN caps are alternatives only if leaving male AN adapters installed, not three more required closures.
- **Surge tank:** zero unused-port plugs in current plan. SUPPLY receives first lift; OUTLET2 is custom second lift inlet; OUTLET1 sends DW200 pressure feed; RETURN receives regulator bypass; OVERFLOW goes to one main tank. Preserve the custom-use/internal-passage verification.
- **Mallory regulator:** original fittings/plugs all lost. Two ordered SUM-220165B adapters cover upper inlet and lower bypass. SUM-220648B feeds rail from one 3/8 NPT regulated outlet; DER-98450 and Haltech kit use another; purchased EVIL ENERGY 3/8 NPT plug closes third. Second EVIL plug is spare.
- **Russell RUS-644123 rail adapter:** recorded user-installed; not a missing purchase.
- **Owned coolant parts:** expansion cap, all required hose clamps, front 35 mm silicone elbows, Aeroflow barb adapters and welded ACE hardline bungs. Verify radiator neck size against the 35 mm elbows.
- **Fuel tanks:** crossover bungs already welded; both AC PERFORMANCE hangers owned. Do not purchase those again.
- **Oil cooler adapters:** two EVIL ENERGY M22x1.5 to -12 AN adapters recorded owned. Dailey filter mount adapters supplied/owned. WIX-57045 filter owned.
- **Brake supplies ordered:** two ten-packs OPS-F208 = 20 nuts for 16 required; one RUS-R49005 ten-pack = eight washers required; four WIL-220-6890 transitions; one four-tab pack AAF-ALL60030; four WIL-300-15780 clips. Clutch SUM-770945-KIT supplies two transitions; use one in current route.
- **Hoses:** selected main-system hose SKUs and hose-end quantities match the checked order, apart from conditional adapter items above and the later-added vent circuits. Rigid tubing is TWO 25-foot coils (50 ft total); route lengths remain to be measured.

## Engineering decisions to preserve

1. **Brake masters:** Tilton's [76-series product documentation](https://tiltonracing.com/product/76-series-master-cylinders/) says not designed for ABS. Existing front/rear are 76-700 and 76-750. Final master selection, bore, mounting and adapters remain unresolved. Do not silently select replacements or label candidate adapters fit-confirmed.
2. **Clutch:** Wilwood 260-1333 pull slave; current route is master adapter -> 3/16-inch SAE double-flare hardline -> chassis transition -> 12-inch -3 AN flex hose -> slave adapter. Keep the flex section. Confirm actual inlet and master bore.
3. **Expansion overflow:** SUM-221002 (1/8-27 male NPT to 5/16 barb) was ordered. Owner measured original brass thread large end approximately 3/8 inch. This did not verify pitch; retain the thread check.
4. **Oil suction:** 35-inch -16 run; current Fragola hose record lists 28 inHg vacuum and 5.5-inch minimum bend radius. Installed hot-oil suction routing still needs review against Dailey requirements.
5. **Fuel balance and surge:** preserve verification of internal OUTLET2 passage, submerged hoses, overflow capacity and two-tank balance. No port/function swapping without tracing actual hardware.

## Printed installation guide

[Whole-car fitting installation checklist](whole-car-fitting-installation-checklist.pdf) is US Letter with route IDs, part numbers, sizes/angles, cut or finished hose lengths, checkboxes and note space. It is refreshed for F10/F11 and the confirmed Haltech sensor purchase. It is an installation reference, not proof every item was ordered.

The owner's annotated fitting and hose-length worksheets were already incorporated into the schematic. The originals remain private; do not upload them or raw receipt PDFs to the public site without reviewing personal information.

## How to continue

- Use the supplemental purchase table for newly ordered master inlets, FRA-650205 adapters, slave adapter and hanger RETURN adapter. Check delivery and physical fit separately. Continue with remaining outstanding items.
- Resolve the ABS master decision before completing related purchases/fabrication.
- Verify purchase/receipt of the newly added vent parts with the owner or purchase records.
- Update chain metadata, parts rows and issue text together when facts change. Legacy `Buy` / `Proposed` entries in `index.html` are selection statuses, not a synchronized purchasing ledger; reconcile against this audit/CSV.
- Preserve current hose angles and lengths from the filled worksheets unless the owner changes them. Do not assume cut lengths are complete hose assembly lengths.
- Parse the embedded scripts and check affected circuit/parts views before publication. Use a fresh remote head and a non-forced update so concurrent changes are preserved.
