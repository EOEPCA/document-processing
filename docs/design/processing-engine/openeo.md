# OpenEO Processing Engine

EOEPCA supports earth observation processing via the [openEO](https://openeo.org/) standard.
We recommend reading up on openEO to understand the basic motivation.

In openEO terminology, a processing engine is referred to as a 'back-end'. Various open source and proprietary back-ends already exist.
A back-end implements the openEO API on top of a specific technology stack. This means that implementations often differ in terms of the capabilities and processes of
the openEO API that it implements. 

Back-ends also offer a number of 'collections' which represent (earth observation) datasets that can be processed on that backend.
Hence, data access and processing can be optimized in a specific instance.

## openEO Geotrellis

This component will be further documented in it's own [repository](https://github.com/Open-EO/openeo-geopyspark-driver/blob/master/README.md).

It is built on top of the Geotrellis Scala library, utilizing [Apache Spark](https://spark.apache.org/) for high performance distributed computing.

This backend targets various container orchestrators such as Kubernetes and Apache YARN and can also run standalone in a simple Docker container.
For HPC, we recommend to simply orchestrate multiple standalone instances using e.g. SLURM, or explore [more complex](https://github.com/Open-EO/openeo-geotrellis-kubernetes/blob/master/hpc/hpc.md) options.


## openEO XArray

This backend can be found [here](https://github.com/Open-EO/openeo-processes-dask).

It is built on top of XArray, which relies on Dask for distributed processing. 

Dask can be deployed in a Kubernetes environment, or standalone.
