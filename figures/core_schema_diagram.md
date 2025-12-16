---
config:
  theme: redux
---
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
	    - Author [PersonOrganization]
	    - Contributor [PersonOrganization]
		- Title [Text]
	    - Identifier* [Identifier]
	    - URL [URL]
    }

    class DefinedTerm {
	    - Term* [Text]
		- Term description [Text]
	    - Term URL [URL]
	    - Code [Text]
	    - Terminology [URL]
    }

    class Identifier {
	    - Value* [Text]
	    - Scheme* [Text]
    }

    class DataCatalog {
	    - Name* [Text]
		- Identifier [Identifier]
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
	    - Update date [Date | DateTime]
	    - Language [Text]
	    - Access rights [Text]
	    - Source RDI* [DataCatalog]
	    - Has part [Dataset | CreativeWork]
	    - Is part of [Dataset | CreativeWork]
	    - Is based on [Dataset | CreativeWork]
	    - Access type [Boolean]
		- Spatial resolution [Text | xsd:decimal]
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