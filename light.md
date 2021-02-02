# HuBMAP Light Sheet Fluorescence Microscopy (UF-TMC)

### Last Updated: 1/26/2021

## Overview:
This document details light sheet fluorescence microscopy (LSFM) data states, metadata fields, file structure, QA/QC thresholds, and data processing. 

## Description: 
Light sheet fluorescence microscopy is used to image large volumes of tissue following clearing and multiplexed immunolabeling protocols. Datasets consist of one or more Z-stacks, series of optical sections along the z axis. Corresponding Z-stack planes can be stitched together for a Multiview dataset. 

## Defintions: 
Terms used in this document: 
|**Term** |  **Definition**| 
|--|--|
| Fluorescence | Light produced by a fluorophore that is bound to an antibody tag|
| Volume | Three-dimensional region of interest|
| Tile | Field of view in the xy dimension|
| Y axis | Plane that determines height|
| X axis | Plane that determines width|
| Z axis | Plane that determines depth|
| Optical section/plane | A tile at a specific depth in the z-stack |
| Z-stack | A series of images produced at different stage heights or z positions|
| Mutliview | A series of Z-stacks collected in a serpentine path used to acquire large volume datasets. A percentage of tile overlap will occur for both the x- and y-axes. |
| Stitching | Image stitching is the process of combining multiple images (tiles) with overlapping fields of view to produce a single, large image.|
| Tile overlap | Percent of shared region with neighboring tiles in xy dimension|
| Serpentine | Pattern of z-stack acquisition, used for stitching z planes|
| Channels | Name of the fluorescence excitation wavelengths used. May be expressed as a fluorophore name (e.g. DAPI, GFP, DsRED, Cy5), wavelength (e.g. 488, 540, 750), or color (e.g. green, red, blue).|

*Grey Box* - Whole volume of tissue following clearing protocol.
*Multicolor boxes* - Nine Z-stacks encompassing the user defined volume of interest; numbered in order of acquisition. This multi-Z-stack dataset is called a Multiview. 
*Box 3* - Example of Z-stack with 10 optical planes (red dashed squares). Distance between optical planes is “IncrementZ”. 
*Green dashed arrows* -  Serpentine acquisition sequence of Z-stacks for a Multiview data set.

![](https://lh6.googleusercontent.com/amEsImzzbWvEvf1sZgWm8TYKOWBMyBLkKGqkQxSWzVSw1VS4cYcYk2e2IGBl8drtAHxu4HQXMBd96pMfXG8EP9H0nzpzgTXpC38FS-9IHdlmwLDc9_sGtMsPKd0rM3v5KSx0-ANlgg1Ps46XEw)
*Figure 1: The first 10 optical planes imaged are in Box 1, 11-20 in Box 2, 21-30 in Box 3, and so on. The total number of z-stacks acquired (SizeV) is determined by the xy plane field of view which depends on instrument and acquisition settings.*

![](https://lh3.googleusercontent.com/VtQKat9m0SBXs1bT5rIpe-LvcApJcoOEcy6_G3iI3Jd1bcq86gyKD62G2WR32mzD92lt6TSWuBBJ4gb-mm_aFtwFFuxxeTh6-lzpOR3ZG4qJaUugHd9Pk-6pUCrqaSnPcXv2msofwEokZOat0Q)
*Figure 2:Stitching together neighboring z-stack tiles occurs in post-processing (data state, level 2). Tile stitching occurs within the same Z-plane from boxes 1 thru 9 and is reliant upon overlap in the X- and Y- field of view. Tile stitching is a supervised task and may have minor error in alignments. Automated stitching alignment is not without error either and is increasingly challenging for larger volumes of tissue. Standard overlap of tiles is 5%.*

## HuBMAP Lightsheet Data States (Levels): 
|**Data State** |  **Description**| **Example File Type** | 
|--|--|--|
|  0 | Raw image data: This is the data that comes directly off the microscope without preprocessing; sometimes referred to as tiled or unstitched data. (may not always be included).| CZI, OME-TIFF|
| 1 |  Processed Microscopy data: Can include stitching, thresholding, background subtraction, z-stack alignment, deconvolution. May not always be included. |  TIFF, MP4|
| 2 |  Segmentation: Computationally predicted cell (nucleus, cytoplasm) and/or structural boundaries (tubules, ventricles, etc.) May not always be included. |  CSV, TIFF, MP4, STL|
| 3 |  Annotation (Cells and Structures): Interpretation of microscopy image and/or segmentation in terms of biology (e.g. unhealthy vs healthy, cell-type, function, functional region). May not always be included. |  TIFF, MP4|

## Metadata:
The following metadata fields reside in a CSV within the parent folder of each dataset. Terms are native to the *.CZI file generated from Zeiss’s Zen acquisition software.
 
Essential Metadata Overview for Volumetric Reconstruction

|**Light sheet microscopy** |  **Defintion**| **Example** | 
|--|--|--|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
|  0 | a| CZI|
