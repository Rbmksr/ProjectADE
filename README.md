Vergleich von Datenverarbeitung mit Spark und Pandas

Projektbeschreibung

Dieses Projekt vergleicht die Verarbeitung von Schifffahrtsdaten mithilfe von Apache Spark und Pandas. Die Daten stammen aus dem Automatic Identification System (AIS), das von Schiffen weltweit zur Übermittlung von Positions- und Navigationsdaten genutzt wird. Ziel ist es, die Leistungsfähigkeit beider Ansätze bei der Verarbeitung von großen Datensätzen zu bewerten.

# Project Advanced Data Engineering

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


### Ergebnisse der Download-Zeitmessung mit Spark
Die Download-Zeit für 2 Dateien mit Spark beträgt 6 Minuten und 46 Sekunden.

### Download Time Results with Pandas
The download time for 5 files with Pandas is 1 minutes and 52 seconds.
The download time for 5 files with Pandas is 1 minutes and 20 seconds.
The download time for 4 files with Pandas is 1 minutes and 8 seconds.
The download time for 4 files with Pandas is 1 minutes and 16 seconds.
The download time for 3 files with Pandas is 0 minutes and 49 seconds.
The download time for 2 files with Pandas is 0 minutes and 34 seconds.
The download time for 1 files with Pandas is 0 minutes and 23 seconds.
The download time for 2 files with Pandas is 0 minutes and 32 seconds.
The download time for 2 files with Pandas is 1 minutes and 34 seconds.
The download time for 2 files with Pandas is 6 minutes and 17 seconds.
The download time for 2 files with Pandas is 7 minutes and 31 seconds.

### Download Time Results with Spark
The download time for 5 files with Spark is 0 minutes and 0 seconds.
The download time for 4 files with Spark is 0 minutes and 0 seconds.
The download time for 3 files with Spark is 0 minutes and 0 seconds.
The download time for 2 files with Spark is 0 minutes and 0 seconds.
The download time for 1 files with Spark is 0 minutes and 0 seconds.
The download time for 5 files with Spark is 5 minutes and 49 seconds.
The download time for 2 files with Spark is 6 minutes and 4 seconds.
The download time for 2 files with Spark is 6 minutes and 41 seconds.
