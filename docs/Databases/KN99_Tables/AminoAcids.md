
# AminoAcids

The primary key for this table is aaid


Name                                 | Type                 | Required  
:------------------------------------|:--------------------:|:---------:
aaid                                 | string               | Yes (Primary Key)
all AA three letter codes            | decimal              | Yes, but default set to 0.00000

* * *
**[KEY]** and **[REQUIRED]** columns should be included in every sheet. **[OPTIONAL]** columns must be included when there are samples which would have non-empty entries in those columns.

## aaid

A unique name. No spaces. Camelcase or underscores -- you may mix -- clarity is key.

## amino acid three letter codes

All values for these entries are in g/L. An entry in a given amino acid means that amino acid is present at the given concentration. Each column defaults to 0.