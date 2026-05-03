# ⚗️ Batch Process Mass Balance & Enthalpy Balance — API Manufacturing

> Complete **material balance, enthalpy balance, and utility calculations** for a multi-step pharmaceutical batch manufacturing process involving cyanide reaction, layer separation, distillation, and crystallization.

---

## 📌 Overview

This project presents a full **batch process mass balance (H&MB)** for a pharmaceutical API manufacturing plant. The Excel workbook covers all unit operations across the entire batch cycle — from raw material charging to final crystallized product — including heat duty calculations and utility flow rate sizing.

| Parameter | Value |
|-----------|-------|
| Document type | Heat & Mass Balance (H&MB) |
| Process type | Multi-step Batch API Synthesis |
| Software | Microsoft Excel |
| Mass balance | ✅ Verified (Total IN = Total OUT = 26,744 kg) |

---

## 🔄 Process Overview

```
Raw Materials
(Hexane, MPBD, IN-1)
        ↓
[1] 6.3 KL GLR Pre-Mixer (PM-1402)
    Mixing at 8°C · BCT: 16.5 hrs
        ↓
[2] 10 KL SSR Reaction Reactors (R-1310 to R-1317)
    Cyanide Reaction + Layer Separation + Distillation · BCT: 171 hrs
        ↑
[3] 3 KL SSR Cyanide Reactor (R-1402)
    Sodium Cyanide solution preparation · BCT: 2.5 hrs
        ↓
[4] 6.3 KL GLR Crystallization (R-1212 / R-1213 / R-1214)
    Crystallization at low temperature · BCT: 31.3 hrs
        ↓
Final Product (Liquid Mass for Crystallization: 4,167 kg)
```

---

## 🏭 Equipment Summary

| Equipment | Tag No. | Capacity | MOC | BCT | Qty |
|-----------|---------|----------|-----|-----|-----|
| GLR Pre-Mixer | PM-1402 / PM-XXXX | 6.3 KL | MSGL | 16.5 hrs | 2 |
| Cyanide Reactor | R-1402 | 3.0 KL | SSR | 2.5 hrs | 1 |
| Reaction Reactor | R-1310 to R-1317 | 10.0 KL | SS316 | 171 hrs | 8 |
| Crystallization Reactor | R-1212 to R-1214 | 6.3 KL | GLR | 31.3 hrs | 3 |

---

## ⚖️ Overall Mass Balance (BFD Sheet)

**Total Input = Total Output = 26,744 kg** ✅

### Inputs to 10 KL SSR Reactors

| Material | Quantity (kg) |
|----------|--------------|
| Hexane (1st charge) | 3,500 |
| Water from Cyanide Reactor | 1,200 |
| Sodium Cyanide from R-1402 | 250 |
| SC | 21 |
| Cat-2 | 30 |
| 1st Water Wash | 500 |
| 2nd Water Wash (Hypo + Water) | 1,250 |
| 3rd Water Wash | 1,500 |
| 4th Water Wash (+ Acetic Acid) | 1,510 |
| IPA | 2,000 |
| Base-Liquid | 85 |
| CFG-2 Powder | 5 |
| 1st HCL + Water Lot | 260 |
| 2nd HCL + Water Lot | 260 |
| Hexane (2nd charge) | 2,800 |
| 3rd HCL + Water Lot | 260 |
| 5th Water Wash | 500 |
| 6th–10th Water Washes | 6,013 |
| **Total** | **~23,944** |

### Outputs

| Stream | Quantity (kg) | Destination |
|--------|--------------|-------------|
| Recover Solvent (ATM) | 2,000 | Solvent Recovery |
| Recover Solvent (Vacuum) | 1,100 | Solvent Recovery |
| Main Aq. Cyanide Layer | 2,000 | Hypo Treatment |
| 1st–4th Water Wash Aq. Layers | 6,610 | ETP |
| 5th–10th Water Wash Aq. Layers | 9,067 | ETP |
| **Liquid Mass for Crystallization** | **4,167** | **Next Step** |

---

## 📋 Mass Balance — Unit Operations (Sheet: xx)

### Unit 1 — 6.3 KL GLR Pre-Mixer (PM-1402)

| Step | Process Action | Material | Mass In (kg) | Mass Out (kg) | Temp | Utility |
|------|---------------|----------|-------------|--------------|------|---------|
| 1 | Receive Hexane from Day Tank | Hexane | 1,200 | 1,200 | 20–25°C | CHW |
| 2 | Charge MPBD under vacuum | MPBD | 875 | 2,075 | 20–25°C | CW/CHW |
| 3 | Charge IN-1 under vacuum | IN-1 | 1,225 | 3,300 | 20–25°C | CW/CHW |
| 4 | Apply brine, cool to 8°C | — | — | 3,300 | 8°C | CHW/CHB |
| 5 | Mix for 1 hr | — | — | 3,300 | 8°C | CHW/CHB |
| **Total** | | | **3,300** | **3,300** | | |

**Batch Cycle Time: 16.5 hrs · Pressure: FV to ATM · MOC: MSGL**

---

### Unit 2 — 3 KL SSR Cyanide Reactor (R-1402)

| Step | Process Action | Material | Mass In (kg) | Mass Out (kg) | Temp | Utility |
|------|---------------|----------|-------------|--------------|------|---------|
| 1 | Charge water | Water | 1,200 | 1,200 | 25–30°C | CW/CHW |
| 2 | Charge Sodium Cyanide under vacuum | NaCN | 250 | 1,450 | 25–30°C | CW/CHW |
| 3 | Mix for 1 hr | — | — | 1,450 | 25–30°C | CW/CHW |
| **Total** | | | **1,450** | **1,450** | | |

**Batch Cycle Time: 2.5 hrs · Pressure: ATM to Vacuum · RPM: 95**

---

### Unit 3 — 10 KL SSR Reactors (R-1310 to R-1317) — Selected Steps

| Step | Key Action | Mass Out (kg) | Temp | Utility |
|------|-----------|--------------|------|---------|
| 1 | Charge Hexane | 3,500 | 25–30°C | CW |
| 2 | Feed mixture from Cyanide Reactor | 4,700 | 25–30°C | CW |
| 5 | Cool to 24°C, start stirrer | 5,001 | 24°C | CHW |
| 6 | Slow addition of PM-1402 mixture (4 hrs) | 8,301 | 24°C | CHW |
| 9 | Increase to 40°C, settle | 8,301 | 40°C | Steam |
| 10 | Layer separation — Aq. to R-1215/R-1216 | 6,301 | 35–40°C | Steam/CW |
| 20 | Steam distillation, recover solvent (6 hrs) | 3,851 | 65°C | Steam/CW |
| 23 | Add 2000 kg IPA | 4,751 | 65°C | CW |
| 27 | Cool to 2°C, maintain 24 hrs | 4,841 | 2°C | CHB |
| 31–33 | HCL additions + Hexane charge | 8,161 | −10°C | CHB |
| 37 | Separate IPA + water layer → IPA Recovery | 5,921 | 33°C | CW/Steam |

**Batch Cycle Time: 171 hrs · Pressure: FV to ATM · MOC: SS316**

---

## 🌡️ Enthalpy Balance Summary (Sheet: Enthalpy Balance)

### 6.3 KL GLR Pre-Mixer — Chilling Water (Steps 1–3)

| Parameter | Value | Unit |
|-----------|-------|------|
| Process fluid volume | 6.3 | m³ |
| Mass of reaction material | 3,300 | kg |
| Avg. specific heat | 0.7 | kcal/kg·°C |
| Initial temperature | 30 | °C |
| Final temperature | 15 | °C |
| Thermodynamic heat | 34,650 | kcal |
| Overall HTC | 175 | kcal/hr·m²·°C |
| Effective HT area | 16.6 | m² |
| **Heat load** | **46,200** | **kcal/hr** |
| Min. chilling water flow | 14.2 | m³/hr |
| Calculated flow rate | 9.24 | m³/hr |
| Chilling time assumed | 45 | min |

### 6.3 KL GLR Pre-Mixer — Brine (Steps 4–5)

| Parameter | Value | Unit |
|-----------|-------|------|
| Mass of reaction material | 3,300 | kg |
| Initial temperature | 15 | °C |
| Final temperature | 8 | °C |
| Thermodynamic heat | 16,170 | kcal |
| Overall HTC | 150 | kcal/hr·m²·°C |
| **Heat load** | **48,510** | **kcal/hr** |
| Min. brine flow rate | 14.2 | m³/hr |
| Calculated flow rate | 9.702 | m³/hr |
| Brine time assumed | 20 | min |

### 3 KL SSR Cyanide Reactor — Chilling Water (Steps 1–3)

| Parameter | Value | Unit |
|-----------|-------|------|
| Process fluid volume | 3.0 | m³ |
| Mass of reaction material | 1,450 | kg |
| Initial temperature | 30 | °C |
| Final temperature | 25 | °C |
| Thermodynamic heat | 5,075 | kcal |
| Effective HT area | 9.4 | m² |
| Overall HTC | 175 | kcal/hr·m²·°C |
| **Heat load** | **15,225** | **kcal/hr** |
| Min. chilling water flow | 14.2 | m³/hr |
| Calculated flow rate | 3.045 | m³/hr |
| Chilling time assumed | 20 | min |

---

## 🔧 Key Process Parameters

| Parameter | Value |
|-----------|-------|
| Utilities used | CW, CHW, CHB, Steam, Vacuum, Nitrogen |
| Temperature range | −10°C to 65°C |
| Pressure range | Full Vacuum to ATM |
| Process nature | Acidic & Basic |
| Key solvent | Hexane (recovered by distillation) |
| Secondary solvent | IPA (recovered via IPA recovery reactor) |
| Cyanide treatment | Hypo treatment before ETP discharge |

---

## 🗂️ File Structure

```
📁 batch-mass-balance-api/
│
├── README.md           ← This file
├── H_MB.xlsx           ← Complete H&MB workbook (5 sheets)
│
└── 📄 Sheet Contents
    ├── xx              ← Full step-by-step mass balance for all reactors
    ├── BFD             ← Block Flow Diagram with input/output summary
    ├── Enthalpy Balance← Heat duty and utility flow rate calculations
    ├── Utility Calc.   ← Detailed utility sizing calculations
    └── RM Data         ← Raw material properties and data
```

---

## 🔬 Key Engineering Takeaways

1. **Mass balance verified** — Total input = Total output = 26,744 kg across all units
2. **Solvent recovery built in** — Hexane recovered by ATM + vacuum distillation; IPA sent to dedicated recovery reactor
3. **Cyanide safety** — Aqueous cyanide layer sent to hypo treatment before ETP; multiple water washes confirm safe disposal
4. **Chilling dominates utility load** — CHW required at 14.2 m³/hr minimum; brine needed for sub-zero steps (−10°C)
5. **Long batch cycle** — 10 KL SSR BCT of 171 hrs is the bottleneck; 8 reactors run in parallel to meet throughput
6. **Temperature control is critical** — Reaction requires precision cooling from −10°C (HCl addition) to +65°C (distillation)

---

## 👨‍🔬 Author

**Satyambhai Shihora**
Chemical Engineering Student — Otto von Guericke Universität Magdeburg
[LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)

---

## 📚 References

1. Perry's Chemical Engineers' Handbook — Heat Transfer and Mass Balance Methods
2. TEMA Standards — Heat Exchanger Design
3. ICH Q7 — Good Manufacturing Practice for Active Pharmaceutical Ingredients

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
