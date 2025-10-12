# Introduction

The documentation for the `<BB>` building block is organised as follows...

* **Introduction**<br>
  Introduction to the BB - including summary of purpose and capabilities.
* **Getting Started**<br>
  Quick start instructions - including installation, e.g. of a local instance.
* **Design**<br>
  Description of the BB design - including its subcomponent architecture and interfaces.
* **Usage**<br>
  Tutorials, How-tos, etc. to communicate usage of the BB.
* **Administration**<br>
  Configuration and maintenance of the BB.
* **API**<br>
  Details of APIs provided by the BB - including endpoints, usage descriptions and examples etc.

## About `<BB>`

The Processing Editor provides a GUI for creating and executing processes on EOEPCA backends.

## Capabilities

Both the _openEO API_ and the _OGC API - Processes_ are supported.

The functionalities include:

- discovering available resources such as imagery collections and processing functions,
- combining them into workflows using a GUI graph builder,
- and submitting those for actual calculation, including job management and visualisation of the results.

## Design

The [EOEPCA Processing Editor](https://github.com/EOEPCA/processing-editor) is a clone of the [openEO Web Editor](https://github.com/Open-EO/openeo-web-editor/), just with a custom design and added functionality regarding _OGC API - Processes_.

It is a dockerised Node.js project serving a [Vue.js](https://vuejs.org/) web app, utilising the [openEO JS Client](https://github.com/Open-EO/openeo-js-client) and [openEO Vue Components](https://github.com/Open-EO/openeo-vue-components/), and leveraging [OpenLayers](https://openlayers.org/) and [CodeMirror](https://codemirror.net/).
