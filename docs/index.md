# Introduction

The _Processing Building Block_ is designed to provide capabilities for the hosted execution of processing workflows.

These workflows are defined either as OGC Application Packages or as openEO Process Graphs. 

The key to successful execution of user-defined processing (such as algorithms or models) within a platform is the availability of appropriately curated input data that meets the specific needs of the processing workflow.

## About the Processing Building Block

The main goal of the _Processing Building Block_ is to offer a consistent and reliable data foundation upon which developers of processing workflows can depend. 

To achieve this, a generic data curation approach is favoured, allowing the needs of various processing workflows to be met across multiple platforms. This approach eliminates the necessity for each individual platform to develop its own unique data integration solutions.

Included in the Processing Building Block components, the _Processing Engine_ offers a versatile and scalable solution for managing and executing EO data processing workflows, with the added
capability of integrating with various backend execution environments and supporting data discovery processes.

The _Processing Engine_ functions as follows:

- **Service API Provider**: The Processing Engine offers a service API through which processing workflows are submitted for execution. This API is the primary interface for users to interact with the Processing BB, facilitating the submission and management of processing tasks.

- **Support for openEO and Data Discovery**: In the case of openEO, the Processing Engine also encompasses functionalities related to data discovery. This integration signifies that the engine not only manages processing tasks but also aids in identifying and retrieving relevant datasets for processing.

- **Integration with Backend Execution Environments**: The architecture of the _Processing Building Block_ is designed to support an extensible set of backend execution environments capable of running the processing workflows. This extensibility means that the Processing Engine can be adapted to various deployment scenarios, enhancing its versatility and applicability.

- **Role in Workflow Management**: The _Processing Engine_ plays a central role in the workflow management ecosystem of the EOEPCA project. It acts as the gateway through which processing requests are channelled, managed, and executed, interfacing with other components like Processing Runners, Data Sources, and Processing Clients.

For effective implementation, the Processing BB is envisioned to be modular in design, making it adaptable and extensible. This modular structure enables it to meet diverse processing requirements and integrate smoothly with different platform architectures.

## Capabilities

The relevant use cases for the _Processing Building Block_ are centred around the architecture and components that enable efficient and adaptable processing workflows. 

It comprises the following key components, each addressing specific aspects of processing in EO:

- **Processing Engine**: Serves as the core component, providing a service API for submitting processing workflows. In some instances, it also includes functionalities for data discovery. This engine is crucial for initiating and managing processing tasks.

- **Processing Runner**: Offers the execution environment for the processing workflows. It is designed to be plugged into the Processing Engine for specific deployment scenarios, providing the necessary computational resources and environment for processing tasks.

- **Processing Data Source**: Integrates with data sources to make datasets available as inputs for processing workflows. This component ensures that the required data is accessible and in the correct format for processing, bridging the gap between data storage and processing functionalities.

- **Processing Client**: A library with bindings for common programming languages such as Python, facilitating programmatic access to the Processing Engine's services via its API. This client enables developers and users to interact with the Processing Engine, submit jobs, and manage workflows programmatically.

- **Processing Development Tooling**: Includes tools that support the development, visualisation, and packaging of processing workflows. These tools are essential for the creation and testing of new processing algorithms and models, enhancing the usability and accessibility of the _Processing Building Block_.

The _Processing Building Block_ includes multiple Processing Engines and Runners, as it is designed to support a range of processing workflow approaches and execution environments: