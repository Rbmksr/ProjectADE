# Project Advanced Data Engineering

### Outline
This project compares the processing of maritime data using Apache Spark and Pandas. The data comes from the Automatic Identification System (AIS), which is used by ships worldwide to transmit position and navigation information. The goal is to assess the performance of both approaches in processing large datasets.

### Structure
Our project consists of 4 different Notebooks.
1. ADE_PRO_Spark: 
This Notebook contains the prototype of our use case using Apache Spark for the Implementation. This notebook also contains texts regarding our use case, the limitations of the prototype and our observations of the behaviour of both Spark and Pandas.
2. ADE_Pro: 
This Notebook contains the protopye of our use case using Pandas instead of Spark to handle the data. This Notebook contains only the Pandas Implementation.
3. Scalability: 
This Notebook contains tests and their documentation regarding topics such as different volumes of data and different hardware configurations.
4. Fault Tolerance: 
This Notebook contains tests seeking to answer questions regarding different topics of Sparks fault tolerance.

### Data
Our Project usese Danish AIS Data (further explanations in the Notebook ADE_PRO_Spark). The source of the data is the following site: https://web.ais.dk/aisdata/. You can either manually Download the data we use or simply execute the notebook AIS_PRO_Spark. This will automatically create a folder and download the files we used during testing. If you choose the manual download you have to update a variable called local_storage_path in all 4 notebooks with the path where you saved the files. The links to the exact files we used during testing are:
1. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip
2. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip
3. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip
4. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip
5. https://web.ais.dk/aisdata/aisdk-2024-03-01.zip

### Order of Execution
We recommend you to start with the notebook ADE_PRO_Spark, in order to get an overview of the use case and our thoughts while doing the project. After that you can use the notebook ADE_Pro to experience the difference in performence between the Spark version and the Pandas version and compare the code of the different implementations. You can use the notebooks Scalability and Fault Tolerance individually to watch the different tests we conducted.
