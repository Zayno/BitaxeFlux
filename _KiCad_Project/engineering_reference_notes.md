# Engineering reference notes — historical source ledger

This is the single historical/provenance appendix to PROJECT_CLEANUP_REPORT.md. It is not an assembly guide, BOM, manufacturing release, or a statement that old names describe the current hardware. Old names below identify source archive members only.

The BM1373 symbol/footprint originated from community reference designs and was subsequently adapted for BitaxeFluxAstra. This cleanup preserves the supplied mapping and geometry; it does not independently qualify that adaptation. The source schematic note attributed the geometry to Naja Duo c095459.

## Exact migration ledger

| Old Name | New Name | Type | Notes |
|---|---|---|---|
| Flux_A1:BM1373_mode1 | BitaxeFluxAstra:BM1373_mode1 | Symbol | All 32 pin definitions, including types/numbers/names, preserved. |
| BM1340_mode0 / BM1340_mode1 in unused bitaxe.kicad_sym | Removed unused definitions | Symbols | Neither is referenced by the active schematic. |
| bitaxe:BM1340; BM1340.kicad_mod; legacy default A2 / BM1340_mode1 | BitaxeFluxAstra:BM1373; BM1373.kicad_mod; A1 / BM1373 | ASIC footprint | Both schematic assignment and PCB library identity migrated. All 156 pad objects preserved. |
| BM1340.step (embedded and external product identity) | 3d/BM1373.step | Model | Same STEP entities; only two PRODUCT name strings changed. Model transform unchanged. Old embedded records removed as redundant metadata. |
| BitaxeNajaDuo.kicad_sch PCB sheet metadata | BitaxeFluxAstra.kicad_sch | PCB metadata | Stale sheet filename corrected; UUIDs and pad nets unchanged. |
| BitaxeNajaDuo.step remembered export filename | BitaxeFluxAstra.step | Project setting | No STEP board export was generated. |
| Naja Duo c095459 schematic provenance note | BM1373 identification note; provenance in this file | Documentation | Electrical and thermal qualification warning retained. |
| bitaxe.kicad_wks | BitaxeFluxAstra.kicad_wks | Worksheet | Local bytes and embedded payload unchanged; embedded registry label and project path renamed. |
| Flux_A1.kicad_sym; Flux_A1 library alias | BitaxeFluxAstra.kicad_sym; BitaxeFluxAstra | Symbol library | Exactly the 48 used embedded definitions. |

## Schematic and footprint migrations

| Old Name | New Name | Type | Notes |
|---|---|---|---|
| `BitaxeFlux.kicad_sch` | `BitaxeFluxAstra.kicad_sch` | Schematic | Sheet UUIDs, symbol UUIDs, pin mapping and all electrical objects preserved. |
| `ASIC.kicad_sch` | `BitaxeFluxAstra_ASIC.kicad_sch` | Schematic | Sheet UUIDs, symbol UUIDs, pin mapping and all electrical objects preserved. |
| `ESP32.kicad_sch` | `BitaxeFluxAstra_ESP32.kicad_sch` | Schematic | Sheet UUIDs, symbol UUIDs, pin mapping and all electrical objects preserved. |
| `Power.kicad_sch` | `BitaxeFluxAstra_Power.kicad_sch` | Schematic | Sheet UUIDs, symbol UUIDs, pin mapping and all electrical objects preserved. |
| `fan.kicad_sch` | `BitaxeFluxAstra_fan.kicad_sch` | Schematic | Sheet UUIDs, symbol UUIDs, pin mapping and all electrical objects preserved. |
| `bitaxe:470531000` | `BitaxeFluxAstra:470531000` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:BM1340` | `BitaxeFluxAstra:BM1373` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:bitaxe_logo_small` | `BitaxeFluxAstra:BitaxeFluxAstra_logo_small` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:ESP32-S3-WROOM-1` | `BitaxeFluxAstra:ESP32-S3-WROOM-1` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20` | `BitaxeFluxAstra:FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:IND-SMD_L2.0-W1.6` | `BitaxeFluxAstra:IND-SMD_L2.0-W1.6` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:Inherited_Unqualified_CPU_Mount` | `BitaxeFluxAstra:Inherited_Unqualified_CPU_Mount` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:LQFN40-CLIP` | `BitaxeFluxAstra:LQFN40-CLIP` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:NetTie-2_SMD_Pad0.2mmx1mm` | `BitaxeFluxAstra:NetTie-2_SMD_Pad0.2mmx1mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:SLC1175-271MEC_COC` | `BitaxeFluxAstra:SLC1175-271MEC_COC` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:SMD3225-4P` | `BitaxeFluxAstra:SMD3225-4P` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR` | `BitaxeFluxAstra:SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:SW_CS1213AGF260_CRS` | `BitaxeFluxAstra:SW_CS1213AGF260_CRS` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:TestPoint_Pad_1.0x0.4mm` | `BitaxeFluxAstra:TestPoint_Pad_1.0x0.4mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:USB_C_Receptacle_GCT_USB4105-xx-A` | `BitaxeFluxAstra:USB_C_Receptacle_GCT_USB4105-xx-A` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `bitaxe:XT30PW-M` | `BitaxeFluxAstra:XT30PW-M` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Capacitor_SMD:CP_Elec_6.3x5.9` | `Capacitor_SMD:CP_Elec_6.3x5.9` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Capacitor_SMD:C_0402_1005Metric` | `Capacitor_SMD:C_0402_1005Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Capacitor_SMD:C_0603_1608Metric` | `Capacitor_SMD:C_0603_1608Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Capacitor_SMD:C_0805_2012Metric` | `Capacitor_SMD:C_0805_2012Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Capacitor_SMD:C_1206_3216Metric` | `Capacitor_SMD:C_1206_3216Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Connector_AMASS:AMASS_XT30UPB-M_1x02_P5.0mm_Vertical` | `Connector_AMASS:AMASS_XT30UPB-M_1x02_P5.0mm_Vertical` | Footprint snapshot | Recovered from placed J1 at 0 degrees; copied all pads and graphics without geometry edits. Board remains untouched. |
| `Diode_SMD:D_SOD-123F` | `Diode_SMD:D_SOD-123F` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Fiducial:Fiducial_1mm_Mask2mm` | `Fiducial:Fiducial_1mm_Mask2mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `MountingHole:MountingHole_3.2mm_M3_Pad_Via` | `MountingHole:MountingHole_3.2mm_M3_Pad_Via` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Package_DFN_QFN:QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm` | `Package_DFN_QFN:QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Package_SO:TSSOP-16_4.4x5mm_P0.65mm` | `Package_SO:TSSOP-16_4.4x5mm_P0.65mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Package_TO_SOT_SMD:SOT-23-5` | `Package_TO_SOT_SMD:SOT-23-5` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Package_TO_SOT_SMD:SOT-23-6` | `Package_TO_SOT_SMD:SOT-23-6` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Resistor_SMD:R_0402_1005Metric` | `Resistor_SMD:R_0402_1005Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `Resistor_SMD:R_0805_2012Metric` | `Resistor_SMD:R_0805_2012Metric` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |
| `TestPoint:TestPoint_Pad_D1.0mm` | `TestPoint:TestPoint_Pad_D1.0mm` | Footprint | Pad/copper/mask/paste/courtyard and all origin geometry copied exactly; only name/path metadata changed. |

## Retained or migrated source members

53 source files supply the retained project, libraries, models, licence and worksheet. The recovered J1 footprint and current documentation are new derived files.

| Source path (relative to outer archive folder) | Clean destination / disposition |
|---|---|
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/470531000.stp` | `3d/470531000.stp` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM1340.step` | `3d/BM1373.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CS1213AG-tr.stp` | `3d/CS1213AG-tr.stp` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/ESP32-S3-WROOM-1-N8R2--3DModel-STEP-56544.STEP` | `3d/ESP32-S3-WROOM-1-N8R2--3DModel-STEP-56544.STEP` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.step` | `3d/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND-SMD_L2.0-W1.6-H1.1.step` | `3d/IND-SMD_L2.0-W1.6-H1.1.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.step` | `3d/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TPS546D24ARVFR.step` | `3d/TPS546D24ARVFR.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XT30PW-M.stp` | `3d/XT30PW-M.stp` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/oscillator3.2x2.5.step` | `3d/oscillator3.2x2.5.step` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/ASIC.kicad_sch` | `BitaxeFluxAstra_ASIC.kicad_sch` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/BitaxeFlux.kicad_pcb` | `BitaxeFluxAstra.kicad_pcb` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/BitaxeFlux.kicad_pro` | `BitaxeFluxAstra.kicad_pro` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/BitaxeFlux.kicad_sch` | `BitaxeFluxAstra.kicad_sch` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/ESP32.kicad_sch` | `BitaxeFluxAstra_ESP32.kicad_sch` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/Flux_A1.kicad_sym` | `BitaxeFluxAstra.kicad_sym (only current embedded definitions retained)` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/Power.kicad_sch` | `BitaxeFluxAstra_Power.kicad_sch` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.kicad_wks` | `BitaxeFluxAstra.kicad_wks` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/470531000.kicad_mod` | `BitaxeFluxAstra.pretty/470531000.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BM1340.kicad_mod` | `BitaxeFluxAstra.pretty/BM1373.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/ESP32-S3-WROOM-1.kicad_mod` | `BitaxeFluxAstra.pretty/ESP32-S3-WROOM-1.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.kicad_mod` | `BitaxeFluxAstra.pretty/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/IND-SMD_L2.0-W1.6.kicad_mod` | `BitaxeFluxAstra.pretty/IND-SMD_L2.0-W1.6.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Inherited_Unqualified_CPU_Mount.kicad_mod` | `BitaxeFluxAstra.pretty/Inherited_Unqualified_CPU_Mount.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/LQFN40-CLIP.kicad_mod` | `BitaxeFluxAstra.pretty/LQFN40-CLIP.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/NetTie-2_SMD_Pad0.2mmx1mm.kicad_mod` | `BitaxeFluxAstra.pretty/NetTie-2_SMD_Pad0.2mmx1mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SLC1175-271MEC_COC.kicad_mod` | `BitaxeFluxAstra.pretty/SLC1175-271MEC_COC.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SMD3225-4P.kicad_mod` | `BitaxeFluxAstra.pretty/SMD3225-4P.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.kicad_mod` | `BitaxeFluxAstra.pretty/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SW_CS1213AGF260_CRS.kicad_mod` | `BitaxeFluxAstra.pretty/SW_CS1213AGF260_CRS.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TestPoint_Pad_1.0x0.4mm.kicad_mod` | `BitaxeFluxAstra.pretty/TestPoint_Pad_1.0x0.4mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/USB_C_Receptacle_GCT_USB4105-xx-A.kicad_mod` | `BitaxeFluxAstra.pretty/USB_C_Receptacle_GCT_USB4105-xx-A.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/XT30PW-M.kicad_mod` | `BitaxeFluxAstra.pretty/XT30PW-M.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/bitaxe_logo_small.kicad_mod` | `BitaxeFluxAstra.pretty/BitaxeFluxAstra_logo_small.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/fan.kicad_sch` | `BitaxeFluxAstra_fan.kicad_sch` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Capacitor_SMD.pretty/CP_Elec_6.3x5.9.kicad_mod` | `footprints/Capacitor_SMD.pretty/CP_Elec_6.3x5.9.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Capacitor_SMD.pretty/C_0402_1005Metric.kicad_mod` | `footprints/Capacitor_SMD.pretty/C_0402_1005Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Capacitor_SMD.pretty/C_0603_1608Metric.kicad_mod` | `footprints/Capacitor_SMD.pretty/C_0603_1608Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Capacitor_SMD.pretty/C_0805_2012Metric.kicad_mod` | `footprints/Capacitor_SMD.pretty/C_0805_2012Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Capacitor_SMD.pretty/C_1206_3216Metric.kicad_mod` | `footprints/Capacitor_SMD.pretty/C_1206_3216Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Diode_SMD.pretty/D_SOD-123F.kicad_mod` | `footprints/Diode_SMD.pretty/D_SOD-123F.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Fiducial.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | `footprints/Fiducial.pretty/Fiducial_1mm_Mask2mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/MountingHole.pretty/MountingHole_3.2mm_M3_Pad_Via.kicad_mod` | `footprints/MountingHole.pretty/MountingHole_3.2mm_M3_Pad_Via.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Package_DFN_QFN.pretty/QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm.kicad_mod` | `footprints/Package_DFN_QFN.pretty/QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Package_SO.pretty/TSSOP-16_4.4x5mm_P0.65mm.kicad_mod` | `footprints/Package_SO.pretty/TSSOP-16_4.4x5mm_P0.65mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Package_TO_SOT_SMD.pretty/SOT-23-5.kicad_mod` | `footprints/Package_TO_SOT_SMD.pretty/SOT-23-5.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Package_TO_SOT_SMD.pretty/SOT-23-6.kicad_mod` | `footprints/Package_TO_SOT_SMD.pretty/SOT-23-6.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Resistor_SMD.pretty/R_0402_1005Metric.kicad_mod` | `footprints/Resistor_SMD.pretty/R_0402_1005Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/Resistor_SMD.pretty/R_0805_2012Metric.kicad_mod` | `footprints/Resistor_SMD.pretty/R_0805_2012Metric.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/footprints/TestPoint.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | `footprints/TestPoint.pretty/TestPoint_Pad_D1.0mm.kicad_mod` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/fp-lib-table` | `fp-lib-table` |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/sym-lib-table` | `sym-lib-table` |
| `LICENSE` | `LICENSE` |

## Complete removed-file ledger

706 files are excluded from the clean deliverable. No source archive or extracted baseline file was deleted or changed. Current dependency tracing was performed before exclusion.

| Removed source path (relative to outer archive folder) | Why unnecessary in this deliverable |
|---|---|
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/141_TL3330AFxxxQG.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/21-0164B_L622-1_MXM.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/2R5TPE220MAFB.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/470531000.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/54-00164.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM04B-SRSS-TB.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM1340.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM1368xx.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BQB0016A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BitaxeGT_heatsink.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Bitaxe_Heatsink.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CS1213AG-tr.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-002AH.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-036AH-SMT-TR.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-037AH.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CX3225SB16000H0FLJCC.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Coilcraft-SLC1175.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Cree_PLCC6.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DCK0006A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DHVQFN14_SOT762-1_NEX.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DISST7789-176x320.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DQG0008A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DQH0008A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DRC0010J.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DRL0006A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/ESP32-S3-WROOM-1-N8R2--3DModel-STEP-56544.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FFC2B35-08-T.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FP1006V2-R.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FTSH-105-01-F-DV-K.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Fan 60x60x25mm.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/GDIM107050-R15S1MTF-0R37.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/GT heatsink.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IHLP2020CZ.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND-SMD_L11.0-W7.2-H7.5.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND-SMD_L2.0-W1.6-H1.1.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_-1R5MC_SUM.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_FP1107R1_EAT.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_SLC1175_COC.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/OLED_0.91_128x32.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/PLCC6_LED_3_5X3_4X2_8_CRW.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/QFN16_4X4_MCH.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SLC1175-271MEC_COC.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SMV_z90.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SN74AXC1T45DBVR.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SOT-23-5_M5_MCH.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/ST-4ETB2k_(202).stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SW_CS1213AGF260_CRS.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TENSILITY_54-00164.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TPS546D24ARVFR.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TPSM863257RDXR--3DModel-STEP-510211.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TSM-104-01-L-SH-A.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TSOT-23-5_RIT.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TXB0104RGYR.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TYPE-C-SMD_SBC-160S1A-20-S412.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/USB_10118193-0001LF.STEP` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/VSSOP-8_L2.0-W2.3-H0.9-LS3.1-P0.50.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XRCGB27M120F3M10R0_MUR.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XT30PW-M.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XTAL_SC32S-7PF20PPM_EPS.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/bm1370.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/c-63862-1-r-3d.stp` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/oscillator3.2x2.5.step` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A0_to_A1_Schematic_Changes.md` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A1_Net_Closure_Report.txt` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A1_Pin_Disposition_Report.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/ERC_A1_Report.txt` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/LICENSE` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/README.md` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/SHA256SUMS.txt` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/Schematic_Coverage_Ledger.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A0_14_Endpoint_Resolutions.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A0_Component_Snapshot.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A1_Netlist.xml` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Connectivity_Checks.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/ERC_A1_Report.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Footprint_Pin_Number_Audit.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Hierarchy_Port_Audit.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Intentional_Open_Nodes.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Original_Peer_Group_Differences.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Packaged_Project_Verification.txt` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Symbol_Library_Comparison.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Symbol_Pin_Model_Changes.csv` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/build_changes.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/new_references.json` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/ASIC.kicad_sch` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_pcb` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_prl` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_pro` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_sch` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/ESP32.kicad_sch` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/Flux_A1.kicad_sym` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/Power.kicad_sch` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.kicad_sym` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.kicad_wks` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/1366_logo.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/470531000.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/63862-1.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1340.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1366.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1368.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1370.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1397.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BQB0016A-MFG.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BarrelJack_Wuerth_694106106102_2.0x5.5mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CAP_2R5TPE220MAFB.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CLX6E-FKC-CH1M1D1BB7C3D3.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CSD17311Q5.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CUI_PJ-037AH.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/DCK0006A_N.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/DHVQFN14_SOT762-1_NEX.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/ESP32-S3-WROOM-1.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1005R1-R15-R.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1107R1-R23-R.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1107R1.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FTSH-105-01-F-DV-K.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/GDIM107050-R15S1MTF-0R37.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Heatsink-5hole-BitaxeGT.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Heatsink-BitaxeGT.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/IND-SMD_L11.0-W7.2.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/IND-SMD_L2.0-W1.6.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Inductor-74438357082.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Inherited_Unqualified_CPU_Mount.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/JST_SH_BM04B-SRSS-TB_1x04-1MP_P1.00mm_Vertical.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/LQFN40-CLIP.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/L_Coilcraft_SLC1175.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/NetTie-0.25mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/NetTie-2_SMD_Pad0.2mmx1mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/PinHeader_1x04_P2.54mm_Vertical_shifted.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/RT9080-33GJ5.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/RVF0040A.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SAMTEC_TSM-104-01-L-SH-A.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SC32S-7PF20PPM.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SLC1175-271MEC_COC.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SMD3225-4P.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SN74AXC1T45.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SOT-23-5.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/ST7789-176x320.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SW_CS1213AGF260_CRS.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SW_TL3330AF130QG_EWI.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ_nopaste.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TENSILITY_54-00164.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TPS40305.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TPSM863257RDX.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TXB0104.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Tag-Connect_TC2030-IDC-NL_2x03_P1.27mm_Vertical.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TestPoint_Pad_1.0x0.4mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/USB_10118193-0001LF_AMP.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/USB_C_Receptacle_GCT_USB4105-xx-A.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/XT30PW-M.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/bitaxe_logo_small.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/logo-fcu.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/logo.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/polarity.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/fan.kicad_sch` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/CP_Elec_6.3x5.9.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0402_1005Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0603_1608Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0805_2012Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_1206_3216Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Diode_SMD.pretty/D_SOD-123F.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Fiducial.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/MountingHole.pretty/MountingHole_3.2mm_M3_Pad_Via.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_DFN_QFN.pretty/QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_SO.pretty/TSSOP-16_4.4x5mm_P0.65mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-5.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-6.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Resistor_SMD.pretty/R_0402_1005Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Resistor_SMD.pretty/R_0805_2012Metric.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/TestPoint.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/fp-lib-table` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/sym-lib-table` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-ASIC.svg` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-ESP32.svg` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-Power.svg` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-fan.svg` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `1BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux.svg` | Redundant archived package tree; current dependencies copied from the selected active tree. |
| `3d/141_TL3330AFxxxQG.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/21-0164B_L622-1_MXM.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/2R5TPE220MAFB.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/470531000.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/54-00164.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/BM04B-SRSS-TB.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/BM1340.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/BM1368xx.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/BQB0016A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/BitaxeGT_heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/Bitaxe_Heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/CS1213AG-tr.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/CUI_DEVICES_PJ-002AH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/CUI_DEVICES_PJ-036AH-SMT-TR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/CUI_DEVICES_PJ-037AH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/CX3225SB16000H0FLJCC.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/Coilcraft-SLC1175.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/Cree_PLCC6.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DCK0006A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DHVQFN14_SOT762-1_NEX.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DISST7789-176x320.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DQG0008A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DQH0008A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DRC0010J.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/DRL0006A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/ESP32-S3-WROOM-1-N8R2--3DModel-STEP-56544.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/FFC2B35-08-T.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/FP1006V2-R.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/FTSH-105-01-F-DV-K.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/Fan 60x60x25mm.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/GDIM107050-R15S1MTF-0R37.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/GT heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IHLP2020CZ.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IND-SMD_L11.0-W7.2-H7.5.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IND-SMD_L2.0-W1.6-H1.1.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IND_-1R5MC_SUM.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IND_FP1107R1_EAT.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/IND_SLC1175_COC.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/OLED_0.91_128x32.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/PLCC6_LED_3_5X3_4X2_8_CRW.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/QFN16_4X4_MCH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SLC1175-271MEC_COC.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SMV_z90.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SN74AXC1T45DBVR.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SOT-23-5_M5_MCH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/ST-4ETB2k_(202).stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/SW_CS1213AGF260_CRS.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TENSILITY_54-00164.kicad_mod` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TPS546D24ARVFR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TPSM863257RDXR--3DModel-STEP-510211.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TSM-104-01-L-SH-A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TSOT-23-5_RIT.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TXB0104RGYR.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/TYPE-C-SMD_SBC-160S1A-20-S412.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/USB_10118193-0001LF.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/VSSOP-8_L2.0-W2.3-H0.9-LS3.1-P0.50.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/XRCGB27M120F3M10R0_MUR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/XT30PW-M.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/XTAL_SC32S-7PF20PPM_EPS.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/bm1370.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/c-63862-1-r-3d.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `3d/oscillator3.2x2.5.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `A0_to_A1_Schematic_Changes.md` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `A1_Net_Closure_Report.txt` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `A1_Pin_Disposition_Report.csv` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/HEAD` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/config` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/description` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/hooks/README.sample` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/index` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/info/exclude` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/logs/HEAD` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/logs/refs/heads/master` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/00/0481f6ab05bc55f9f78b3b8b307d4a1b303c81` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/00/76b9273966237ee3dbd82188f6b1f1d3352297` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/00/87a0021b44ce28766e960148d9ea2c6bf3b41b` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/01/e043ff3978166813e8ff7d2945410e23efc848` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/03/5b5bfc83222bdc7550a2a1ec55e342aa22fab1` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/03/661d04b9d7909e85e6fc81f79eb36bcc6b67da` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/07/4e34dd600f0339f339b981327c3ecd8780e4aa` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/0b/b1f0d25393a4cad5998f7feee28d62118f0f08` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/0f/1cf48ccf145c8cdcdc344d53ad198d0032fbfd` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/0f/68b23c91fa49e4ee74ef33577d768f2b3eff1f` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/12/a8aed981bdb31b4670fcc3861e8d4207e86692` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/14/67e91b623ef8b712970486961e77b9a88d8691` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/14/e5e0978b9da6c7d02d9d4339dbb75b1443338a` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/18/27cab4deb254fd87700b229e6c263eda9644bd` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/21/7181f2b4e1dacd62732c30ce9bff5da2f3150b` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/22/065cd6dd0f01781232f6a5664bddec43c9eaa9` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/23/a40464d84695fe2ffb434f58697ee48969fb52` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/29/1b9615b3c3fa89b2909e739baa70e6725a0188` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/2a/6fa3dcdd3a4dab11a933c6a3918b035c29540d` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/2c/ed9d39181d8200bd17faceff4d1a1e762d5a08` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/34/70f2ebfa3835a8b9719a4cbf490f267637ced7` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/38/5c0cffb22d952cc53461fb5ff5e1e3f0cfef0d` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/3e/328bdfa2f967121d026f20ddf7338882927671` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/3e/71130b2772b0a4009d4ebd88a5e47e8def575e` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/3f/c38543790b2da1cb6036e39604143b2a56c0e1` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/40/97a8b295d5fcd3ba5b3d97c5a2a1b746c45725` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/53/549823250a82b2b16af73d19c0b46c95094a36` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/56/54bb09d7632ce004b8d33fad6cf6911bd92769` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/59/c2a4979eabe06917d71464043ce522a371b80c` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/5b/38aaebabc9defa6d78c199351a8db0ca2c2520` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/5f/29a4f9a8361b7a9653633ef59a71cace713a7a` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/5f/6e159293c076de99fb411e00aeb65a3063ef77` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/67/c15d430957582923a6bd831d085d3a0ea5e676` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/6b/9e4b688ee9bb6a65d914da4fb69a58c43d3571` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/6e/e6a5c9119c35a42238ab57f34b6d19c52f0fbd` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/70/d7404a8c6da75a97c39bbe3bb7eb3f15afcf66` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/72/53fab0a7fbcea5b7cc900ac4da9415d4f75d30` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/79/5c6331ea0b2674c6d2c402da65aa6eba6b5c1d` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/7f/ccbbf3569b87635725f8eb764c0fc4fc162875` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/81/c1fb5dd208e8294defd99d6fc97db4750b7de2` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/83/5f0011cb5207081c6323378d15e85cc17620c5` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/84/6a59ce8f6f94866d667bd7f943991017454282` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/85/172a241029b8b059a08a7226e775fc15290cc5` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/94/10a6c49d04161ca3e4e7746790d2dcbd1b5d37` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/99/8251f8e9c5262610cb09e359d8b45f279b84ec` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/9b/20d5bc1e980adf56c38266f141992628c6c5ea` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/9c/f431304b8a3402379751ede8d21df580fcb3ad` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/9d/0dbcd1f9866cf361d3e3dbb6adcddce662a8ae` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/9e/370cbd0ba3292081a3272b92f33ad3c03adc57` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/a0/7cdddef1e521cc1a10ae7517a878515e1c2a86` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/a6/f3788dd90e51b71ba9a1c9ab64f55f2a0d4dcb` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/ae/92b75d159d1d1ec2d528ba5ca6a909fce1684c` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/b2/2ecf9e1d9f429086095b60f9aae503e6c0f7dd` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/b7/22c727e772a8e546e1e3497c13d2ec3b5c0746` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/bc/1f149e798b5594d80e8094b55d52fe740f370d` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/bc/5a21394bd2fb98be538bcd5a3fcfc18a3f4424` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/bd/540da862972a1b9212cdbe5734cedc6f319dd5` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/bd/d0fb3eaabfe7d70eae57631ac03f45a84e9562` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/bf/275e575b507d65c3e79ce26b7e0ea2ea785f24` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/ca/02774d0e0a1b5e89f61d7ae507ab4684c07709` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/ca/2a810dd15d7bf75326b7e61543386a5081e339` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/cb/68c3c9cba3c34c1ad0ebd5c0a64dbdc920c5e6` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/d0/ba4a13b03d544470b2c78d43b7843cdb80c21f` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/d4/0e663391d4b974d937cbd843d2ce926b272cd9` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/d4/556afce474bcd718d1441de0bb3edb5220adce` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/da/5f7ffe906c6ee3940a5553c25871cd1a52419c` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/dc/15000f2c851414367517d1f0de878c0da0632a` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/e1/6bf601c0ee0981a4999d63d1259444a5b3e363` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/e2/290f66645857320cbd26b431c6be91f648dc4b` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/eb/6c0addcea25233947575a08e31f31c9b7e3003` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/ee/db70e8d5d98a8d1dd3af629467fd3a7665eaa0` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/f3/7d21ab818d76d33dca08cbf9e454a2b04593cf` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/f4/eb49f9ce243f9780eb96696e628be6bf491641` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/f9/d4b73917a32a9a36a85dbd8d21efecff1581d2` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/fe/66ab0e0d8c2530878a66c113dc8dde85e4d353` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/objects/fe/cf701e2e3455c2211b1a1a33c9590b18268b78` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/heads/master` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Last_Save_project` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Last_Save_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Save_project_1` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Save_sch_1` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Save_sch_2` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.git/refs/tags/Save_sch_3` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/.gitignore` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/ASIC.kicad_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/BitaxeFlux.kicad_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/ESP32.kicad_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/Power.kicad_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/README.txt` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/.history/fan.kicad_sch` | Editor history / redundant backup; not a current project dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/141_TL3330AFxxxQG.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/21-0164B_L622-1_MXM.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/2R5TPE220MAFB.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/54-00164.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM04B-SRSS-TB.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BM1368xx.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BQB0016A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/BitaxeGT_heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Bitaxe_Heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-002AH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-036AH-SMT-TR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CUI_DEVICES_PJ-037AH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/CX3225SB16000H0FLJCC.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Coilcraft-SLC1175.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Cree_PLCC6.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DCK0006A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DHVQFN14_SOT762-1_NEX.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DISST7789-176x320.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DQG0008A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DQH0008A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DRC0010J.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/DRL0006A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FFC2B35-08-T.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FP1006V2-R.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/FTSH-105-01-F-DV-K.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/Fan 60x60x25mm.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/GDIM107050-R15S1MTF-0R37.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/GT heatsink.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IHLP2020CZ.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND-SMD_L11.0-W7.2-H7.5.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_-1R5MC_SUM.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_FP1107R1_EAT.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/IND_SLC1175_COC.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/OLED_0.91_128x32.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/PLCC6_LED_3_5X3_4X2_8_CRW.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/QFN16_4X4_MCH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SLC1175-271MEC_COC.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SMV_z90.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SN74AXC1T45DBVR.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SOT-23-5_M5_MCH.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/ST-4ETB2k_(202).stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/SW_CS1213AGF260_CRS.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TENSILITY_54-00164.kicad_mod` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TPSM863257RDXR--3DModel-STEP-510211.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TSM-104-01-L-SH-A.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TSOT-23-5_RIT.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TXB0104RGYR.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/TYPE-C-SMD_SBC-160S1A-20-S412.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/USB_10118193-0001LF.STEP` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/VSSOP-8_L2.0-W2.3-H0.9-LS3.1-P0.50.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XRCGB27M120F3M10R0_MUR.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/XTAL_SC32S-7PF20PPM_EPS.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/bm1370.step` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/3d/c-63862-1-r-3d.stp` | Unreferenced or duplicate model; every current project-local model reference is resolved in the clean package. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A0_to_A1_Schematic_Changes.md` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A1_Net_Closure_Report.txt` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/A1_Pin_Disposition_Report.csv` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/BitaxeFlux.kicad_prl` | Machine/editor-local preference and session state; not a design dependency. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/ERC_A1_Report.txt` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/LICENSE` | Duplicate licence text; one unchanged root LICENSE retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/README.md` | Stale package instructions/checksums; replaced by current cleanup instructions and checksums. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/SHA256SUMS.txt` | Stale package instructions/checksums; replaced by current cleanup instructions and checksums. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/Schematic_Coverage_Ledger.csv` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A0_14_Endpoint_Resolutions.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A0_Component_Snapshot.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/A1_Netlist.xml` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Connectivity_Checks.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/ERC_A1_Report.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Footprint_Pin_Number_Audit.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Hierarchy_Port_Audit.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Intentional_Open_Nodes.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Original_Peer_Group_Differences.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Packaged_Project_Verification.txt` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Symbol_Library_Comparison.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/Symbol_Pin_Model_Changes.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/build_changes.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/audit/new_references.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.kicad_sym` | Unused legacy symbol collection; all 48 current embedded symbols migrated to the clean library. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/1366_logo.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/63862-1.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BM1366.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BM1368.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BM1370.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BM1397.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BQB0016A-MFG.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/BarrelJack_Wuerth_694106106102_2.0x5.5mm.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/CAP_2R5TPE220MAFB.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/CLX6E-FKC-CH1M1D1BB7C3D3.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/CSD17311Q5.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/CUI_PJ-037AH.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/DCK0006A_N.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/DHVQFN14_SOT762-1_NEX.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FP1005R1-R15-R.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FP1107R1-R23-R.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FP1107R1.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/FTSH-105-01-F-DV-K.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/GDIM107050-R15S1MTF-0R37.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Heatsink-5hole-BitaxeGT.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Heatsink-BitaxeGT.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/IND-SMD_L11.0-W7.2.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Inductor-74438357082.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/JST_SH_BM04B-SRSS-TB_1x04-1MP_P1.00mm_Vertical.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/L_Coilcraft_SLC1175.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/NetTie-0.25mm.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/PinHeader_1x04_P2.54mm_Vertical_shifted.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/RT9080-33GJ5.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/RVF0040A.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SAMTEC_TSM-104-01-L-SH-A.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SC32S-7PF20PPM.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SN74AXC1T45.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SOT-23-5.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/ST7789-176x320.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/SW_TL3330AF130QG_EWI.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Sinhoo SMTSO3015CTJ.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Sinhoo SMTSO3015CTJ_nopaste.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TENSILITY_54-00164.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TPS40305.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TPSM863257RDX.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TXB0104.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/Tag-Connect_TC2030-IDC-NL_2x03_P1.27mm_Vertical.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/USB_10118193-0001LF_AMP.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/logo-fcu.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/logo.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/bitaxe.pretty/polarity.kicad_mod` | Unreferenced or duplicate footprint; retained union includes both current schematic and placed PCB libraries. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/ASIC.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_pcb` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_prl` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_pro` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/BitaxeFlux.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/ESP32.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/Flux_A1.kicad_sym` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/Power.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.kicad_sym` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.kicad_wks` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/1366_logo.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/470531000.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/63862-1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1340.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1366.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1368.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1370.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BM1397.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BQB0016A-MFG.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/BarrelJack_Wuerth_694106106102_2.0x5.5mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CAP_2R5TPE220MAFB.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CLX6E-FKC-CH1M1D1BB7C3D3.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CSD17311Q5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/CUI_PJ-037AH.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/DCK0006A_N.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/DHVQFN14_SOT762-1_NEX.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/ESP32-S3-WROOM-1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1005R1-R15-R.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1107R1-R23-R.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FP1107R1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/FTSH-105-01-F-DV-K.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/GDIM107050-R15S1MTF-0R37.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Heatsink-5hole-BitaxeGT.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Heatsink-BitaxeGT.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/IND-SMD_L11.0-W7.2.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/IND-SMD_L2.0-W1.6.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Inductor-74438357082.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Inherited_Unqualified_CPU_Mount.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/JST_SH_BM04B-SRSS-TB_1x04-1MP_P1.00mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/LQFN40-CLIP.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/L_Coilcraft_SLC1175.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/NetTie-0.25mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/NetTie-2_SMD_Pad0.2mmx1mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/PinHeader_1x04_P2.54mm_Vertical_shifted.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/RT9080-33GJ5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/RVF0040A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SAMTEC_TSM-104-01-L-SH-A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SC32S-7PF20PPM.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SLC1175-271MEC_COC.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SMD3225-4P.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SN74AXC1T45.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SOT-23-5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/ST7789-176x320.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SW_CS1213AGF260_CRS.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/SW_TL3330AF130QG_EWI.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ_nopaste.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TENSILITY_54-00164.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TPS40305.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TPSM863257RDX.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TXB0104.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/Tag-Connect_TC2030-IDC-NL_2x03_P1.27mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TestPoint_Pad_1.0x0.4mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/USB_10118193-0001LF_AMP.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/USB_C_Receptacle_GCT_USB4105-xx-A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/XT30PW-M.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/bitaxe_logo_small.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/logo-fcu.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/logo.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/bitaxe.pretty/polarity.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/fan.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/CP_Elec_6.3x5.9.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0402_1005Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0603_1608Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_0805_2012Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Capacitor_SMD.pretty/C_1206_3216Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Diode_SMD.pretty/D_SOD-123F.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Fiducial.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/MountingHole.pretty/MountingHole_3.2mm_M3_Pad_Via.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_DFN_QFN.pretty/QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_SO.pretty/TSSOP-16_4.4x5mm_P0.65mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-6.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Resistor_SMD.pretty/R_0402_1005Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/Resistor_SMD.pretty/R_0805_2012Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/footprints/TestPoint.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/fp-lib-table` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/hardware/sym-lib-table` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/pdf/BitaxeFlux.pdf` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-ASIC.svg` | Stale rendered schematic export; current editable sheets retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-ESP32.svg` | Stale rendered schematic export; current editable sheets retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-Power.svg` | Stale rendered schematic export; current editable sheets retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux-fan.svg` | Stale rendered schematic export; current editable sheets retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED/schematic_previews/BitaxeFlux.svg` | Stale rendered schematic export; current editable sheets retained. |
| `BitaxeFluxAstra_A1_SCHEMATIC_CLOSED.zip` | Nested historical archive; not needed to open or edit the clean project. |
| `ERC_A1_Report.txt` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `README.md` | Stale package instructions/checksums; replaced by current cleanup instructions and checksums. |
| `SHA256SUMS.txt` | Stale package instructions/checksums; replaced by current cleanup instructions and checksums. |
| `Schematic_Coverage_Ledger.csv` | Historical closure report or redundant repository material; qualification holds transcribed into current report. |
| `audit/A0_14_Endpoint_Resolutions.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/A0_Component_Snapshot.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/A1_Netlist.xml` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Connectivity_Checks.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/ERC_A1_Report.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Footprint_Pin_Number_Audit.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Hierarchy_Port_Audit.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Intentional_Open_Nodes.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Original_Peer_Group_Differences.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Packaged_Project_Verification.txt` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Symbol_Library_Comparison.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/Symbol_Pin_Model_Changes.csv` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/build_changes.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `audit/new_references.json` | Previous revision audit/export; not evidence for this cleanup or selected current save. |
| `hardware/ASIC.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/BitaxeFlux.kicad_pcb` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/BitaxeFlux.kicad_prl` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/BitaxeFlux.kicad_pro` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/BitaxeFlux.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/ESP32.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/Flux_A1.kicad_sym` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/Power.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.kicad_sym` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.kicad_wks` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/1366_logo.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/470531000.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/63862-1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BM1340.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BM1366.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BM1368.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BM1370.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BM1397.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BQB0016A-MFG.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/BarrelJack_Wuerth_694106106102_2.0x5.5mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/CAP_2R5TPE220MAFB.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/CLX6E-FKC-CH1M1D1BB7C3D3.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/CSD17311Q5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/CUI_PJ-037AH.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/DCK0006A_N.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/DHVQFN14_SOT762-1_NEX.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/ESP32-S3-WROOM-1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FP1005R1-R15-R.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FP1107R1-R23-R.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FP1107R1.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FPC-SMD_30P-P0.50_XUNPU_FPC-05F-30PH20.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FPC-SMD_P0.50-8P_FGS-XJ-H2.0.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/FTSH-105-01-F-DV-K.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/GDIM107050-R15S1MTF-0R37.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Heatsink-5hole-BitaxeGT.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Heatsink-BitaxeGT.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/IND-SMD_L11.0-W7.2.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/IND-SMD_L2.0-W1.6.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Inductor-74438357082.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Inherited_Unqualified_CPU_Mount.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/JST_SH_BM04B-SRSS-TB_1x04-1MP_P1.00mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/LQFN40-CLIP.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/L_Coilcraft_SLC1175.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/NetTie-0.25mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/NetTie-2_SMD_Pad0.2mmx1mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/PAD-SMD_L5.0-W2.0_STHW4-DU-HN050206.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/PinHeader_1x04_P2.54mm_Vertical_shifted.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/RT9080-33GJ5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/RVF0040A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SAMTEC_TSM-104-01-L-SH-A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SC32S-7PF20PPM.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SLC1175-271MEC_COC.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SMD3225-4P.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SN74AXC1T45.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SOT-23-5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SOT-583-8_L2.1-W1.2-P0.50-LS1.6-BR.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/ST7789-176x320.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SW_CS1213AGF260_CRS.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/SW_TL3330AF130QG_EWI.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Sinhoo SMTSO3015CTJ_nopaste.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TENSILITY_54-00164.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TPS40305.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TPSM863257RDX.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TXB0104.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/Tag-Connect_TC2030-IDC-NL_2x03_P1.27mm_Vertical.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TestPoint_Pad_1.0x0.4mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/USB_10118193-0001LF_AMP.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/USB_C_Receptacle_GCT_USB4105-xx-A.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/XT30PW-M.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/bitaxe_logo_small.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/logo-fcu.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/logo.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/bitaxe.pretty/polarity.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/fan.kicad_sch` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Capacitor_SMD.pretty/CP_Elec_6.3x5.9.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Capacitor_SMD.pretty/C_0402_1005Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Capacitor_SMD.pretty/C_0603_1608Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Capacitor_SMD.pretty/C_0805_2012Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Capacitor_SMD.pretty/C_1206_3216Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Diode_SMD.pretty/D_SOD-123F.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Fiducial.pretty/Fiducial_1mm_Mask2mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/MountingHole.pretty/MountingHole_3.2mm_M3_Pad_Via.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Package_DFN_QFN.pretty/QFN-16-1EP_4x4mm_P0.65mm_EP2.1x2.1mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Package_SO.pretty/TSSOP-16_4.4x5mm_P0.65mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-5.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Package_TO_SOT_SMD.pretty/SOT-23-6.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Resistor_SMD.pretty/R_0402_1005Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/Resistor_SMD.pretty/R_0805_2012Metric.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/footprints/TestPoint.pretty/TestPoint_Pad_D1.0mm.kicad_mod` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/fp-lib-table` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `hardware/sym-lib-table` | Older hardware snapshot / duplicate repository; selected active project supersedes this copy. |
| `schematic_previews/BitaxeFlux-ASIC.svg` | Stale rendered schematic export; current editable sheets retained. |
| `schematic_previews/BitaxeFlux-ESP32.svg` | Stale rendered schematic export; current editable sheets retained. |
| `schematic_previews/BitaxeFlux-Power.svg` | Stale rendered schematic export; current editable sheets retained. |
| `schematic_previews/BitaxeFlux-fan.svg` | Stale rendered schematic export; current editable sheets retained. |
| `schematic_previews/BitaxeFlux.svg` | Stale rendered schematic export; current editable sheets retained. |

## Directory disposition

All obsolete repository and duplicate package directories disappear with their listed files. Project-local footprints and models are rebuilt from the referenced union; paths above show exactly which members remain. No input directory is required beside the clean folder.

## Intentional legacy-search results

All BM1340 / bm1340 / BM1340_mode0 / BM1340_mode1 / Naja Duo / naja-duo / NajaDuo results are historical names in this appendix. No such identities remain in the editable project, active libraries, clean model text or README. The exact filename and migration ledger is the reason for retaining these strings here.

GND_1 substring hits outside this file are legitimate symbol-unit and pin-function identifiers, including GND_1_1, GND_1 and PGND_13. They are not an obsolete second-ASIC ground net; none was renamed. No current net named 0V8_1 or 1V2_1 was found.
