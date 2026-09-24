# Counting Pixels and Calculating Marine Habitat Areas
## Overview
 
Once a habitat classification map has been produced, the next step is to quantify the extent of each habitat class. This can be achieved by counting the number of pixels assigned to each class and converting these counts into area measurements.
 
Because each pixel represents a known ground area, the total area of a habitat can be estimated using the pixel count and pixel size.
 
## Workflow 
### 1. Load the Classified Raster
Open the classified habitat raster and identify its spatial resolution. The spatial resolution determines the size of each pixel on the ground.
<p align="center">
<img src="https://images.openai.com/static-rsc-4/rtmqJhFIJ6sHBbfsa_OXJAynQFZHuH2uzhIvH8oJXftLVXX8wv_eBUAKO9KpOuWshT2BFu9gDiN6UtZ7WMNJHIPSZ6ppixuBuZk3Z-S5ek41nHKyt2lY9-qN1lz_nv5SAZmjcv_l61ceA4V5-MYsCKS1Cbqndy3msNeDvie4Ov1XKxgGgvEL3SZPNrZmnnar?purpose=fullsize" width="600">
</p>

For example:
 
- 10 m × 10 m pixel = 100 m²
- 30 m × 30 m pixel = 900 m²
 
The pixel area is calculated as:
 
**Pixel Area = Pixel Width × Pixel Height**
 
### 2. Count Pixels for Each Habitat Class
Count the number of pixels belonging to each class in the classified raster.
 
Example:
 
| Class | Habitat | Pixel Count |
|---------|---------|---------|
| 1 | Coral Reef | 1,200 |
| 2 | Seagrass | 850 |
| 3 | Mangrove | 430 |
| 4 | Sand | 670 |

 
### 3. Calculate Habitat Area
The area occupied by each habitat class is calculated using:
 
**Habitat Area = Pixel Count × Pixel Area**
 
For example, if the raster resolution is 10 m and each pixel represents 100 m²:
 
- Coral Reef Area = 1,200 × 100 = 120,000 m²

### 4. Convert Area Units 
Area values can be converted into hectares (ha) or square kilometres (km²) for easier interpretation.
 
Conversions:
 
- 1 hectare (ha) = 10,000 m²
- 1 km² = 1,000,000 m²

 
### 5. Calculate Percentage Coverage

The proportional coverage of each habitat class can be calculated as:
 
**Percentage Cover = (Class Pixel Count ÷ Total Pixel Count) × 100**
 
This provides the contribution of each habitat class relative to the total mapped area.
 
## Example Output
 
| Habitat | Pixel Count | Area (ha) | Percentage Cover (%) |
|----------|------------|-----------|---------------------|
| Coral Reef | 1,200 | 12.0 | 38.1 |
| Seagrass | 850 | 8.5 | 27.0 |
| Mangrove | 430 | 4.3 | 13.6 |
| Sand | 670 | 6.7 | 21.3 |
 
## Summary
 
This workflow estimates habitat extent by counting the number of pixels assigned to each class and converting these counts into area measurements. The results provide habitat coverage statistics in square metres, hectares, square kilometres, and percentage cover. This approach is commonly used in habitat mapping, land-cover classification, and environmental monitoring studies.
`