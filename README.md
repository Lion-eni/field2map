## Why I Built Field2Map

Field2Map grew out of a field research idea I was exploring in 2025.

I wanted to investigate how activities in a coastal residential environment could affect aquatic ecosystems. In the area I was interested in, drainage gutters were connected to canals and waterways that ultimately flow into the Lagos Lagoon. The idea was to spatially document pollution outputs on land and show how these pathways could connect land-based activities to the aquatic environment.

Photographs were an important part of the proposed fieldwork. I had more than 100 photographs and wanted to associate each photograph with its geographic location and eventually visualize the observations spatially.

My initial approach was to look for existing tools that could place photographs on a map. While these tools could provide a visual representation, I wanted to go beyond simply displaying photographs. I wanted the underlying geographic information in a structured format that could be taken into GIS platforms such as ArcGIS, QGIS, or other geospatial analysis environments.

I then worked with EXIF metadata extraction for the first time.

The process was much more complicated than I initially expected. I spent several hours working through the metadata extraction process and troubleshooting how to obtain the information I needed in a usable CSV format.

Even after successfully producing the CSV, the workflow was not finished. I encountered further problems trying to get the resulting dataset properly recognized and used in ArcGIS, which required additional troubleshooting and experimentation with other geospatial workflows.

The experience made me realize that there was an opportunity to simplify the first part of this process.

That became the idea behind Field2Map.

Instead of requiring users to manually work through multiple technical steps to turn photographs into geographic data, Field2Map aims to provide a simple workflow:

**Photographs → EXIF metadata → validated coordinates → structured dataset → interactive map**

Field2Map V1 extracts GPS coordinates and selected metadata from photographs, validates the results, displays the information in a structured table, generates an interactive map, and exports the results as a CSV file.

The current version is deliberately simple. It is a starting point for developing a more comprehensive tool for field data collection, environmental research, mapping, and geospatial analysis.
