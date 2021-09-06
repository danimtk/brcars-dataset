<p align="center">
    <img src="https://github.com/danimtk/brcars/blob/main/resources/brcars-cover.png" alt="BRCars logo" width="100%">
</p>

<h3 align="center">BRCars Dataset</h3>

<p align="center">
  BRCars is a dataset for fine-grained classification and other computer vision tasks. The dataset contains a total of 311,595 images belonging to 53,747 car advertisements of 427 car models. The images were collected from <a target="_blank" href="http://webmotors.com.br">webmotors.com.br</a>.
</p>

## General information

BRCars images were split into two sets, BRCars-196 and BRCars-427.
BRCars-196: this set has 196 classes, with each class referring to a car model. This set is composed of the most common car models (those that had more than 200 car advertisements).
BRCars-427: this set has images of the 196 classes of BRCars-196, plus 231 classes with fewer images (unbalanced classes).

**It is important to mention that according to the current <a target="_blank" href="https://www.webmotors.com.br/seguranca/politica-de-privacidade/">privacy terms</a> of the website, commercial use of the data is prohibited without the prior and express consent of <a target="_blank" href="http://webmotors.com.br"> Webmotors </a>.**

## Download

The image files are splited in tar.gz files. It can be downloaded from this <a target="_blank" href="https://b.link/brcars">link<a>.
    
After downloading and extracting the tar.gz file, the folder structure will look like this:

```text
brcars427/
        ├── 0/
        │   ├── 643/
        │   │   ├── file1.jpg
        │   │   ├── ...
        │   │   └── fileN.jpg
        │   ├── .../
        │   └── 3770/
        ├── 1/
        │   ├── 643/
        │   │   ├── file1.jpg
        │   │   ├── ...
        │   │   └── fileN.jpg
        │   ├── .../
        │   └── 3770/
        └── 2/
            ├── 643/
            │   ├── file1.jpg
            │   ├── ...
            │   └── fileN.jpg
            ├── .../
            └── 3770/
```
### Granularity hierarchy

Although the images of BRCars-196 and BRCars-427 are grouped so that the level of granularity is given by the model, the images can be grouped into other granularity levels. The following figure shows the hierarchical tree with the possible levels of possible granularities.

<p align="center">
    <img src="https://github.com/danimtk/brcars/blob/main/resources/granularities_hierarchical_tree.png" alt="hierarchical tree of granularity" width="420">
</p>

The images can be grouped by make, model, year and by instance. The granularity per instance allows you to group images belonging to a specific car. This latter granularity is possible due to the nature of the data source, which groups different images from a single real instance of the car.

### brcars-196.csv and brcars-427.csv files

The files brcars-196.csv and brcars-427.csv have the same structure. They have x attributes, that are:

**id** *- is a unique identifier of the car instance;*

**model_id** *- is the identifier of the car model;*

**model_label** *- the textual label of the car model;*

**make_id** *- the make identifier of the car;*

**make_label** *- the make textual label of the car;*

**year** *- the year of the car fabrication;*

**persp** *- the perspective of the car contained in the image (c for cockpit and e  for external);*

**uri** *- uniform resource identifier to image file;*

**split** *- the split of data (0 for train split, 1 for validation split, and 2 for the test).*
