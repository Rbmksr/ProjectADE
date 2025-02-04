# Project Advanced Data Engineering

### Outline
This project compares the processing of maritime data using Apache Spark and Pandas. The data comes from the Automatic Identification System (AIS), which is used by ships worldwide to transmit position and navigation information. The goal is to assess the performance of both approaches in processing large datasets.

### Structure
Our project consists of 4 different Notebooks.
1. ADE_PRO_Spark: 
This notebook presents the prototype of our use case, implemented using Apache Spark. It also includes discussions on the use case, the limitations of the prototype, and our observations regarding the behavior of both Spark and Pandas.
2. ADE_Pro: 
This notebook contains the prototype of our use case but implemented using Pandas instead of Spark for data handling. It focuses solely on the Pandas implementation.
3. Scalability: 
This notebook documents tests related to scalability, including the effects of varying data volumes and different hardware configurations.
4. Fault Tolerance: 
This notebook contains tests designed to explore various aspects of Spark’s fault tolerance.

### Data
Our project uses Danish AIS data (further explained in the ADE_PRO_Spark notebook). The data source is available at: https://web.ais.dk/aisdata/.

You can obtain the data in two ways:

Automatic Download: Run the AIS_PRO_Spark notebook, which will automatically create a folder and download the files used during testing.
Manual Download: Download the data manually from the source. If you choose this option, you must update the local_storage_path variable in all four notebooks to reflect the location where you saved the files.
The exact files used during testing can be found at the following links:
1. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip
2. https://web.ais.dk/aisdata/aisdk-2024-03-02.zip
3. https://web.ais.dk/aisdata/aisdk-2024-03-03.zip
4. https://web.ais.dk/aisdata/aisdk-2024-03-04.zip
5. https://web.ais.dk/aisdata/aisdk-2024-03-05.zip

### Order of Execution
We recommend starting with the notebook ADE_PRO_Spark to gain an overview of the use case and our thought process throughout the project. After that, you can explore the ADE_Pro notebook to experience the performance differences between the Spark and Pandas versions and compare their implementations.

Additionally, you can use the Scalability and Fault Tolerance notebooks independently to review the various tests we conducted.

### Download Time Results with Spark
The download time for 5 files with Spark is 0 minutes and 0 seconds.
