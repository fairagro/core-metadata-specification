
# FAIRagro Metadata Set for Publication Standards
Version 1
11.12.2025

## 1. Motivation

The FAIRagro Publication Metadata Set is a metadata schema for publishing research data sets in the agrosystem domain. It defines a core minimal metadata set to make required information available for FAIRagro services such as the FAIRagro Search Hub. It is harmonized with existing generic metadata standards as well as ongoing NFDI wide developments. In combination with Agrischemas, FAIRagros domain-specific metadata approach, it offers a solid foundation for FAIR datasets.

## 2. Metadata concepts
```mermaid
classDiagram
direction LR
    class PersonOrganization {
	    - Type* [Person | Organization]
	    - Name* [Text]
	    - if Person; Affiliation* [Organization]
	    - Identifier* [Identifier]
	    - E-Mail [Text]
    }

    class Place {
	    - Type [City | Country | State]
	    - Name [Text]
	    - Bounding box* [Text]
	    - Elevation [Text]
	    - Spatial reference system [Identifier]
    }


    class CreativeWork {
	    - Type* [CreativeWork | Article | Book | Poster]
	    - Title [Text]
	    - Author [PersonOrganization]
	    - Contributor [PersonOrganization]
	    - Identifier* [Identifier]
	    - URL [URL]
    }

    class DefinedTerm {
	    - Term* [Text]
	    - Term URL [URL]
	    - Code [Text]
	    - Term description [Text]
	    - Terminology [URL]
    }

    class Identifier {
	    - Value* [Text]
	    - Scheme [Text]
	    - URL* [URL]
    }

    class DataCatalog {
	    - Name* [Text]
	    - URL* [URL]
    }

    class Dataset {
	    - Title* [Text]
	    - Alternative title [Text]
	    - Author* [PersonOrganization]
	    - Point of Contact* [PersonOrganization]
	    - Contributor [PersonOrganization]
	    - Description* [Text]
	    - Subject* [DefinedTerm]
	    - Identifier* [Identifier]
	    - Keywords* [DefinedTerm]
	    - License* [URL]
	    - URL* [URL]
	    - Spatial coverage [Place]
			- Temporal coverage [DateTime | Text]
	    - Version [Text]
	    - Format [Text]
	    - Production date [Date | DateTime]
	    - Distribution date [Date | DateTime]
	    - Deposit date [Date | DateTime]
	    - Update date [Date | DateTime]
	    - Language [Text]
	    - Data category [Text]
	    - Access rights [Text]
	    - Source RDI* [DataCatalog]
	    - Has part [Dataset | CreativeWork]
	    - Is part of [Dataset | CreativeWork]
	    - Is based on [Dataset | CreativeWork]
	    - Access type [Boolean]
    }

    Dataset --> PersonOrganization
    Dataset --> DefinedTerm
    Dataset --> Identifier
    Dataset --> CreativeWork
    Dataset --> DataCatalog
    Dataset --> Place
    PersonOrganization --> Identifier
    CreativeWork --> PersonOrganization
    CreativeWork --> Identifier
    Place --> Identifier
    DataCatalog --> Identifier
```

Cardinalities are defined in relation to their respective concepts. Example: A cardinality of “1” for a property does only apply, if an instance of its related concept exists. This doesn’t necessitate the existence of such an instance.

### 3.1 Dataset

**Definition:** A body of structured information describing some topic(s) of interest.

Schema.org representation:
```
{
	“@type”: “https://schema.org/Dataset”
}
```

#### 3.1.1 Title
**Definition:** “The main title of the Dataset” (taken from DataVerse)
**Cardinality:** 1
**Range:** Text
[Schema.org](http://schema.org) representation:
```
{
	“[https://schema.org/name](https://schema.org/name)”: “Example title”
}
```


