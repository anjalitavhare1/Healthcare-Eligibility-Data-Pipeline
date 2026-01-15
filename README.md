# Assignment
# HEALTHCARE ELIGIBILITY DATA PIPELINE

## OVERVIEW
This project builds a configuration-driven data ingestion pipeline for healthcare eligibility data.
It processes files from multiple partners with varying formats and standardizes them into a single unified dataset.

---

## KEY FEATURES
- Configuration-based partner ingestion
- Support for multiple delimiters and file formats
- Unified standardized output schema
- Built-in validation and error handling
- Output generation in CSV and Excel formats

---

## SUPPORTED PARTNERS
- **Acme Health** : Pipe-delimited (.txt)
- **Better Care** : Comma-delimited (.csv)

---

## STANDARD OUTPUT SCHEMA
- **external_id** : Partner-specific identifier
- **first_name**  : Title Case
- **last_name**   : Title Case
- **dob**         : ISO format (YYYY-MM-DD)
- **email**       : Lowercase
- **phone**       : XXX-XXX-XXXX
- **partner_code**: Partner identifier

---

## HOW TO RUN (GOOGLE COLAB)
1. Open Google Colab
2. Upload the notebook and input files (`acme.txt`, `bettercare.csv`)
3. Run all cells sequentially

### Outputs Generated
- `final_eligibility_output.csv`
- `final_eligibility_output.xlsx`

---

## ADDING A NEW PARTNER
1. Add a new partner entry to the configuration
2. Specify delimiter, file path, column mapping, and partner code
3. No changes to ingestion logic are required

---

## DATA VALIDATION
- Mandatory field checks
- Graceful handling of invalid dates and phone numbers
- Automatic rejection of invalid records
- Partner-level processing logs

---

## TECH STACK
Python, Pandas, Google Colab
