# Nestlé Case Study
This project aims to build a data pipeline involving the ingestion, processing, and storage of data in a Data Lake utilizing the **Azure** architecture.

# The Challenge
You have been provided with 6 distinct datasets: **Positions (Cargos), Zip Code (CEP), Clients, Employees, Level, and PQ.**
Remember that we are the largest consumer goods company in the world, and in a real-world scenario, you will work with much larger datasets.

### Must-have:
* **ETL and Documentation.**
* **Language Selection:** Choose a language to demonstrate your logic (**Python, PySpark, Scala, or R**).
* **Technical Requirement:** Utilization of at least 2 functions (**Window, GroupBy, Union**).
* **Responsibility:** You are responsible for processing and establishing relationships between these bases in the best possible way!
* **Deliverable:** A presentation or commented code with documentation (or both).

### Nice to have:
* 5 relevant insights from the presented datasets.
* Utilization of an extra Library/Framework (e.g., **Pandas**).
* Logic or handling for **sensitive data (PII)**.
* **Data visualization**.

---

# Pipeline Architecture

![alt text](IMG/pipeline.JPG)

# Technologies

* **Ingestion:** Python  
* **Processing:** PySpark (Databricks)  
* **Storage:** Azure Data Lake Storage Gen 2  
* **Data Format:** CSV, Parquet  
* **Cloud:** Azure  
* **Analytical Storage:** Azure Synapse Analytics  
* **Version Control:** BitBucket  
* **Data Visualization:** Power BI  
* **Tools:** Git, GitHub, Figma  

---

# Scenario

**Data** The data for this project is extracted from six CSV files containing information about employees of a fictional company. 

**Data Pipeline Overview** The pipeline begins with the ingestion of data into **Azure Data Lake Storage (ADLS) Gen 2** using Python. Inside **Databricks**, the CSV files are consumed from the **Raw** layer. After this stage, the data undergoes validations and transformations and is moved to the **Processed** layer. Once processed, the data is consumed by **Azure Synapse Analytics** for large-scale analysis. Finally, **interactive dashboards in Power BI** are created for results visualization and decision-making. Additionally, the infrastructure required for the pipeline execution is provisioned and managed using **Terraform**, ensuring automated creation and configuration of Azure resources.

### Project Steps:

1.  **Data Ingestion:** The first stage of the pipeline is data ingestion into **Azure Data Lake Storage (ADLS) Gen 2** using **Python**. The CSV files are sent to the Data Lake for further processing.  
    
    ![alt text](IMG/upload_python.JPG)

2.  **Raw Layer Reading:** Before starting the transformations, the data is read in CSV format from the raw layer.  
    
    ![alt text](IMG/adls.JPG)

3.  **Data Treatment (Validations and Transformations):** The data undergoes a treatment process, which includes necessary validations and transformations, such as data cleaning and adjustments according to business requirements.  
    
    ![alt text](IMG/databricks.JPG)

4.  **Storage in the Processed Layer:** After treatment, the processed data is moved to the **Processed layer**, where it is stored with high quality and ready for deeper analysis.  
    
    ![alt text](IMG/processed.JPG)

5.  **Consumption by Azure Synapse Analytics:** The data is consumed by **Azure Synapse Analytics**, where external tables are created that connect to the processed layer.  
    
    ![alt text](IMG/image.png)

6.  **Insight Generation:** With the data already cleaned and adjusted, insights are generated for data analysis and exploration.  
    
    ![alt text](IMG/query.JPG)

7.  **Power BI Dashboard Creation:** Finally, **interactive dashboards** are created in **Power BI**, offering a visual interface for presenting the data in the pipeline.  
    
    ![alt text](IMG/intro.jpg)  
    ![alt text](IMG/dashboard.JPG)

8.  **Infrastructure as Code (Terraform):** The infrastructure required to support the data pipeline is provisioned using **Terraform**, ensuring consistency, automation, and ease of environment replication. This includes the configuration of **Azure Data Lake Storage (ADLS) Gen 2**, **Databricks**, **Synapse Analytics**, and other dependencies used in the project.
