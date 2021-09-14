<p align="center">
    <img src="https://github.com/danimtk/brcars-dataset/blob/main/resources/brcars-cover.png" alt="BRCars logo" width="100%">
</p>

<h3 align="center">BRCars Dataset</h3>

<p align="center">
  BRCars is a dataset for fine-grained classification and other computer vision tasks. The dataset contains a total of 300,325 images belonging to 52K car advertisements of 427 car models. The images were collected from <a target="_blank" href="http://webmotors.com.br">webmotors.com.br</a>.
</p>

## General information

BRCars images were split into two sets, BRCars-196 and BRCars-427.
BRCars-196: this set has 196 classes, with each class referring to a car model. This set is composed of the most common car models (those that had more than 200 car advertisements).
BRCars-427: this set has images of the 196 classes of BRCars-196, plus 231 classes with fewer images (unbalanced classes).

**It is important to mention that according to the current <a target="_blank" href="https://www.webmotors.com.br/seguranca/politica-de-privacidade/">privacy terms</a> of the website, commercial use of the data is prohibited without the prior and express consent of <a target="_blank" href="http://webmotors.com.br"> Webmotors </a>.**

## Download

The image files are zipped. It can be downloaded from this <a target="_blank" href="https://b.link/brcars">link<a>.
    
After downloading and extracting the .zip file, the folder structure will look like this:

```text
brcars427/
        ├── 0/
        │   ├── 1/
        │   │   ├── file1.jpg
        │   │   ├── ...
        │   │   └── fileN.jpg
        │   ├── .../
        │   └── 427/
        ├── 1/
        │   ├── 1/
        │   │   ├── file1.jpg
        │   │   ├── ...
        │   │   └── fileN.jpg
        │   ├── .../
        │   └── 427/
        └── 2/
            ├── 1/
            │   ├── file1.jpg
            │   ├── ...
            │   └── fileN.jpg
            ├── .../
            └── 427/
```
### Granularity hierarchy

Although the images of BRCars-196 and BRCars-427 are grouped so that the level of granularity is given by the model, the images can be grouped into other granularity levels. The following figure shows the hierarchical tree with the possible levels of possible granularities.

<p align="center">
    <img src="https://github.com/danimtk/brcars-dataset/blob/main/resources/granularities_hierarchical_tree.png" alt="hierarchical tree of granularity" width="420">
</p>

The images can be grouped by make, model, year and by instance. The granularity per instance allows you to group images belonging to a specific car. This latter granularity is possible due to the nature of the data source, which groups different images from a single real instance of the car.

### brcars196.csv and brcars427.csv files

The files brcars196.csv and brcars427.csv have the same structure (It can be downloaded from this <a target="_blank" href="https://b.link/brcars">link<a>). They have nine attributes, that are:

**id** *- is a unique identifier of each car instance;*

**model_id** *- is the identifier of the car model;*

**model_label** *- the textual label of the car model;*

**make_id** *- the make identifier of the car;*

**make_label** *- the textual label of the car;*

**year** *- the year of the car fabrication;*

**persp** *- the perspective of the car contained in the image (**c** for cockpit and **e** for external);*

**uri** *- uniform resource identifier to image file;*

**split** *- the split of data (**0** for train split, **1** for validation split, and **2** for the test).*


### Citation
If you use BRCars in your research we would appreciate a citation to the paper:
```
@inproceedings{kuhn2021brcars,
  title={BRCars: a Dataset for Fine-Grained Classification of Car Images},
  author={Kuhn, Daniel M and Moreira, Viviane P},
  booktitle={2021 34nd SIBGRAPI Conference on Graphics, Patterns and Images (SIBGRAPI)},
  year={2021},
  organization={IEEE}
}
```

