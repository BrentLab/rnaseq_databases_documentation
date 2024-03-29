# BioSample

The primary key for this table is bioSampleNumber

- If multiple aliquots of cells are taken at the same time from the same culture (e.g. tube or colony on an agarose plate) then they are aliquots of a single biosample, so only one entry is needed in the biosample table.  

- If you are entering data, or using data, from this table, and you notice a column that is poorly defined in any way (eg, it is never used, should have defined choices and does not, etc), then post an issues report on the appropriate github repository.

## Update Instructions

- Never include a the primary key column (in this case bioSampleNumber) -- that is automatically populated by the database.

- If there is a __default entry__ for a given field, you do not need to include the field in a table used to update the database from `brentlabRnaSeqTools`. Otherwise, the field is required to exist in the table you wish to send to the database.

Name                                 | Type                 | Required  
:------------------------------------|:--------------------:|:---------:
bioSampleNumber                      | int                  | Yes (Primary Key)
harvestDate                          | datetime             | Yes
harvester                            | string               | Yes
experimentDesign                     | string               | Yes
experimentObservations               | string               | Yes, default 'none'
bioSampleObservations                | string               | yes, default 'none'
strain                               | string               | Yes -- foreign key to `strain` table
timePoint                            | float                | Yes
innocpH                              | float                | Yes, default -1
gcid                                 | integer              | Yes -- foreign key to `growthCondition` table

* * *
**[KEY]** and **[REQUIRED]** columns should be included in every sheet. **[OPTIONAL]** columns must be included when there are samples which would have non-empty entries in those columns.

## bioSampleNumber

**[KEY]** Sequential positive integers uniquely identifying the samples taken by a given harvester on a given date. Numbers can be reused as long as the harvester and date are different.

## harvestDate

**[REQUIRED]** The date (e.g. 05.17.20) on which the cells were taken out of culture and growth was stopped. See [general specifications](https://github.com/BrentLab/database_files/wiki) for format details.

## harvester

**[REQUIRED]** Name of the person (e.g. J.PLAGGENBERG)  who was in charge of the experiment. If more than one person was involved, just pick one. See [general specifications](https://github.com/BrentLab/database_files/wiki) for format details.

## experimentDesign

**[REQUIRED]** This should be a short string with no spaces that refers to a design which is actually explained in some other document. E.g. ZEVNeg1_10_15_20_90_SCGal_plates. Do not use something that could be mistaken for a number, such as “20.20”. This doesn’t have to be so descriptive -- you could even use ZEV1, since it will be explained elsewhere. The other document should have the same name as the table entry. It should describe the experiment and list the relevant fields needed to keep all the treatments and samples separate. An example can be found here. 

## bioSampleObservations

**[OPTIONAL]** This is a free text entry field meant to record anything about this sample, specifically pertaining to this table's data, that does not fit into other fields. This __should not be used for storing any information pertinent to experimental design or the strain__.

## strain

Unique strain identifier, eg TDY12345. This is a foreign key to the strain table. Check to make sure your strain is already in the strain table. If it is not, please ask for it to be added.

## timePoint

**[OPTIONAL]** A decimal number in minutes (if whole minutes, there is no need to add the decimal point).
The time between the treatment and the sample collection. Use -1 (neg1 as an integer) for samples collected immediately before the treatment is applied.

## innocpH

pH at innoculation. Default is -1, meaning un-measured.

## gcid

An integer entry which corresponds to a record in the `growthCondition` table. This is the foreign key to the `growthCondition` table