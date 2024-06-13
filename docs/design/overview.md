# Architecture

The _Processing Building Block_ includes multiple Processing Engines and Runners, as it is designed to support a range of processing workflow approaches and execution environments:

- **Processing Engines**: The _Processing Building Block_  is capable of supporting one or more
processing workflow approaches. These include:
    
    - OGC Application Packages via OGC API Processes (deployment, instantiation and execution).

    - openEO Process Graphs via the openEO Specification.

- **Processing Runners**: The _Processing Building Block_ should supports the execution of processing workflows in various extensible execution environments. Previous projects focused
mainly in Docker and Kubernetes, some experiments were also performed in OGC activities for High-Performance Computing (HPC) by GeoLabs and EURAC, and Terradue for Argo Workflows. Other possible environments for Processing Runners
include also, but are not limited, to Dask Cluster and Apache Airflow.
