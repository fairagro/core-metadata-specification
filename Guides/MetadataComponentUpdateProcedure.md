# Metadata component update procedure
This document explains the necessary steps required to publish an updated version of a metadata component (Publication Metadata Set, Agrischemas) that is part of the FAIRagro Core Metadata Specification.

When work on a new version begins, a copy of the current version file is created in the respective metadata component folder in its own version folder. The folder and new file are named after the date and the new version number. 

 - Folder for the Publication Metadata Set: https://github.com/fairagro/core-metadata-specification/tree/main/specification/publicationMetadataSet
 - Folder for Agrischemas: https://github.com/fairagro/core-metadata-specification/tree/main/specification/agrischemas 

The new version number and the update date are changed in the header of the file. Changes to the metadata component are applied directly inside the file and every change is recorded in the respective changelog file of the metadata component.

 - Changelog for the Publication Metadata Set: https://github.com/fairagro/core-metadata-specification/blob/main/specification/publicationMetadataSet/FAIRagro_PublicationMetadataSet_Changelog.md
 - Changelog for Agrischemas: https://github.com/fairagro/core-metadata-specification/blob/main/specification/agrischemas/FAIRagro_Agrischemas_Changelog.md

Changelog entries follow the guidelines of https://keepachangelog.com/.

If necessary, generate new versions of the figures that are part of the metadata component by copying the Mermaid (https://mermaid.ai/) markup from the metadata component file into the Mermaid playground and then exporting the figure as a PNG. This PNG file will be used for making the figures available at publication. Store the PNG files inside the version folder and attach the version number to the end of the file name .

Once a version is ready for release, it has to be published via the FAIRagro Knowlegde Base. This requires writing rights for the corresponding Github repository (https://github.com/fairagro/knowledgebase).

The current version of the metadata component needs be archived, also via the Knowledge Base. The archive folder (https://github.com/fairagro/knowledgebase/tree/main/docs/tech-guides/core_metadata_specification/archive) includes a subfolder for each of the metadata components.

- Archive folder for the Publication Metadata Set: https://github.com/fairagro/knowledgebase/tree/main/docs/tech-guides/core_metadata_specification/archive/publication_metadata_set/
- Archive folder for Agrischemas: https://github.com/fairagro/knowledgebase/tree/main/docs/tech-guides/core_metadata_specification/archive/agrischemas/

For each version being archived, a new folder is created in one of these archival folders, named after the version number (e.g. https://github.com/fairagro/knowledgebase/tree/main/docs/tech-guides/core_metadata_specification/archive/publication_metadata_set/1_0_0/). The files for the current version, taken from the folder of the of metadata component, are copied into the archive folder as well as the images related to the version (stored in the "images" folder of the Knowledge Base, https://github.com/fairagro/knowledgebase/tree/main/docs/images).
Replace the archive changelog file with the  updated changelog file of the metadata component.

Afterwards the new version can be published via the Knowledge Base. Copy the contents of the new version file into the main page file https://github.com/fairagro/knowledgebase/blob/main/docs/tech-guides/core_metadata_specification/index.en.md, copy the updated figures into the images folder (https://github.com/fairagro/knowledgebase/tree/main/docs/images) and update the paths accordingly.
