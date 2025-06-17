# 🧾 CSV (Comma-Separated Values)

Comma-Separated Values (CSV) is one of the most ubiquitous file formats for representing structured tabular data in plain text. Despite its simplicity, CSV has become a cornerstone of data exchange across domains as diverse as bioinformatics, social science, software engineering, and public administration.

CSV files encode data in rows, with each row consisting of values separated by commas (`,`), though delimiters can vary. Its wide support across platforms and languages makes it a de facto standard for lightweight data interchange—even though CSV is not always formally standardized across all implementations.

---

## 📄 Format Metadata

| Field | Value |
|------|-------|
| **Filename extensions** | `.csv` |
| **Internet media type** | `text/csv` |
| **Uniform Type Identifier (UTI)** | `public.comma-separated-values-text` |
| **UTI conformation** | `public.delimited-values-text` |
| **Type of format** | Delimited text / serial tabular data |
| **Container for** | Flat tables (rows and columns of scalar values) |
| **Standard** | [RFC 4180](https://datatracker.ietf.org/doc/html/rfc4180) |
| **Developed by** | Informally developed; later formalized by the IETF |
| **Initial usage** | 1970s (VisiCalc, IBM mainframes); RFC published in 2005 |
| **Extended from** | ASCII, spreadsheet-like exports |
| **Open format?** | ✅ Yes |
| **Official website** | N/A (standard via IETF RFC) |

---

## 🧬 Common Use Cases

CSV is favored for its ease of inspection, creation, and manipulation using basic tools. It is widely used for:

- Exporting spreadsheets (Excel, LibreOffice)
- Data interchange between software
- Bioinformatics pipelines (e.g., gene expression matrices)
- Machine learning datasets (e.g., from UCI ML repository)
- Data publication in open science and open government

---

## 💻 Language-Specific Usage

=== "Python (pandas)"
    ```python
    import pandas as pd
    df = pd.read_csv("data.csv")
    print(df.head())
    ```

=== "R"
    ```r
    df <- read.csv("data.csv")
    head(df)
    ```

=== "JavaScript (D3.js)"
    ```javascript
    d3.csv("data.csv").then(data => {
      console.log(data);
    });
    ```

=== "Shell (csvkit)"
    ```bash
    csvlook data.csv
    csvstat data.csv
    ```

=== "Excel / LibreOffice"
    Open `.csv` files directly as spreadsheets.

---

## 🧭 History & Evolution

CSV's origins are informal, dating back to mainframe exports and early spreadsheet programs like VisiCalc in the late 1970s. It became increasingly popular with the rise of Microsoft Excel, which embraced and extended it—though sometimes in ways that caused compatibility issues (e.g., with date and number formats).

Recognizing this proliferation, RFC 4180 was published in 2005 to describe a "common format" for CSV. However, many tools still implement variations, such as different delimiters (e.g., semicolons in Europe), quotation rules, or line endings.

CSV's strength lies in its simplicity. But that same simplicity also limits its robustness: it lacks support for hierarchical or relational data, metadata, encoding declarations, and schema enforcement.

---

## 🔎 Known Limitations

- ❌ No support for nested or hierarchical data
- ❌ No built-in data typing or schema definition
- ❌ No metadata (e.g., units, descriptions, provenance)
- ⚠️ Encoding ambiguity (UTF-8 vs Latin-1 vs Windows-1252)
- ⚠️ Inconsistent delimiter usage internationally
- ⚠️ Difficult to validate or normalize across tools

---

## 📚 References

- RFC 4180: [Common Format and MIME Type for CSV Files](https://datatracker.ietf.org/doc/html/rfc4180)
- [Wikipedia: CSV](https://en.wikipedia.org/wiki/Comma-separated_values)
- Kandel et al., 2011. "Research Directions in Data Wrangling"
- [Frictionless Data: CSV Dialects](https://specs.frictionlessdata.io/csv-dialect/)
