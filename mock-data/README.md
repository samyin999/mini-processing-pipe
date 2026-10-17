# mock-data

Made-up data for minipipe. Nothing here is real: names, IDs, paths and contents are invented.

## export_0001: a review platform export (10 documents)

| Path | What it is |
|---|---|
| `export_0001_loadfile.dat` | the load file: one record per document |
| `NATIVES\0001\<Document ID>.<ext>` | the documents' native files |
| `TEXT\0001\<Document ID>.txt` | the documents' extracted text |

### The `.dat` format (Concordance style, as Reveal writes it)

- UTF-8 **with a byte-order mark** (`EF BB BF`) at the start.
- Every value is wrapped in **þ** (thorn, U+00FE) quotes.
- Values are separated by **DC4** (the control character `\x14`).
- Records end with **CRLF** (`\r\n`).
- The first record is the header (the field names).
- A value may contain a line break. That line break is part of the value, not the end of a record.
- Paths inside the `.dat` use backslashes, relative to the export folder.

Fields: `DOCUMENT ID`, `HOST REFERENCE` (a parent's ID, for an attachment), `DOCUMENT DATE` (dd/mm/yyyy), `DOCUMENT TYPE`,
`DOCUMENT TITLE`, `FROM`, `TO`, `CUSTODIAN`, `RELATIVENATIVEFILE`, `RELATIVETEXTFILE`, `[META] FILE PATH` (where the
original came from), `[META] FILE SIZE (bytes)`, `[RT] MD5 HASH` (of the original), `[RV] TV FILE ID`.

## source_0001: the originals the export was made from

`[META] FILE PATH` in the `.dat` points here: `\\fileserver\import\0001\` stands for this folder.
A path running through `Archive.zip` means a file inside that zip.

## Notes

- The files' contents are placeholder text, not real `.docx` / `.pdf` / `.msg` files. Only their bytes, sizes and MD5s matter.
- **The exact bytes matter** (MD5s, the line break inside a value). `.gitattributes` stops git converting line endings here.
- This export has **deliberate problems** for minipipe to find. The list is in [ANSWERS.md](ANSWERS.md): try finding them with your code before you look.
