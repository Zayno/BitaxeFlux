# BitaxeFluxAstra A1 — Clean Engineering Project

Open `BitaxeFluxAstra.kicad_pro` in **KiCad 10**. All five editable sheets, the preserved board and all used symbol/footprint libraries are included.

This package is for **pre-layout engineering review**. The PCB remains the earlier snapshot; it does not implement all A1 schematic changes. Do not manufacture this board from this package or automatically update it from the schematic as part of cleanup.

The ASIC is **Bitmain BM1373**, reference **A1**, configuration **Mode 1**. Its local symbol is `BitaxeFluxAstra:BM1373_mode1` and its footprint is `BitaxeFluxAstra:BM1373`.

R49 remains DNP. Unqualified thermal-shutdown and optional programming/tuning parts retain their DNP states. Qualification HOLD items remain open.

Read `PROJECT_CLEANUP_REPORT.md` for verification, preserved HOLD items and limitations. Exact historical file/migration names are isolated in `engineering_reference_notes.md`. `BitaxeFluxAstra_Integrity.json` records current structural verification. `SHA256SUMS.txt` covers delivery files except itself.

Static equivalence and extracted-package dependency checks passed. **Native KiCad opening, ERC, DRC and exported-netlist comparison have not been run** in this environment. Full acceptance remains pending that review. Optional standard 3D models use the normal KiCad 10 3D-model package; every required custom model is local or embedded.

No placement, routing or fabrication outputs are included. The supplied licence is preserved in `LICENSE`.
