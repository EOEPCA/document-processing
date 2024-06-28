# Application Package Processing Engine

## Introduction to the overall EMS/ADES architecture 

The OGC initiatives in Testbed-13, Testbed-14, and Testbed-15 have pioneered the development of an advanced architectural framework designed to facilitate the ad-hoc deployment and execution of applications proximate to the data source. This strategic positioning minimizes data transfer, enhancing efficiency between data repositories and application processes.

These testbeds laid the foundational design for an architecture that supports the encapsulation, deployment, and execution of Earth Observation Applications across distributed Cloud Platforms. This framework ensures that applications are efficiently integrated and managed within cloud environments, providing scalable solutions for Earth Observation data processing.

Building on established OGC standards such as WPS (Web Processing Service) and OWS-Context, these testbed activities have refined the concept of Application Packages. These packages encapsulate data processing applications or workflows, allowing for streamlined deployment and execution across varied Cloud Platforms.

The WPS service played a pivotal role by enabling end-user portals and B2B client applications to submit processing parameters, initiate on-demand or systematic data processing requests, and establish data pipelines for retrieving the processed information.

Each Application Package contains detailed specifications about the execution units or workflow scripts to be executed, along with configurations for parameterization or customization. This modular approach facilitates the precise tailoring of processing workflows to specific project needs.

The architecture articulated in these testbeds integrates the Application Package with key services: the Execution Management Service (EMS) and the Application Deployment and Execution Service (ADES). The EMS orchestrates the deployment and invocation of processing services workflows, leveraging multiple deployment and execution platforms through WPS-T, a transactional extension of WPS. The ADES, in turn, functions as the execution engine, managing the application lifecycle previously configured as a WPS service by the EMS.

The EMS orchestrates the application package across the selected ADES platform, managing the deployment and execution of workflow components either locally or remotely. It ensures a streamlined operation from deployment to execution, fostering a responsive and agile processing environment.

Primary responsibilities of the ADES include:

- Validating and approving application deployment and execution requests from the EMS.
- Managing the execution of processes within the processing cluster, ensuring robust performance and reliability.
- Monitoring ongoing process execution to maintain operational integrity and performance.
- Retrieving and delivering processed results efficiently, ensuring data integrity and accessibility.

Additionally, the ADES handles critical sub-steps such as the staging-in of input data and the staging-out of output data, essential for maintaining a seamless flow in data processing activities. This comprehensive approach not only enhances operational efficiency but also ensures that the architecture can support complex, data-intensive workflows in an optimized manner.

## Evolution of the Application Package

The OGC Innovation Program's Earth Observation Applications Pilot, conducted between December 2019 and July 2020, investigated the software architecture initially developed through OGC Testbeds 13-15. This architecture facilitated the deployment and execution of externally developed applications on Earth Observation (EO) data and processing platforms.

The pilot program served as an evaluation of the interoperability frameworks previously established in OGC Testbeds 13 to 15, proving to be a foundational step for conducting maturity assessments within operational environments. During the pilot, further enhancements and precise definitions were crafted, which refined the process for deploying and executing applications across a variety of platforms with nly minimal modifications required.

The Pilot validated the strategy of using Docker for secure and efficient application packaging, and HTTP Web APIs or Web Services for managing and executing applications. Moreover, the pilot defined clear application patterns that govern data inputs and outputs, reinforced the use of the Common Workflow Language (CWL) for detailed application description, execution, and workflow construction. It also endorsed the adoption of the SpatioTemporal Asset Catalog (STAC) to serve as a comprehensive data manifest, delineating the necessary inputs and outputs for applications. These advancements collectively enhance the deployment flexibility and interoperability of applications within diverse EO data ecosystems.

The conclusion of the OGC Earth Observation Applications Pilot emphasized the need for standardized subsets of the Common Workflow Language (CWL) that all platforms should support. This standardization was reckoned essential to ensure that application developers experience consistency and predictability when deploying their applications across different platforms. As a result, the pilot advocated for the creation of an OGC Best Practice document that would outline the use of CWL within application packages.

This proposed Best Practice document would aim to serve as a comprehensive guide, addressing the diverse application design patterns explored during the pilot. It would provide detailed guidelines for the automated generation of CWL, enabling a more streamlined and efficient development process for EO applications. This initiative would seek to enhance the interoperability and usability of Earth Observation data and processing platforms by leveraging CWL’s robust framework for describing and executing workflows, thereby fostering a more unified and effective approach to application development within the geospatial community.

# The Common Workflow Language and the OCG Earth Observation Application Packages.

CWL was selected as the open standard to support the packaging of Earth Observation applications in several OGC activities and these are depicted below:


``` mermaid
flowchart LR
    subgraph References["`**References**`"]
      subgraph Testbed-13
        tb13["`EP Application Package Engineering Report (17-023)
            Application Deployment and Execution Service Engineering Report (17-024)
            Cloud Engineering Report (17-035)`"]
    end
    subgraph Testbed-14
        tb14["`Application Package Engineering Report (18-049r1)
            ADES & EMS Results and Best Practices Engineering Report (18-050r1)`"]
    end
    subgraph Testbed-15
        tb15["`Catalogue and Discovery Engineering Report (19-020r1)`"]
    end
    end
    subgraph eoap["`**Earth Observation Applications Pilot**`"]
        eoaper["`20-042 Terradue Engineering Report
                20-045 CRIM Engineering Report
                20-038 European Union Satellite Centre Engineering Report
                20-043 EOX Consortium Engineering Report
                20-037 Pixalytics Engineering Report
                20-034 Spacebel Engineering Report`"]
        summary-er["EO Applications Pilot 
        Summary Engineering Report (20-073)"]
        eoaper --> summary-er
    end
    Testbed-13 --> eoap
    Testbed-14 --> eoap
    Testbed-15 --> eoap
    summary-er --> bp["`Best Practice for Earth Observation Application Package (20-089)`"] 
    bp --> tb16["`Testbed-16: Earth Observation Application Packages with Jupyter Notebooks`"]
    bp --> tb17["`Testbed 17: COG/Zarr Evaluation Engineering Report`"]
    bp --> tb18["`Testbed-18: Testbed-18: Reproducible FAIR Best Practices Engineering Report`"]
```


