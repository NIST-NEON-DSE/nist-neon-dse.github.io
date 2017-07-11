# NIST DSE Plant Identification with Neon Remote Sensing Data
## A Data-Science competition for ecological data
*  Scaling ecological patterns and processes across is still controversial, but crucial in facing environmental changes;
* This Data Science Challenge and Evaluation is sponsored by the National Institute of Standards and Technology (NIST) Data Science Evaluation (DSE) Series;
* The Data Science Challenge is organized by the University of Florida: a collaboration between the WEecology lab, S. Bohlman lab, and the Data Science Research lab;
* The scope is to integrate data collected by the National Ecological Observatory Network (NEON), from the field to airborne, with the final aim of performing tree species classification;
* We solicit open participations from University, Research institute teams, individuals.
## Why we care
* **Theme**: Species identification of individual trees via airborne remote sensing:
 * Management, Global change, Ecosystem services;
* **Motivation**: scaling up from the field to landscape:
 * financial and logistic limitations restrict field data collection:
 * The combined use of of field data along with remote sensing could make the problem feasible.
## The Data
**Airborne**:
  * Hyperspectral images (.tif):
    * spatial resolution 1m2;
    * 426 fatures (380 < wavelength < 2510nm);
  * High Resolution RGB images (.tif):
    * spatial resolution 0.25m2
  * Canopy high model (.tif)
    * spatial resolution 1m2;
  * Point Cloud LiDAR data.
**Field Data**:
  * stem height,
  * stem latitude and longitude,
  * DBH,
  * species identification,
  * crown diameter
**Individual Tree Crowns**:
  * crown boundaries and stem locations
  * data are manually drawn in the field
  * confidence scores of data collection uncertainty
![alt text](/Users/sergiomarconi/Pictures/Data.png)
## The tasks
* **Crown Delineation**: estimate size, shape, and location of individual tree crowns;
* **Alignment**: pair trees measured at field and landscape, with offset up to several meters;
* **Classification**: determine the species identity of each tree in the scene from remotely sensed data.
### Crown delineation
**Inputs**:
  * **Training**:
    * hyperspectral,
    * RGB,
    * LiDAR,
    * ITC data.
  * **Testing**:
    * hyperspectral,
    * RGB,
    * LiDAR.
**Output**:
  * Shapefiles containing individual crown position and shape.
![alt text](/Users/sergiomarconi/Pictures/Delineation.png)
### Alignment
**Input**:
  * **Training**:
    * ITC,
    * Field Structure Data,
    * remote sensing images (for optional use);
  * **Testing**:
    * Crown to stem linking labels;
**Output**:
    * labels relating ITC and field data.
![alt text](/Users/sergiomarconi/Pictures/Alignment.png)
### Classification
**Input**:
  * **Training**:
    * Field Structure Data (some species labelled),
    * ITC data,
    * Hyperspectral,
    * LiDAR,
    * RGB images;
  * **Testing**:
    * NEON field data (no one labelled with species),
    * ITC data,
    * Hyperspectral,
    * LiDAR,
    * RGB images
**Output**:
  * Array haof probabilities of different species and genera identities for each test ITC
![alt text](/Users/sergiomarconi/Pictures/Classification.png)
