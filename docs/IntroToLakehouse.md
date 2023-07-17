Late 1980s businesses wanted to harness data-driven insights for business decisions and innovation.

Move from relational databases to systems that could manage and analyze data that was being generated at high volumes at a faster pace.

### **Data warehouses** were the solution
- PROS
    - Business intelligence
    - Analytics
    - Structured and clean data
    - Predefined schemas
- CONS
    - No support for semi or unstructured data
    - Inflexible schemas
    - Struggled with volume and velocity upsticks
    - Long processing time

<br>

Early 2000s Big Data explosion introduced data lakes.

### **Data Lakes**
- PROS
    - Flexible data storage (Structured, semi-structured and unstructured)
    - Streaming support
    - Cost efficient in the cloud
    - Support for AI/ML 
- CONS
    - No transactional support
    - Poor data reliability (mostly due to the various formats)
    - Slow analysis performance (due to large volume of data)
    - Data governance concerns
        - creates challenges with security/privacy enforcement
    - Data warehouses still needed

![Complex technology stack](img/complex_techonoly_stack.PNG)

- Introduced complexity and delay
- Data had to be copied between the systems

<br>

### **Data Lakehouse**

- Developed as an open architecture combining the benefits of a data lake with the analytical power and controls of a data lakehouse
- Single reliable source of truth
    - Can store all data of any type together
    - This provides direct access for AI and BI together

- PROS
    - Transaction support (ACID guarantees)
    - Schema enforcement and governance
        - for data integrity and robust auditing needs
    - Data governance
        - to support privacy regulation and data use metrics
    - BI support
        - to reduce latency between obtaining data and drawing insights
    - Decoupled storage from compute
        - each operates on their own clusters allowing them to scale independently
    - Open storage formats (such as Apache Parquet)
    - Support diverse data types
        - Access structured, semi-structured and unstructured data in one location
    - Support for diverse workloads
        - All teams (data science, ML, SQL analytics) access the same data repository
    - End-to-end streaming
        - For real time reports