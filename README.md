# Field2Map

### From field photographs to mapped geographic data

Field2Map is a Python-based geospatial tool that extracts GPS coordinates and selected metadata from photographs, validates the geographic information, and converts the results into a structured dataset and interactive map.

## Why I Built Field2Map

Field2Map grew out of a field research idea I was exploring in 2025.

I wanted to investigate how activities in a coastal residential environment could affect aquatic ecosystems. In the area I was interested in, drainage gutters were connected to canals and waterways that ultimately flow into the Lagos Lagoon.

The idea was to spatially document pollution outputs on land and explore how these pathways could connect land-based activities to the aquatic environment.

Photographs were an important part of the proposed fieldwork. I had more than 100 photographs and wanted to associate each photograph with its geographic location and eventually visualize the observations spatially.

My initial approach was to look for existing tools that could place photographs on a map. While these tools could provide a visual representation, I wanted to go beyond simply displaying photographs. I wanted the underlying geographic information in a structured format that could be taken into GIS platforms such as ArcGIS and QGIS and potentially used for further analysis.

I then worked with EXIF metadata extraction for the first time.

The process was much more complicated than I initially expected. I spent several hours working through the metadata extraction process and troubleshooting how to obtain the information I needed in a usable CSV format.

Even after successfully producing the CSV, the workflow was not finished. I encountered further problems trying to get the resulting dataset properly recognized and used in ArcGIS, which required additional troubleshooting.

That experience led to Field2Map.

Instead of treating photographs as the final product, Field2Map treats them as a potential source of structured geographic data.

The goal is to simplify the first stage of this workflow:

**Photographs → EXIF metadata → validated coordinates → structured dataset → interactive map**

## What Field2Map Does

Field2Map V1 can:

- Read EXIF metadata from photographs
- Extract GPS latitude and longitude when available
- Extract photograph date and time
- Extract camera make and model
- Validate geographic coordinates
- Display extracted information in a structured table
- Generate an interactive map
- Export results as CSV
- Export the interactive map as an HTML file

## Workflow

```text
Field photographs
        ↓
EXIF metadata
        ↓
GPS coordinate extraction
        ↓
Validation
        ↓
Structured results table
        ↓
Interactive map
        ↓
CSV + HTML export
