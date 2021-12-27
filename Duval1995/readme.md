# Terry Duval's 1995 dissertation about English gainwords in Maori

![CLDF validation](https://github.com/lexibank/uralex/workflows/CLDF-validation/badge.svg)

This folder contains CLDF-conform data about placenames borrowed from English into Maori from the first 22 pages of volume 3 of [A preliminary dictionary of Maori gainwords compiled on historical principles](https://ir.canterbury.ac.nz/handle/10092/4865) (1995) by Terry P. Duval

**Source**:

```
@thesis{Duval1995,
  author = {Terry P. Duval},
  title = {A preliminary dictionary of Maori gainwords compiled on historical principles},
  year = {1995},
  publisher = {University of Canterbury. Maori},
}
```
The Python scripts used for reading and preprocessing the pdf are made available in the folder [preprocessing](https://github.com/martino-vic/en_borrowings_maori/tree/master/Duval1995/preprocessing). 

**CLDF Metadata**: [metadata.json](./metadata.json)

**Sources**: [sources.bib](./sources.bib)

property | value
 --- | ---
[dc:conformsTo](http://purl.org/dc/terms/conformsTo) | [CLDF Wordlist](http://cldf.clld.org/v1.0/terms.rdf#Wordlist)
[dc:license](http://purl.org/dc/terms/license) | https://creativecommons.org/licenses/by/4.0/
[rdf:ID](http://www.w3.org/1999/02/22-rdf-syntax-ns#ID) | en_borrowings_maori
[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type) | http://www.w3.org/ns/dcat#Distribution


## <a name="table-formscsv"></a>Table [forms.csv](./forms.csv)

property | value
 --- | ---
[dc:conformsTo](http://purl.org/dc/terms/conformsTo) | [CLDF FormTable](http://cldf.clld.org/v1.0/terms.rdf#FormTable)
[dc:extent](http://purl.org/dc/terms/extent) | 1686


### Columns

Name/Property | Datatype | Description
 --- | --- | ---
[ID](http://cldf.clld.org/v1.0/terms.rdf#id) | `string` | Primary key
[Form](http://cldf.clld.org/v1.0/terms.rdf#form) | `string` | written in the orthography of the language in question
`IPA` | `string` | Phonetic transcription in International Phonetic Alphabet
[Language_ID](http://cldf.clld.org/v1.0/terms.rdf#languageReference) | `string` | References [languages.csv::ID](#table-languagescsv)
[Parameter_ID](http://cldf.clld.org/v1.0/terms.rdf#parameterReference) | `string` |

## <a name="table-languagescsv"></a>Table [languages.csv](./languages.csv)

property | value
 --- | ---
[dc:conformsTo](http://purl.org/dc/terms/conformsTo) | [CLDF LanguageTable](http://cldf.clld.org/v1.0/terms.rdf#LanguageTable)
[dc:extent](http://purl.org/dc/terms/extent) | 2


### Columns

Name/Property | Datatype | Description
 --- | --- | ---
[ID](http://cldf.clld.org/v1.0/terms.rdf#id) | `string` | Primary key
[Name](http://cldf.clld.org/v1.0/terms.rdf#name) | `string` |
[Glottocode](http://cldf.clld.org/v1.0/terms.rdf#glottocode) | `string` |
[ISO639P3code](http://cldf.clld.org/v1.0/terms.rdf#iso639P3code) | `string` |
[Macroarea](http://cldf.clld.org/v1.0/terms.rdf#macroarea) | `string` |
[Latitude](http://cldf.clld.org/v1.0/terms.rdf#latitude) | `decimal` |
[Longitude](http://cldf.clld.org/v1.0/terms.rdf#longitude) | `decimal` |
`Family` | `string` |

## <a name="table-borrowingscsv"></a>Table [borrowings.csv](./borrowings.csv)

property | value
 --- | ---
[dc:conformsTo](http://purl.org/dc/terms/conformsTo) | [CLDF BorrowingTable](http://cldf.clld.org/v1.0/terms.rdf#BorrowingTable)
[dc:extent](http://purl.org/dc/terms/extent) | 842


### Columns

Name/Property | Datatype | Description
 --- | --- | ---
[ID](http://cldf.clld.org/v1.0/terms.rdf#id) | `string` | Primary key
[Target_Form_ID](http://cldf.clld.org/v1.0/terms.rdf#targetFormReference) | `string` | References the recipient word in the target language<br>References [forms.csv::ID](#table-formscsv)
[Source_Form_ID](http://cldf.clld.org/v1.0/terms.rdf#sourceFormReference) | `string` | References the donor word from the source language<br>References [forms.csv::ID](#table-formscsv)