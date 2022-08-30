    strain = models.CharField(primary_key = True, max_length=8)
    baseStrain = models.CharField(max_length=200, default = "none")  # added to differentiate lab control from clinical strain
    genotype1 = models.CharField(max_length=200, null = False, blank = False)
    perturbation1 = models.CharField(max_length=200, default = "none")
    marker1 = models.CharField(max_length=200, default = "none")
    genotype2 = models.CharField(max_length=200, default = "none")
    perturbation2 = models.CharField(max_length=200, default = "none")
    marker2 = models.CharField(max_length=200, default = "none")

# AminoAcids

The primary key for this table is aaid


Name                 | Type                 | Required  
:--------------------|:--------------------:|:---------:
strain               | string               | Yes (Primary Key)
baseStrain           | decimal              | Yes, but default set to 0.00000
genotype1            | string               | yes
perturbation1        | string               | yes, default 'none'
marker1              | string               | yes, choices
genotype2            | string               | yes, default 'none'
perturbation2        | string               | yes, default 'none'
marker2              | string               | yes, choices
strainNotes          | string               | yes, default 'none'

* * *
**[KEY]** and **[REQUIRED]** columns should be included in every sheet. **[OPTIONAL]** columns must be included when there are samples which would have non-empty entries in those columns.

## strain

A unique name. No spaces. Camelcase or underscores -- you may mix -- clarity is key.

## baseStrain

The parent strain -- meant to differentiate from clinical strains

## genotype1

perturbed locus

## perturbation1

One of the following

* none (default)
* deletion
* over
* swap

## marker1

One of the following

* none (default)
* NAT
* G418

## genotype2

Second perturbation, if one exists. Default 'none'

## perturbation2

One of the following

* none (default)
* deletion
* over
* swap

## marker2

One of the following

* none (default)
* NAT
* G418

## strainNotes

Things we should know about a given strain. If the strain is bad, use 
`bad_strain`. Default 'none'