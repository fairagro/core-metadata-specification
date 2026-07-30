# FAIRagro Core Metadata Specification

##  1. Introduction and motivation
FAIRagro offers a metadata framework for publishing research datasets in the agrosystem domain and is meant to be implemented in data publication services such as Research Data Infrastructures (RDIs) and data repositories.

For generic metadata, the Publication Metadata Set builds on [Schema.org](https://schema.org){:target="_blank"} and other standards ([DC Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/){:target="_blank"}, [DCAT](https://www.w3.org/TR/vocab-dcat-3/){:target="_blank"}) and combines these to define a set of types, properties and cardinalities and links between the types. 

Domain specific metadata is expressed through the Agrischemas framework. It additionaly builds on [Bioschemas](https://bioschemas.org/){:target="_blank"} to add agricultural related information to [Dataset](https://schema.org/Dataset){:target="_blank"} metadata with a focus on increasing its findability. It uses existing [types](https://bioschemas.org/types/){:target="_blank"} and [properties](https://schema.org/Property){:target="_blank"} and recommends semantic concepts to achieve interoperability. It can be implemented in already existing [Schema.org](https://schema.org){:target="_blank"} interfaces by mapping domain-specific information available in local data/metadata to structures described in this document. 
**Agrischemas offers a list of recommended types and properties for findability based on this approach.**

These two components of FAIRagros metadata approach define a Core Metadata Specification to make required information available for FAIRagro services such as the [FAIRagro Search Hub](https://search-hub.fairagro.net/){:target="_blank"} which is based on [Dataverse](https://dataverse.org/){:target="_blank"}. The Core Metadata Specification is harmonized with existing generic metadata standards as well as ongoing [NFDI](https://www.nfdi.de/){:target="_blank"} wide developments.

---
# <small>Contributors</small>
The Publication Metadata Set and Agrischemas are collaborative efforts within the FAIRagro consortium and adjacent communities. Contributors include participants from FAIRagro Task Areas [3](https://fairagro.net/fairagro_team_category/ta-3/){:target="_blank"}, [4](https://fairagro.net/fairagro_team_category/ta-4/){:target="_blank"} and the [“Agri-schemas” project](https://github.com/Rothamsted/agri-schemas/tree/master){:target="_blank"} for Agrischemas.

For feedback contact Gabriel Schneider ([schneiderg@zbmed.de](mailto:schneiderg@zbmed.de){:target="_blank"}) or the [Agrischemas mailinglist](mailto:agri-wg-bioschemas@listserv.dfn.de){:target="_blank"}.

(*Last Update: 2026-07-30*)

---
#<small>How to cite this page?</small>
Schneider, G., Jung, J., Reinosch, N. & Martini, D. *et al.* (2025). *FAIRagro Core Metadata Specification*. FAIRagro Knowledge Base. [https://knowledgebase.fairagro.net/en/tech-guides/core_metadata_specification/](https://knowledgebase.fairagro.net/en/tech-guides/core_metadata_specification/). Under: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/){:target="_blank"}.  

[![CC BY Logo](../images/cc-by.png)](https://creativecommons.org/licenses/by/4.0/){:target="_blank"}
