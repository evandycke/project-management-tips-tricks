# ETL project plan

Below is an example of an ETL project plan. For each action, you will find out who should carry it out :
* DBA : DataBase Administrator
* ETLA : ETL Architect
* ETLM : ETL Manager
* ETLD : ETL Developer
* SA : System Administrator
* DQS : Data Quality Specialist

## Step 1 : Setting up the development environment

1. Configure the hardware infrastructure (DBA)
2. Software and tools installation (DBA / ETLA)
3. Put in place documents on best practices and standards (ETLM / ETLA)

## Step 2 : Business needs analysis

1. Review of the emerging documentation with the Data Modeller (ETLA / SA)
2. Definition and documentation of business rules (ETLA / SA)
3. Analysis of source systems (ETLA / SA)
4. Definition of the scope of the project phases (ETLM)

## Step 3 : Design of the data mapping (Logical data mapping)

1. Review of the data warehouse data model (ETLA)
2. Review of business rules (ETLA)
3. Analysis of source systems (ETLA)
4. Creation of the data mapping document (ETLA)

## Step 4 : Data quality strategy

1. Definition of data quality rules (ETLM /DQS)
2. Documentation of data faults (ETLM / DQS)
3. Assignment of liability for data faults (ETLM / DQS)
4. Creation of the data mapping document (ETLM / DQS)
5. Awareness of end users of data faults (ETLM / DQS)
6. Integration of quality rules in the mapping document (ETLM / DQS)

## Step 5 : Development of ETL processes

1. Review of the mapping document (ETLD)
2. Development of simple dimensions (ETLD)
3. Development of SCD-2 dimensions - History (ETLD)
4. Development of SCD-2 dimensions - Incremental (ETLD)
5. Development of fact tables - History (ETLD)
6. Development of fact tables - Incremental (ETLD)
7. Automation of processes (ETLD)

## Step 6 : Unit tests - Quality assurance tests - Acceptance test

1. Setting up the test environment (DBA / ETLA)
2. Creation of test plans and scripts (SA)
3. Loading data (ETLD)
4. Running unit test scripts (SA)
5. Data quality control (SA)
6. Data validation (SA)
7. Validation of business rules (SA)
8. Obtaining acceptance (ETLM)

## Step 7 : Deployment

1. Creation of supporting documents (ETLA)
2. Creation of recovery mechanism documents (ETLA)
3. Establishment of the production environment (ETLA)
4. Loading historical data (ETLA)
5. Incremental process scheduling (ETLA)

## Step 8 : Maintenance

1. Development of audit reports for known issues (ETLA)
2. Checking the execution logs (ETLA)
3. Establishment of the production environment (ETLA)