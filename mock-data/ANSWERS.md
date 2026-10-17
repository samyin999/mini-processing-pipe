# export_0001: the planted problems (spoilers)

| Document | Problem | Where the fix is |
|---|---|---|
| ABC.001.0001.0003 | native **missing** | original loose in `source_0001\Documents\Reports\` |
| ABC.001.0001.0004 | title has a **line break inside the value** (the record spans two lines) | nothing to fix: a reader must keep it as one record |
| ABC.001.0001.0005 | native **wrong size** (truncated: 20 bytes short; MD5 differs) | original in `source_0001\Documents\Finance\` |
| ABC.001.0001.0006 | title has **leading and trailing spaces**; **blank date** | cleaning for the `.mdb` |
| ABC.001.0001.0007 | native **missing** | original **inside** `source_0001\Archive.zip` (`Contracts/Contract scan.pdf`) |
| ABC.001.0001.0008 | text file **missing**; title has **non-ASCII** characters (é, en dash) | text: regenerate or report; title: encoding must survive |
| ABC.001.0001.0009 | **blank `RELATIVENATIVEFILE`**, and no native on disk | name it `NATIVES\0001\ABC.001.0001.0009.jpg` (from its neighbours), restore from `source_0001\Documents\Photos\` |
| ABC.001.0001.0010 | native **missing**, original **nowhere** in the source; blank custodian | NOT FOUND: needs a person |
| ABC.001.0001.0001 | `TO` ends in a **trailing `;`** | cleaning: split parties on `;`, drop the empty one |
| ABC.001.0001.0002 | an attachment (`HOST REFERENCE` = 0001); its original is inside the `.msg`, so not in the source as a loose file | its native is fine in the export: nothing to restore |

Every document's `[RT] MD5 HASH` and `[META] FILE SIZE (bytes)` describe the **original**. Match by MD5, never by name.
