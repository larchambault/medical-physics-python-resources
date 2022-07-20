# Medical physics python resources

[TOC]

## General medical physics tool

### PyMedPhys

- *repository*: <https://github.com/pymedphys/pymedphys>

- *documentation*: <https://docs.pymedphys.com/>

- *Overview*:

  > PyMedPhys aims to be a Medical Physics open source [monorepo](https://cacm.acm.org/magazines/2016/7/204032-why-google-stores-billions-of-lines-of-code-in-a-single-repository/fulltext) where we can all store, review, use, and learn off of each other’s code. It is a library of tools that we all have access to and, because of its [license](https://choosealicense.com/licenses/agpl-3.0/), will all have access to whatever it becomes in the future. It is inspired by the collaborative work of our physics peers in astronomy and their [Astropy Project](http://www.astropy.org/).

## DICOM manipulation

### Pydicom

- *Repository*: https://github.com/pydicom/pydicom

- *Overview*:

  > Pydicom is a pure Python package for working with [DICOM](http://en.wikipedia.org/wiki/DICOM) files such as medical images, reports, and radiotherapy objects.
  >
  > Pydicom makes it easy to read these complex files into natural pythonic structures for easy manipulation. Modified datasets can be written again to DICOM format files.

- *Python version*
  - 2.7
  - 3.4+

### RT-Utils
- A minimal Python library for RT Struct manipulation
- *Repository*: https://github.com/qurit/rt-utils
- *Overview*:

> RT-Utils is motivated to allow physicians and other users to view the results of segmentation performed on a series of DICOM images. RT-Utils allows you to create or load RT Structs, extract 3d masks from RT Struct ROIs, easily add one or more regions of interest, and save the resulting RT Struct in just a few lines!

### DicomRTTool
- *Repository*: https://github.com/brianmanderson/Dicom_RT_and_Images_to_Mask
- *Overview*

> DicomRTTool, which is designed to alleviate several of the most time-consuming aspects of data preparation by quickly identifying unique region of interest (ROI) names and where image sets with all ROIs are located and then converting DICOM images and RT structures into NumPy arrays and SimpleITK images. It also allows for the conversion of prediction NumPy arrays to DICOM RT structures.
- *Publication*: Anderson et al. PRO, 2021, 10.1016/j.prro.2021.02.003


### Dicompyler core 

- *repository*: https://dicompyler-core.readthedocs.io/en/latest/readme.html
- *Overview*:

  > A library of core radiation therapy modules for DICOM / DICOM RT used by [dicompyler](http://www.dicompyler.com/). This package includes:
  >
  > - `dicomparser`: parse DICOM objects in an easy-to-use manner
  > - `dvh`: Pythonic access to dose volume histogram (DVH) data
  > - `dvhcalc`: Independent DVH calculation using DICOM RT Dose & RT Structure Set

- *Python version*:
  - 2.7
  - 3.4+

- *Reference*:

  - DOI: [10.5281/zenodo.1212458](https://zenodo.org/record/1212458#.W1XqFnZKh5E)

### DVH analytics

- *repository*: https://github.com/cutright/DVH-Analytics

- *Overview*:

  > DVH Analytics is a software application to help radiation oncology departments build an in-house database of treatment planning data for the purpose of historical comparisons and statistical analysis. This code is still in development. Please contact the developer if you are interested in testing or collaborating.
  >
  > The application builds a SQL database of DVHs and various planning parameters from DICOM files (i.e., Plan, Structure, Dose). Since the data is extracted directly from DICOM files, we intend to accommodate an array of treatment planning system vendors.
  >
  > In addition to viewing DVH data, this software provides methods to:
  > - download queried data
  > - view plan contours
  > - create time-series plots of various planning and dosimetric variables
  > - calculate correlations
  > - and generate multi-variable linear regressions.

- *Python version*:

  - 2.7

- *Reference*:

  - JACMP 2018: [10.1002/acm2.12401](https://aapm.onlinelibrary.wiley.com/doi/abs/10.1002/acm2.12401)

### pynetdicom3

- *Repository*: https://github.com/pydicom/pynetdicom3

- *Overview*:

  > *pynetdicom3* is a pure Python (2.7/3.4+) program that implements the DICOM 
  > networking protocol. Working with [pydicom](https://github.com/pydicom/pydicom), it allows the easy creation of DICOM *Service Class Users* (SCUs) and *Service Class Providers* (SCPs).
  >
  > The main user class is `AE`, which is used to represent a DICOM Application Entity. Once the `AE` has been created you would typically either:
  > - Start the application as an SCP by specifying the presentation contexts that you will support, then calling `AE.start()`and waiting for incoming association requests
  > - Use the application as an SCU by specifying the presentation contexts you want the peer SCP to support, then requesting an association via the `AE.associate(addr, port)` method, which returns an `Association` thread.
  >
  > Once the application is associated with a peer AE, DICOM data can be sent between them by utilising the DIMSE-C services (see the DICOM Standard Part 7, Sections [7.5](http://dicom.nema.org/medical/dicom/current/output/html/part07.html#sect_7.5), and [9](http://dicom.nema.org/medical/dicom/current/output/html/part07.html#chapter_9)).

- *Python version*:

  - 2.7
  - 3+

## Radiomics

### pyradiomics

- *Repository*: https://github.com/Radiomics/pyradiomics
- *Overview*: 

  > This is an open-source python package for the extraction of Radiomics features from medical imaging.
  >
  > With this package we aim to establish a reference standard for Radiomic Analysis, and provide a tested and maintained open-source platform for easy and reproducible Radiomic Feature extraction. By doing so, we hope to increase awareness of radiomic capabilities and expand the community.
  >
  > The platform supports both the feature extraction in 2D and 3D.

- *Python version*:
  - 2.7
  - 3.4+
- *Reference*: American Association of Cancer Research, 2017: [10.1158/0008-5472.CAN-17-0339](http://cancerres.aacrjournals.org/content/77/21/e104)



## Quality assurance

### pylinac
- *Repository*: https://github.com/jrkerns/pylinac
- *Documentation*: https://pylinac.readthedocs.io/en/stable/index.html
- *Paper*: Zaila et al. Physica Medica 2016, https://doi.org/10.1016/j.ejmp.2016.07.122
- *Overview*: 
  > Pylinac provides TG-142 quality assurance (QA) tools
  > Pylinac contains high-level modules for automatically analyzing images and data generated by linear accelerators. Most scripts can be utilized with <10 lines of code. The built in GUI is also straight-forward although programming experience may help identify errors.
  > The library also contains lower-level hackable modules & tools for creating your own radiation therapy algorithms.

### QATrack+

- *Website*: http://qatrackplus.com/
- *Repository*: https://bitbucket.org/tohccmedphys/qatrackplus
- *Overview*:
  > QATrack+ is a fully configurable, free, and open source (MIT License) web application for managing QA data for radiation therapy and medical imaging equipment. QATrack+ is now used in many hospitals and clinics [around the world](http://qatrackplus.com/#whos-using)! Visit the QATrack+ homepage at [http://qatrackplus.com](http://qatrackplus.com/)
  >
  > QATrack+ is deployable on most operating system/server/database platform combinations. It was developed in the popular Python programming language using the Django web framework so that QC data may be entered, reviewed, and analyzed using a web browser.
  >
  > Take a look at the [screenshots](https://bitbucket.org/tohccmedphys/qatrackplus/wiki/screenshots) to get an idea of the interface.

### TARDIS
- *Repository*: https://github.com/LamLay/TARDIS-Updated
- *Paper*: Lay et al. SoftwareX, 2022, https://doi.org/10.1016/j.softx.2022.101146 
- *Overview*
  > A Tool for Approximating Radiotherapy Delivery via Informed Simulation (TARDIS): a model that predicts machine parameters at treatment delivery using trajectory files from prior patients

## Imaging

### Spekpy

- *Website*: https://bitbucket.org/spekpy/spekpy_release/wiki/Home
- *Repository*: https://bitbucket.org/spekpy/spekpy_release/src/master/
- *Overview*

> SpekPy is a powerful and free software toolkit for calculating and manipulating x-ray tube spectra. The code is written in the Python programming language. It can be used in a Python interpreter or from a Python script. For more information on SpekPy, please see [Further information](https://bitbucket.org/spekpy/spekpy_release/wiki/Further%20information).