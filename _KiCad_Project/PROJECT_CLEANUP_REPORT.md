# BitaxeFluxAstra A1 — Project Cleanup Report

**Status: cleanup completed and static equivalence checks passed; native KiCad 10 acceptance remains pending.**

This is a pre-layout engineering package. It is not a fabrication release. No placement or routing work was performed. Native project opening, ERC, DRC and a KiCad-exported netlist comparison could not be run because no KiCad executables are available in this environment. A package-manager attempt failed with environment permission errors. Existing source ERC reports were not reused as if they were new test results.

## Baseline selection and preservation

The supplied archive contains multiple nested copies. The selected editable project is the direct project in `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/` (path from archive root); its direct sheets were saved on 2026-09-23. The `hardware/` copies are earlier 2026-09-21 saves, and `.history/` is editor history. The old README points at the earlier hardware folder; the clean README points at the selected current project. See the historical appendix for exact member paths.

All **759 source files were compared byte-for-byte against their archive members** after cleanup. The supplied ZIP and extracted baseline remain untouched.

- Input ZIP SHA-256: `a735cc5ee31e274fe8488379b790a0efd272c18e271a2dd822a4154718339861`
- Selected baseline PCB SHA-256: `65ff76a477dff51094dd9466aada9637b2458c64a507adadf1922626c215d33f`
- Clean PCB SHA-256: `5b73895286a4ce40949bffcc5eb05519087e87d448c8a69d1bad19bc856a09ae`

The PCB file hash changes because library/file identifiers and embedded model metadata change. Physical objects do not change.

## Removed legacy files

**706 source files are omitted; 53 source files are retained or migrated.** No input file was destroyed. The complete per-file deletion inventory, reasons and exact old-to-new names are the historical appendix **[engineering_reference_notes.md](engineering_reference_notes.md)**, which is part of this report. Historical names appear only in that file.

Removed categories: redundant nested project/repository trees; older hardware snapshots; editor history and session preferences; the nested old ZIP; previous ERC/netlist/CSV closure reports; stale schematic SVG previews; old checksums and README copies; the unused original symbol collection; unreferenced footprints; and unused/duplicate 3D models. No current component, symbol pin, board footprint or required library asset was removed.

The current dependency union includes both the schematic and the placed board. A part used only by the preserved board remains available. The original licence is retained unchanged in `LICENSE`.

## Renamed and migrated items

| Old item (exact historical names in appendix) | New item | Type | Notes |
|---|---|---|---|
| Source project basename | `BitaxeFluxAstra` | Project | Root file and all five sheet filenames updated together; instance project keys and sheet filename metadata updated. |
| Prior project symbol alias | `BitaxeFluxAstra` | Library | 48 used symbols, copied from matching embedded caches. |
| Legacy ASIC footprint identity | `BitaxeFluxAstra:BM1373` | Footprint | Schematic and placed A1 point to the same local identity. No geometry change. |
| Source ASIC model identity | `3d/BM1373.step` | 3D model | Product labels renamed; STEP geometric entities and transforms preserved. |
| Source custom footprint alias | `BitaxeFluxAstra.pretty/` | Library | Only 16 required custom entries retained. |
| Legacy worksheet filename | `BitaxeFluxAstra.kicad_wks` | Worksheet | Same local bytes and embedded payload. |
| Missing placed J1 library file | Local `Connector_AMASS` snapshot | Footprint | Recovered from the actual board instance, which has zero rotation; all local geometry retained. |

### A1 identification

| Field | Clean value |
|---|---|
| Reference | A1 |
| Value | BM1373 |
| PARTNO | BM1373 |
| Configuration | Mode 1 |
| Symbol | BitaxeFluxAstra:BM1373_mode1 |
| Footprint | BitaxeFluxAstra:BM1373 |

The visible ASIC note states **A1: Bitmain BM1373, Part Number: BM1373, Configuration: Mode 1**. Existing reference/value locations and property visibility are preserved. The symbol library default reference is corrected to A1 and its default footprint points to the local BM1373 item. No manufacturer ordering code was invented.

## Library migration and portability

- One local symbol library contains **48** used definitions; every library definition exactly matches its clean embedded schematic cache.
- **32** footprint files resolve through local `fp-lib-table` entries, including **16** project-specific footprints and **16** standard-library snapshots. No unused local footprint entry remains.
- J2's 30-pin symbol and FPC footprint, AP2502 symbol, XT30 schematic footprint, ASIC, regulators, oscillator, mounting footprint and existing board logo are retained.
- Ten referenced local 3D model files are included. Parent-directory paths now resolve inside `3d/`.
- J2's unavailable converter-specific WRL path now targets the supplied STEP also used by the placed board; its library model transform is unchanged. The previous source did not supply that WRL, so equivalence of the absent WRL mesh cannot be checked. This does not affect any pad/PCB geometry.
- The USB model variable now uses the KiCad 10 model directory. **Optional standard 3D models still use `${KICAD10_3DMODEL_DIR}` and require the normal KiCad 10 3D-model package.** No private repository/model path remains. These standard model files are not claimed to be bundled.
- Embedded inductor models and worksheet payloads resolve inside their owning documents. The ASIC model is now a local STEP and the obsolete embedded duplicate is removed.

No broad “Update PCB from Schematic” operation was performed. All UUID relationships remain unchanged. The inherited J1 board model is a scaled standard connector model; it has not been requalified or replaced. No heatsink/mounting geometry was changed.

## Electrical-equivalence check

**No electrical design changes found by structural comparison.** The following were compared before and after, with library/filename metadata excluded only where documented:

| Object | Before | After | Result |
|---|---:|---:|---|
| Physical schematic component references | 186 | 186 | Identical |
| All symbol instances, including power symbols | 215 | 215 | Identical placement, UUID, unit and connectivity |
| Wires | 862 | 862 | Byte-identical objects |
| Junctions | 216 | 216 | Byte-identical objects |
| Local labels | 222 | 222 | Byte-identical names and positions |
| Hierarchical labels | 38 | 38 | Byte-identical; sheet pins/UUIDs preserved |
| No-connect markers | 33 | 33 | Byte-identical |
| Native DNP components | 13 | 13 | Identical states |

All embedded symbol pin numbers, names, electrical types and pin geometry were compared and are unchanged, including every BM1373 Mode-1 pin. Component values, established purchasing fields, qualification notes and population properties are unchanged. No current net name was changed.

**This is not a KiCad-exported netlist comparison.** Exact connectivity-bearing source objects and pin models are preserved, but native netlist generation and ERC remain unrun. The old packaged netlist predates the selected save and was deliberately not treated as the current baseline netlist.

DNP references preserved: **C201, C202, D1, R27, R33, R35, R49, R50, R51, R52, R53, R54, R55**. In particular, R49 remains DNP; R33/R35 and D1 remain DNP; all unselected regulator programming/tuning resistors and USB tuning capacitors retain their states. Native board population attributes are also unchanged; the older PCB does not acquire the newer schematic components.

## PCB-equivalence check

**No physical PCB layout changes.** All footprint positions/rotations, pad definitions and non-metadata footprint objects were compared. Track, via, zone, setup, stackup, board drawing/outline and group objects are byte-identical.

| PCB item | Before | After | Changed |
|---|---:|---:|---:|
| Footprints | 173 | 173 | 0 moved, 0 rotated, 0 added/removed |
| Pad objects | 789 | 789 | 0 |
| Track segments | 981 | 981 | 0 |
| Vias | 306 | 306 | 0 |
| Zones, including existing fill data | 22 | 22 | 0; no refill |
| BM1373 pad objects | 156 | 156 | 0 |

| A1 placement | Before | After |
|---|---:|---:|
| X (mm) | 165.911041 | 165.911041 |
| Y (mm) | 103.476103 | 103.476103 |
| Rotation (degrees) | 90 | 90 |

A1 pad-object SHA-256 (identical before/after): `573ad74d2ad4e24457af6ff38c6f016a31dd9667be91502c2b72e2b767d92626`.

The library BM1373 pads, graphics, mask/paste/courtyard, jumper groups, text locations and origin are copied from the supplied footprint. Its reference/value wording is the only visible library text change. The placed PCB A1 pad blocks are byte-identical. ASIC STEP geometric entities are unchanged; only product identity strings differ.

**DRC was not run.** No layout issue was fixed or represented as fixed. The PCB remains the earlier snapshot and is not synchronized with the A1 schematic; pre-existing schematic/PCB differences are intentionally preserved.

## Remaining intentional HOLD / TBD items

These are carried forward from the supplied engineering register, not resolved or newly qualified by this cleanup.

| ID | Open qualification item |
|---|---|
| H01 | BM1373 nominal/max VCORE and maximum current remain unqualified. No values selected; R49 stays DNP. |
| H02 | U3 VSEL/MSEL1/ADRSEL codes, NVM, frequency, loop compensation, current limit and two-phase behavior require bench qualification. |
| H03 | BM1373 thermal absolute limit, diode calibration and R33/R35 hardware trip programming unqualified; independent shutdown is not certified. |
| H04 | USB firmware mode not established in supplied scaffold. USB_VBUS monitor required if self-powered TinyUSB Device mode is used; VBUS isolated from board rails. |
| H05 | J2 exact ordering suffix, mating side/orientation and mating display FPC are not established by the supplied evidence. |
| H06 | 12V maximum qualified input current and PSU transients unknown; protection ratings not selected. |
| H07 | BM1373 package tolerances, height/clamp limits and final via-in-pad manufacturing process unqualified. |
| H08 | U8 exact oscillator ordering suffix, 1.2V operation/enable thresholds and package must be supplier-verified; source topology and metadata retained. |
| H09 | C104/C106 purchasing MPNs TBD / QUALIFY; values retained. C93 2.2nF C0G/NP0 purchasing MPN and C201/C202 tuning values remain unselected. |
| H10 | PCB is the untouched A0 snapshot. It does not implement A1 wiring, new components or corrected schematic footprint assignments; future PCB change and DRC/DFM are outside this task. |
| H11 | Firmware must remap SMBus to GPIO12/GPIO14, mask unused diode 2, preserve LCD strap levels, and qualify fan/diode/PMBus/boot/brownout faults. |
| H12 | D1 clamp voltage, leakage, pull-up behavior and U3/U7 enable-low margin over temperature and supply sequencing require first-article tests. No qualified thermal shutdown claim. |

The selected save's actual native DNP states and properties are authoritative. This cleanup does not certify first-article operation, thermal shutdown, power qualification, footprint suitability, or manufacturing readiness.

## Legacy full-text search

Recursive case-insensitive search covered filenames and all retained file text, including local STEP content. No unintended legacy ASIC or dual-device identity remains outside the single historical appendix. Existing `GND_1` substring hits are symbol-unit identifiers and valid ground pin-function names, not an obsolete second-ASIC net. They are retained to preserve the approved pin model. The detailed classification is in the appendix and current validation JSON.

## Reopened archive and acceptance status

The final ZIP was extracted into a separate verification folder. All file hashes were checked against the delivery folder, all KiCad S-expressions and project JSON were parsed again, the hierarchy was traversed, all used symbols/footprints were resolved through the extracted folder's local tables, and all local/embedded models were checked using only the extracted tree. Static equivalence checks were repeated against the untouched baseline.

This is an extracted-file structural reopen, **not a native KiCad GUI reopen**. No native-open, missing-library/rescue-warning, ERC or DRC result is claimed.

| Acceptance criterion | Status |
|---|---|
| Normal native KiCad 10 project/sheet/PCB opening | Pending — KiCad unavailable |
| No original repository dependency | Verified for schematic/footprint/local-model references |
| No missing custom symbols/footprints | Verified by local-table resolution and embedded-cache comparison |
| Consistent BM1373 identity; no misleading active legacy naming | Verified by recursive text/filename search |
| BM1373 pin numbers and electrical model preserved | Verified structurally |
| ASIC/PCB geometry, routing, zones and placement preserved | Verified structurally and by raw object equality |
| DNP states preserved | Verified for every schematic/PCB instance |
| Electrical connectivity unchanged | Structural equivalence verified; native netlist/ERC pending |
| Diagnostic DRC | Pending — not run |
| Full requested native acceptance | **Not yet demonstrated** |

The engineering reviewer should open `BitaxeFluxAstra.kicad_pro` in KiCad 10, inspect the root/four child sheets and PCB, run ERC, export/compare the native netlist, and run diagnostic DRC without zone refill or automatic repair. Preserve the existing schematic/PCB mismatch; do not automatically update the board. Stop at review; placement/routing is a separate task.

## Current symbol inventory

| Local symbol | Retained role |
|---|---|
| `+3V3_1_4a8ce9bd` | Approved project-local variant |
| `AP2502KTR-G1_501396a2` | U16 custom LED-driver symbol |
| `BAT54H_3eecedd5` | Approved project-local variant |
| `BM1373_mode1` | A1; exact Mode-1 pin map retained |
| `C_Polarized_Small_US_0a906312` | Approved project-local variant |
| `C_Small_05a2ad5e` | Approved project-local variant |
| `C_Small_1d832353` | Approved project-local variant |
| `C_Small_26bf1302` | Approved project-local variant |
| `C_Small_6415990f` | Approved project-local variant |
| `C_Small_6d3a2d65` | Approved project-local variant |
| `C_Small_6dda5bbf` | Approved project-local variant |
| `C_Small_7149b9df` | Approved project-local variant |
| `C_Small_746b5b1c` | Approved project-local variant |
| `C_Small_ab69a06d` | Approved project-local variant |
| `C_Small_bfc2077b` | Approved project-local variant |
| `C_Small_da46732c` | Approved project-local variant |
| `C_Small_e09e0ac2` | Approved project-local variant |
| `Conn_01x04_f305e5a2` | Approved project-local variant |
| `EMC2103_2_f5f07b60` | Approved project-local variant |
| `ESP32-S3-WROOM-1_bcc56e3b` | Approved project-local variant |
| `FerriteBead_50455155` | Approved project-local variant |
| `Fiducial_06a9f6a5` | Approved project-local variant |
| `GND` | Approved project-local variant |
| `GND_b3452fd5` | Approved project-local variant |
| `L_Small_4423e163` | Approved project-local variant |
| `L_c4afdae2` | Approved project-local variant |
| `MountingHole_Pad_2742ec7e` | Approved project-local variant |
| `NetTie_2_a7774715` | Approved project-local variant |
| `PWR_FLAG_5a7055e8` | Approved project-local variant |
| `PWR_FLAG_e7a8bcd3` | Approved project-local variant |
| `R_Small_US_5a0d14d3` | Approved project-local variant |
| `R_Small_US_77e2ba1b` | Approved project-local variant |
| `R_Small_US_ac7390c4` | Approved project-local variant |
| `R_US_b492dec7` | Approved project-local variant |
| `SFV30R-4STE1HLF_dd8c751a` | J2 project-specific 30-pin connector; qualification HOLD retained |
| `SN74AXC4T774PWR_339f628c` | Approved project-local variant |
| `SPST_NO_SW1_4cae15c7` | Approved project-local variant |
| `SPST_NO_SW2_4cae15c7` | Approved project-local variant |
| `TLV73312PDBV_cb346ca4` | Approved project-local variant |
| `TPS546D24S_ExtBias_U3_fe7e355b` | Approved project-local variant |
| `TPS546D24S_ExtBias_U7_fe7e355b` | Approved project-local variant |
| `TPS62933DRLR_1846fcf8` | Approved project-local variant |
| `TestPoint_70911f53` | Approved project-local variant |
| `TestPoint_c9ad6009` | Approved project-local variant |
| `USB_C_Receptacle_USB2.0_102fa207` | Approved project-local variant |
| `VDD_10804a59` | Approved project-local variant |
| `XT30PW-M_5db9d50c` | J1 schematic symbol; four-pad schematic footprint assignment retained |
| `oscillator_ffdd0242` | Approved project-local variant |
