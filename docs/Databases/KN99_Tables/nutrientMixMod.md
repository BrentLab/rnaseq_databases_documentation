# BaseNutrientMix

Entries in g/L. Valid entries are all real numbers in g/L and represent change from the “base” that the record references. Note that there will be a record with name ‘none’ in the “base” table which will allow a user to enter an entirely ‘custom’ nutrient here.  

The combination of 'component' columns should be unique.


Name                                      | Type                 | Required  
:-----------------------------------------|:--------------------:|:---------:
    nutrientMixModName                    | string               | yes
    nutrientMixModDesc                    | string               | yes, default noNutrientDesc
    nutrientMixModDate                    | string               | yes, autofilled
    calciumChloride                       | float                | yes, default 0
    ferricNitrate                         | float                | yes, default 0
    magnesiumSulfate_anhydrous            | float                | yes, default 0
    potassiumChloride                     | float                | yes, default 0
    sodiumBicarbonate                     | float                | yes, default 0
    sodiumChloride                        | float                | yes, default 0
    sodiumPhosphateMonobasic_anhydrous    | float                | yes, default 0
    sodiumPhosphateDibasic_anhydrous      | float                | yes, default 0
    calciumNitrate                        | float                | yes, default 0
    fericChloride                         | float                | yes, default 0
    potassiumIodide                       | float                | yes, default 0
    copperSulfate                         | float                | yes, default 0
    manganeseSulfate                      | float                | yes, default 0
    zincSulfate                           | float                | yes, default 0
    sodiumMolybdate                       | float                | yes, default 0
    potassiumPhosphateMomobasic           | float                | yes, default 0
    calciumPantothenate                   | float                | yes, default 0
    boricAcid                             | float                | yes, default 0
    ammoniumSulfate                       | float                | yes, default 0
    cholineChloride                       | float                | yes, default 0
    folicAcid                             | float                | yes, default 0
    myoInositol                           | float                | yes, default 0
    niacinamide                           | float                | yes, default 0
    dPantothenicAcid_hemicalcium          | float                | yes, default 0
    pyridoxine_hcl                        | float                | yes, default 0
    riboflavin                            | float                | yes, default 0
    thaimine_hcl                          | float                | yes, default 0
    dBiotin                               | float                | yes, default 0
    pAminoBenzoicAcid                     | float                | yes, default 0
    b12                                   | float                | yes, default 0
    adenine                               | float                | yes, default 0
    uracil                                | float                | yes, default 0
    glutathione                           | float                | yes, default 0
    peptone                               | float                | yes, default 0
    yeastExtract                          | float                | yes, default 0
    phenolRed_Na                          | float                | yes, default 0
    pyruvicAcid_Na                        | float                | yes, default 0


* * *
**[KEY]** and **[REQUIRED]** columns should be included in every sheet. **[OPTIONAL]** columns must be included when there are samples which would have non-empty entries in those columns.

## nutrientMixModName

A unique name. No spaces, use underscores.

## each field represents a CHANGE from a baseNutrientMix record

All values for these entries are in g/L. Each column defaults to 0. Negative values are permitted.