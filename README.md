# Ingredient Quote Generator

A single-file browser application built for a contract manufacturing company to automate ingredient pricing quotes. Replaced a fully manual process — previously requiring cross-referencing formula sheets against vendor price lists by hand — with an automated matching and calculation engine.

**Reduced quote turnaround time by 60%** and eliminated manual pricing errors across 50+ vendor products.

---

## What it does

The sales team receives customer formulas listing ingredients and percentages. They previously had to manually look up each ingredient in a vendor price database, calculate costs per kilogram, and build a quote spreadsheet from scratch. This tool automates every step of that process.

- **Vendor price list upload** — reads an Excel file containing the full vendor pricing database, auto-detecting column positions by header name regardless of layout
- **Formula import** — accepts ingredient formulas either by Excel upload or direct paste, parsing ingredient names and percentages automatically from multiple input formats
- **Automated price matching** — fuzzy-matches each formula ingredient against the vendor database, handling partial name matches and variations in naming convention
- **Real-time cost calculation** — calculates cost per kg, extended cost by percentage, and total formula cost as ingredients are loaded
- **Multi-vendor comparison** — surfaces the best available pricing across all vendors for each ingredient
- **Customer-supplied ingredient handling** — detects and flags customer-supplied items separately from vendor-priced items
- **Excel export** — generates a formatted, print-ready quote spreadsheet with one click using the xlsx-js-style library
- **Part number tracking** — auto-increments part numbers across the quote for reference

---

## Technical details

- **Single file** — entire application is one self-contained HTML file, no server, no dependencies to install, no build process
- **Runs in any browser** — open the file, upload your data, generate quotes
- **Excel parsing** — uses the `xlsx` library to read vendor price databases directly from `.xlsx` files, with dynamic column detection that works regardless of spreadsheet layout
- **Fuzzy ingredient matching** — handles inconsistencies between formula ingredient names and vendor database names
- **Formula parsing** — accepts multiple input formats including `"Water 85.55"`, `"Water, 85.55%"`, and standard Excel formula exports
- **No data leaves the browser** — all processing happens client-side, vendor pricing data never touches a server

---

## How to use

1. Download `ayo-quote-generator.html`
2. Open it in any web browser — no installation needed
3. Upload your vendor price list Excel file
4. Either upload a formula Excel file or paste ingredients directly
5. Review the auto-generated quote table
6. Click **Export Quote to Excel** to download the formatted quote

---

## Context

Built during my time as a Procurement Specialist at a contract manufacturing company serving cosmetic and personal care clients. The sales team was spending significant time manually building quotes for each client inquiry — this tool reduced that process from hours to minutes by automating the data cross-referencing and calculation steps entirely.

The vendor price database covered 50+ suppliers and 800+ product entries. The tool was used in production for client quote generation across multiple product lines.

---

*Built by Mecapixel · [github.com/Mecapixel](https://github.com/Mecapixel)*
