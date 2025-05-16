## QUESTIONS

-  What data regarding hydrophobic plant surfaces exist today
-  What proportion of the total amount of possible data does this represent
-  What is the state of collection, aggregation, and harmonization of the existing data
-  Would a different state be scientifically useful

## METHODS

### Question 1 What data regarding hydrophobic plant surfaces exist today

To answer the question of what data are out there, we must first specify what form hydrophobic plant data would take, and ideally generate a test. 

We could limit our inquiry by stating that we are interested in per-species data on plants. With that in mind, we endeavored to generate a single a "record prototype" with the goal of satisfying the immediate needs of a hypothetical future inquirer as to the water contact properties of any given plant. Judging from the construction and effective use of BindingMOAD records (Carlson, et al.) we can observe that useful records will contain cross-record comparable physiochemical properties, consistent methodology labelling and notes, and information about data provenance, and traversable references to standard databases.

The MIAPPE Database supplies a "specification including a checklist and a data model of metadata required to adequately describe plant phenotyping experiments." (Website) Combining critical fields from the MIAPPE base record desctiption, along with new fields for Leaf Hydrophobicity as a

MIAPPE field    Description
ObservationUnitID	Primary key linking to other MIAPPE sheets
GermplasmID (with accepted WFO/Tropicos synonym)	Ensures taxon traceability
ObservationTimeStamp (+ ObservationTimePoint)	Needed if CA changes with developmental stage
EnvironmentParameter & Value	CA is humidity- and surface-age-dependent
ObservationVariableID	Will point to Contact Angle trait in an ontology
MethodID	Tie to your measurement protocol (e.g. static sessile-drop CA)

(Full MIAPPE spec table in Papoutsoglou et al. 2020) PubMed Central

2 Add a Minimal Information for Leaf Hydrophobicity (MILH) extension
New field	Definition / controlled vocab suggestion
ContactAngleMean	Mean static CA (°)
ContactAngleSD / SE	Precision of measurement
LeafSide	{adaxial, abaxial, both} (use Plant Ontology PO:0025034 etc.)
SurfacePreparation	{intact, cleaned, dewaxed, rehydrated…}
MeasurementLiquid	Usually “pure water (18 MΩ)”
MethodDetail	Drop volume, imaging system, goniometer software
ReferenceDOI	Paper or dataset DOI

[Figure 1]

We will then review literature to confirm the fields that would be common to hydrophobicity or related studies in the field. From a review of ten studies selected from a simple search for "hydrophobicity in plant leaves" listed in Table 1, we arrived at a more complete record structure in Figure 2.

[Table 1]

[Figure 2]

It should be noted that this record structure is not intended to be complete at this time, but rather sufficient to "test" whether a scientific article has sufficient information to supply one or more taxon-keyed records. Table 2 lists each record field and an assessment of whether or not the given record fulfills that specific data element.

[Table 2]

Finally, Figure 3 assembles data this exercise to outline define our "minimal record" for our first question. [NOTE is there a reference or better method for "cutting" our minimal record down to this state?]

[Figure 3]

Turning to a general assessment, three general searches against the SCOPUS API were executed and the results were unioned into a single articles list. These searches were intended to find studies about "hydrophobicity in plants." The list of queries resides in Table 3.

[Table 3]

The resultant articles list was LLLLL articles long. In order to take a random sample of the list of articles, MM random integers were generated with a command execution in the Julia language, and articles at those indicies in the list of articles were downloaded where possible. Due to rights limitations, the total number of downloaded articles was NN. The list of articles appears in the related data.

Each article was hand-curated to see if one or more well-formed taxon-based hydrophocity record could be generated. [TODO Consider human curation details here. Could we enlist a second curator? Also, citations to good curation principles (incl but not limited to BindingMOAD?)]

PP acceptable records were generated from QQ articles. The generated records appear in the data attachment.

As a second test, ten searches that mentioned specific plants and hydrophobicity were executed against the SCOPUS API. Care was taken to generate search terms that balanced recall and precision, using the general principle that recall is in this case slightly more important. An example search query appears in Figure 4.

[Figure 4]

Five of the plants searched were known, well-studied taxa including the lotus. Five plants were selectd using random indicies from the TRY database. In order to narrow down the search, specifies specificity was limited to the (genus?) level. For each selected plant, synonyms were assembled manually by the researcher through other plant data sources (WHICH ONES?)

The queries for the ten plants yielded XX articles. (XX0 for the five "known" hydrophobes and XX1 for the five random plants.) The articles were again manually curated for possible empirical plant hydrophobicity data. This process yielded YY records, again appearing in the data supplement for this article.

## DISCUSSION

For our first question, we can observe the proportions of "data-containing articles" out of the total numbers of articles in an attempt to estimate the number of records that might be yielded by an exhaustive inquiry.  [DATA HERE]