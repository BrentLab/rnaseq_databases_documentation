# GrowthConditions

The primary key for this table is gcid

Name                                 | Type                 | Required  
:------------------------------------|:--------------------:|:---------:
gcid                                 | int                  | yes (Primary Key)
gcDate                               | date                 | yes, autofilled
gcDescription                        | string               | yes, default noDescription
baseNutrientMixName                  | string               | yes, foreign key to baseNutrientMix
nutrientMixModName                   | string               | yes, foreign key to nutrientMixMod
aaid                                 | string               | yes, foreign key to AminoAcid
temperature                          | string               | yes, choices
co2                                  | decimal              | yes, default = 0
buffer                               | string               | yes, choices
bufferConc                           | decimal              | yes, default = 0.0
bufferPh                             | decimal              | yes, default = -1
chx                                  | decimal              | yes, default 0
cAMP                                 | decimal              | yes, default 0
mouseSerum                           | decimal              | yes, default 0
glucose                              | decimal              | yes, default 0
galactose                            | decimal              | yes, default 0

## gcid

Primary key. autofilled integer

## gcDate

autofilled to today's date on entry

## gcDescription

brief description of the growth condition

## baseNutrientMixName

foreign key to the baseNutrientMix table

## NutrientMixModName

foreign key to the nutrientMixMod table. Note that this may be used to join the fields of baseNutrient 
and nutrientMixMoficiation. The sum of the two columns is the final conc of each component

## aaid

Foreign key to the AminoAcid table

## temperature

The temperature in degrees C that the cells were grown. This is a categorical column -- not continuous. Current choices are:  

* room
* 30
* 37

## co2

The percentage of the air flowed in that is added CO2 (i.e. from a bottle). Default is 0%, which indicates room air.

## buffer
Name of buffer. Current possible values include:

* none (default)
* mops
* hepes
* mes

## bufferConc

Molar concentration of buffer added beyond what’s in the base medium. Defaults to 0.

## bufferpH

The pH of the buffer solution itself, before it is added to the medium. Default to -1 ( -1 is used as a default to mean a meaningless pH. This is meant to prevent 'null' or 'NA' in the database, therefore providing a a positive way of filtering for samples in which bufferpH is not tracked).

## chx

Concentration of cyclohexamide, an inhibitor of protein synthesis, in micromolar, uM. Defaults to 0.

## cAMP

Concentration of added cyclic AMP in micromolar, uM. Defaults to 0.

## mouseSerum

Percent, volume per volume

## glucose

Final concentration in the medium, regardless of source in g/L. Defaults to 0.

## galactose

Final concentration in the medium, regardless of source in g/L. Defaults to 0.
