# BaseNutrientMix

All components are in g/L and must be >= 0. 

Name                                      | Type                 | Required  
:-----------------------------------------|:--------------------:|:---------:
    baseNutrientName                      | string               | yes
    baseNutrientDesc                      | string               | yes, default noNutrientDesc
    baseNutrientSource                    | string               | yes, default noSource
    baseNutrientDate                      | date                 | yes, autofilled
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

## baseNutrientName

Primary key. No spaces or special character other than an underscore possibly. Uniquely identifies a baseNutrientMix.

## description

Unstructured (so normal english sentences). brief text to describe the nutrient mix

## baseNutrientSource

The origin of the media. This will be an ‘options’ entry and will include any commercial sources of the mix. Should also include ‘brentlab’ as an option for a mix created in the brentlab, as well as the names of other labs or washU sources if applicable

## each field represents a possible component of a base nutrient

All values for these entries are in g/L. Each column defaults to 0. Entries must be >=0.