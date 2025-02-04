Standalone mode (Run as administrator)
---
- setting
    - download JDK and add it's path into Enviroment variable ->system variables -> path
    - use powershell to run bash command
- master
```gherkin=
cd C:\Users\PRLab\Documents\spark-3.5.3-bin-hadoop3\bin
spark-class org.apache.spark.deploy.master.Master
```
- worker
```gherkin=
cd C:\Users\PRLab\Documents\spark-3.5.3-bin-hadoop3\bin 
spark-class org.apache.spark.deploy.worker.Worker spark://192.168.0.102:7077
```
- python connect to cluster
```gherkin=
spark = SparkSession.builder \
    .appName("AIS Data Processing") \
    .master("spark://192.168.0.102:7077") \
    .config("spark.executor.memory", "4g") \
    .config("spark.executor.cores", "2") \
    .getOrCreate()
```
How does the system behave under Node/CPU/Memory/Hardware/... errors and failures?
---
### Node
- two node, stop one -> application is still working
  
![image](https://hackmd.io/_uploads/B1ETPsC_kl.png)
![image](https://hackmd.io/_uploads/B15DOj0dkx.png)
![image](https://hackmd.io/_uploads/SyvGcoROkx.png)
![image](https://hackmd.io/_uploads/SJILdiRdyl.png)
- stop two, application stop
![image](https://hackmd.io/_uploads/Byjq5oCdJg.png)
- add new node, app start working
![image](https://hackmd.io/_uploads/HyE1nsCuJg.png)




### Disk
- Disk space not enough, the app can't work
![image](https://hackmd.io/_uploads/SJW3miJt1g.png)




What happens during network interruptions and partitioning?
---
If a worker node stops, the app will continue to function as long as other worker nodes are available to connect.


How do error handling mechanisms affect efficiency/scale/latency/throughput/... etc.? Are there any worst/best case considerations?
---
### affect
1. Efficiency
- Using parallel downloading (ThreadPoolExecutor) allows multiple files to be downloaded simultaneously, improving efficiency.
- However, if some files fail to download, the program may need to retry or skip them, potentially slowing down the process.
2. Scalability
- Apache Spark’s distributed architecture enables scalability, but if errors (such as CSV file format issues) are not handled properly, they can impact the overall computation.
- The check for the "Type of mobile" column is a protective measure, but if the dataset has numerous format variations, scalability could still be affected.
3. Latency
- In the downloading process: If a ZIP file request (requests.get(url)) fails, the program directly raises an exception (raise_for_status()), which may terminate execution and increase latency.
- In data processing: If CSV reading fails, Spark may stop the entire computation process.
4. Throughput
- Using union() to merge DataFrames increases Spark’s computational load. Applying repartition() can optimize performance.

### Best/Worst Case Considerations
#### Best Case
- All files download successfully without errors, maximizing the benefits of ThreadPoolExecutor for parallel execution.
- The CSV files are formatted consistently, allowing Spark to read and process them without issues.
- Spark effectively utilizes memory and CPU resources, enabling high throughput.
#### Worst Case
- Some download links fail (e.g., 404 or 500 errors), and without a retry mechanism, the program crashes.
- CSV file formats are inconsistent, causing Spark to fail when parsing columns (inferSchema=True may misinterpret column types).
- Too many union() operations consume excessive computational resources. Using repartition() can help optimize performance.


