# Tutorials

## Where to search for tutorials

The Github organization [EOAP](https://github.com/eoap) includes a set of repositories with training material regarding the Earth Observation Application Package.

This set of repositories aims to:

* help developers create Earth Observation (EO) applications using the Common Workflow Language (CWL)
* provide an overview of the CWL, its key concepts
* how to build a CWL-based EO application using practical examples in field guides

### Application Package and CWL as a solution for Earth Observation portability

[![stability-wip](https://img.shields.io/badge/stability-wip-lightgrey.svg)](https://github.com/mkenney/software-guides/blob/master/STABILITY-BADGES.md#work-in-progress)

This documentation provides an introduction to CWL as a solution for the portability of EO applications

Documentation available at: https://eoap.github.io/cwl-eoap/

Repository available at: https://github.com/eoap/cwl-eoap

### Understanding STAC for input/output data modelling in Earth Observation Applications

[![stability-wip](https://img.shields.io/badge/stability-wip-lightgrey.svg)](https://github.com/mkenney/software-guides/blob/master/STABILITY-BADGES.md#work-in-progress)

Documentation and notebooks for understanding the role of STAC as input/output data manifests in Earth Observation applications and a hands-on with real-life scenarios

Documentation available at: https://eoap.github.io/stac-eoap/

Repository available at: https://github.com/eoap/stac-eoap

### Quickwin - A simple Application Package for getting started

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)

This tutorial is designed for developers, scientists, and Earth observation enthusiasts who want to get started with the EO Application Package.

Documentation available at: https://eoap.github.io/quickwin

Repository available at: https://github.com/eoap/quickwin 

### Mastering Earth Observation Application Packaging with CWL

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)


This tutorial is designed for developers, scientists, and Earth observation enthusiasts who want to enhance their skills in creating and sharing EO Application Packages.

Documentation available at: https://eoap.github.io/mastering-app-package

Repository available at: https://github.com/eoap/mastering-app-package

### Quickwin - An Application Package with inline Python code

[![stability-wip](https://img.shields.io/badge/stability-wip-lightgrey.svg)](https://github.com/mkenney/software-guides/blob/master/STABILITY-BADGES.md#work-in-progress)

This tutorial is designed for developers, scientists, and Earth observation enthusiasts who want to get started with the EO Application Package.

Repository available at: https://github.com/eoap/quickwin-inline-code

### Open and reproducible EO Application Package

[![stability-wip](https://img.shields.io/badge/stability-wip-lightgrey.svg)](https://github.com/mkenney/software-guides/blob/master/STABILITY-BADGES.md#work-in-progress)

Many cloud-based solutions for workflows in EO are available to users today, but only few support reproducibility or comply with FAIR data principles. 

This short tutorial demonstrates how EO Application Packages meet these requirements.

Documentation available at: https://eoap.github.io/open-reproducible-app-package

Repository available at: https://github.com/eoap/open-reproducible-app-package

### Inference with the EO Application Package

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)

This tutorial addresses the packaging of the inference using an ONNX model. 

Documentation available at: https://eoap.github.io/inference-eoap

Repository available at: https://github.com/eoap/inference-eoap

## References

### Common Workflow Language

Common Workflow Language User Guide, a guide to introduce you to writing workflows using the Common Workflow Language (CWL) open standards

User guide available at: https://www.commonwl.org/user_guide/

**Specification and standards**

* Common Workflow Language specification: https://www.commonwl.org/specification/
* Common Workflow Language Standards, v1.2: https://www.commonwl.org/v1.2/
* Common Workflow Language Standards, v1.1: https://www.commonwl.org/v1.1/
* Common Workflow Language Standards, v1.0.2: https://www.commonwl.org/v1.0/

### OGC documents

* OGC 20-089r1 Best Practice for Earth Observation Application Package: https://docs.ogc.org/bp/20-089r1.html
* OGC 20-073: OGC Earth Observation Applications Pilot: Summary Engineering Report: http://docs.opengeospatial.org/per/20-073.html
* OGC 20-042: OGC Earth Observations Applications Pilot: Terradue Engineering Report: http://docs.opengeospatial.org/per/20-042.html

### SpatioTemporal Asset Catalogs

* **STAC Item** is the core atomic unit, representing a single spatiotemporal asset as a GeoJSON feature plus datetime and links: https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md
* **STAC Catalog** is a simple, flexible JSON file of links that provides a structure to organize and browse STAC Items. A series of best practices helps make recommendations for creating real world STAC Catalogs: https://github.com/radiantearth/stac-spec/blob/master/catalog-spec/catalog-spec.md
* **STAC Collection** is an extension of the STAC Catalog with additional information such as the extents, license, keywords, providers, etc that describe STAC Items that fall within the Collection: https://github.com/radiantearth/stac-spec/blob/master/collection-spec/collection-spec.md
* **STAC API** provides a RESTful endpoint that enables search of STAC Items, specified in OpenAPI, following OGC's WFS 3: https://github.com/radiantearth/stac-api-spec

## Tools

* **cwltool** the reference reference implementation of the Common Workflow Language standards: https://github.com/common-workflow-language/cwltool
* **calrissian** a CWL runner for Kubernetes: https://duke-gcb.github.io/calrissian/