# 🔬 Pathology Coding Assistant

An **AI-assisted pathology coding tool** that reads a de-identified surgical pathology report and suggests the correct codes — **ICD-10-CM, CPT, modifiers, and MIPS quality measures** — each with a plain-language rationale.

Built by a **CPC-A certified Pathology coder** to reflect real coding workflows, compliance rules, and denial-prevention logic.

**▶️ Live demo:** _add your GitHub Pages link here after enabling Pages_
_(e.g.,https://padmaja-gopal.github.io/pathology-coding-assistant/)_

---

## ✨ What it does

Pick a sample report (or paste your own de-identified one), choose a mode, and get fully coded output:

| Mode | For whom | Output |
|------|----------|--------|
| 🔍 **Assistant** | Working coders | Quick codes + brief rationale |
| 🎓 **Practice** | CPC aspirants | Full step-by-step coding reasoning |
| 🧬 **Structured Extract** | Data/AI use | Clean JSON — registry (ICD-O-3, SNOMED) **and** billable (ICD-10-CM, CPT) codes |

### Try these built-in cases
- **Breast lumpectomy + sentinel node** — full-specificity ICD, separate node coding, MIPS #99
- **3 colon/rectal polypectomies** — multi-specimen sequencing, colonoscopy depth→site mapping, adenoma-over-polyp
- **Whipple (pancreaticoduodenectomy)** — multi-organ Level VI bundling, frozen-section add-ons
- **Prostate + lung resections** — MIPS measure mapping (#250 & #396) with QDCs
- **16-specimen report** — MUE unit-limit checking (denial prevention)
- **Report with identifiers** — HIPAA-safe rejection that names the detected identifiers

---

## 🛡️ Privacy by design (HIPAA-minded)

The tool scans input for **actual patient identifiers** (name, MRN, accession number, DOB, physician name, dates) and **refuses to process** any report containing them — returning:

> ⚠️ *File contains sensitive information so couldn't be processed*
> *Detected: (DOB) (Accession#) …*

It names the specific identifiers found so the user knows exactly what to remove, while distinguishing a real identifier value from a harmless descriptive phrase (avoiding false rejections).

---

## 🧠 Coding logic built in

- **CPT pathology** levels 88300–88309, cytology, IHC, flow cytometry, frozen sections (88331/88332), special stains, decalcification (88311)
- **Bundling / unbundling** across 20+ resection procedures, incl. detailed **Whipple** logic
- **Specimen-to-CPT** assignment rules (literal-descriptor conventions, lymph-node rules, "for tumor" vs "other than tumor")
- **ICD-10-CM integrity** (FY2027 Official Guidelines): prevents **upcoding, downcoding, and non-billable** category-header codes
- **Colonoscopy depth → anatomic site** mapping for site-specific colon codes
- **Modifiers** (26, TC, 90, 91, 59, XS, XU, 92) applied only when triggered
- **MIPS** measures with denominator→numerator mapping, QDC codes, and the three outcome types (Performance Met / Denominator Exception / Performance Not Met)
- **MUE unit limits** — checks how many units of a code a multi-specimen report can bill before a denial

---

## 🗂️ About this repo

This is the **no-setup demo version** — it runs entirely in the browser with pre-loaded sample outputs, so anyone can try it instantly with **no API key**. The production version connects to a live AI model (Anthropic Claude) through a secure backend that keeps the key server-side and enforces the same PHI guardrail.

---

## 👩‍⚕️ Author

**Padmaja Gopal, CPC-A** — Certified Professional Coder (Apprentice), Pathology specialization.
🔗 [linkedin.com/in/padmaja-gopal-925b8b23b](https://linkedin.com/in/padmaja-gopal-925b8b23b)

---

_Suggestions only — a certified coder must validate all codes against current-year CPT®/ICD-10-CM references before billing. CPT® is a registered trademark of the AMA. MIPS specifications: verify at qpp.cms.gov. MUE values change quarterly (CMS NCCI/MUE tables). Demo outputs are representative of the tool's coding logic._
