# 🔬 Pathology Coding Assistant — Live Demo

An AI-assisted tool that suggests **ICD-10-CM + CPT** codes (plus **modifiers** and **MIPS** measures when applicable) from a **de-identified** pathology report — built by a **CPC-A certified Pathology coder**.

**▶️ Live demo:** *(add your GitHub Pages link here after deploying)*

This is the **no-setup demo version** — it runs entirely in the browser with pre-loaded sample cases, so anyone can try it instantly with no API key. The production version connects to a live AI model (Anthropic Claude) through a secure backend.

---

## Try it

Open the page and tap any sample report, then **"Get Codes"**:

| Sample | Demonstrates |
|--------|--------------|
| 🩺 **Breast lumpectomy + sentinel node** | Full-specificity ICD (C50.412), separate node coding (88307 ×2), MIPS #99 |
| 🔬 **3 colon/rectal polypectomies** | Multi-specimen sequencing, depth→site mapping, adenoma-over-polyp, 88305 ×3 |
| 🧬 **Whipple (pancreaticoduodenectomy)** | Multi-organ Level VI bundling, frozen-section add-ons, pT/pN staging |
| 🛑 **Report with patient identifiers** | HIPAA-safe rejection: *"File contains sensitive information so couldn't be processed"* |

Switch between three modes:
- 🔍 **Assistant** — quick codes with rationale (for working coders)
- 🎓 **Practice** — full step-by-step reasoning (for CPC aspirants)
- 🧬 **Structured Extract** — clean JSON with registry (ICD-O-3, SNOMED) *and* billable (ICD-10-CM, CPT) codes

---

## 🛡️ Privacy by design (HIPAA-minded)

The tool scans input for **actual patient identifiers** (MRN, accession number, physician name, dates) and refuses to process them. It distinguishes a real identifier value (`MRN: 4837291`) from a harmless descriptive phrase — avoiding false rejections while protecting PHI.

---

## 🧠 Coding logic built in

- CPT pathology levels **88300–88309**, cytology, IHC, flow cytometry, frozen sections, special stains, decalcification
- **Bundling / unbundling** rules across 20+ resection procedures (incl. detailed Whipple logic)
- **ICD-10-CM integrity** (FY2027 guidelines): prevents upcoding, downcoding, and non-billable category-header codes
- **Colonoscopy depth → anatomic site** mapping for site-specific colon codes
- **Modifiers** (26, TC, 90, 91, 59, XS, XU, 92) applied only when triggered
- **MIPS** measures flagged only when the specimen matches

---

## About

Created by **Padmaja Gopal, CPC-A** — Certified Professional Coder (Apprentice), Pathology specialization.
LinkedIn: [linkedin.com/in/padmaja-gopal-925b8b23b](https://linkedin.com/in/padmaja-gopal-925b8b23b)

*Suggestions only. Always verify against current-year CPT®/ICD-10-CM. CPT® is a registered trademark of the AMA. MIPS: qpp.cms.gov. Demo outputs are representative of the tool's coding logic.*
