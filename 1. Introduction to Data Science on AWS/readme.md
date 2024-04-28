# Benefits of Cloud Computing


## Key Points:
- Cloud computing enables on-demand access to IT resources via the internet.
- Pay-as-you-go pricing model eliminates the need for maintaining physical infrastructure.
- AWS offers a wide range of services, including AI and ML, built on decades of expertise.


### 1. Agility

Cloud computing enables quick and easy resource deployment for rapid experimentation. Users can test new tools or enhance processing with minimal risk, as resources can be quickly scaled up and then decommissioned if experiments fail.


### 2. Cost Savings

Cloud computing helps us save money by allowing us to pay only for the compute resources we use, without making upfront investments in hardware. We can cut costs further by using Amazon EC2 Spot Instances, which offer up to a 90% discount on unused AWS capacity. Additionally, Reserved Instances and Savings Plans provide savings through prepaid options.

### 3. Elasticity
Cloud computing allows for automatic scaling of resources to align with application demands. For instance, if a data science application experiences a surge in model requests, resources can be scaled up automatically. Conversely, when demand decreases, the resources scale down. This eliminates the need for overprovisioning resources to manage peak loads.

### 4. Innovate Faster
Cloud computing speeds up innovation by freeing us from the time-consuming management of infrastructure. It allows businesses to focus on developing unique applications and experimenting with new algorithms, frameworks, and hardware quickly, reducing setup times from months to seconds.

### 5. Deploy Globally in Minutes
Cloud computing enables rapid global deployment of data science applications, allowing businesses to serve customers worldwide efficiently. AWS uses a network of Regions and Availability Zones (AZs), which are clusters of data centers located around the world. This structure not only facilitates proximity to customers, enhancing application performance and response times, but also helps in adhering to local data-privacy laws. The number of AWS Regions and AZs is expanding continuously to support wider global coverage.


<br />

## Data Science Pipelines and Workflows
![](./image/1.png)

<br />

## Pipelines:
- ### Amazon SageMaker:
#### are the standard, full-featured, and most complete wayto implement AI and machine learning pipelines on Amazon SageMaker. 

- ### Kubeflow Pipelines:
#### is a relatively new ecosystem built on Kubernetes that includes an orchestration subsystem called Kubeflow Pipelines. With Kubeflow, we can restart failed pipelines, schedule pipeline runs, analyze training metrics, and track pipeline lineage.

- ###  Apache Airflow on AWS:
#### popular option primarily built to orchestrate data engineering and extract-transform-load (ETL) pipelines.

- ### MLflow: 
#### MLflow is an open source project that initially focused on experiment tracking but now supports pipelines called MLflow Workflows. We can use MLflow to track experiments with Kubeflow and Apache Airflow workflows as well


## Amazon AI Services:

![](./image/2.png)

<br />

### - Data Lake:
A data lake is a centralized, secure repository that allows for the storage, governance, discovery, and sharing of data at any scale. It supports various kinds of analytics and uses multiple AWS services without requiring data transformation. Data lakes store structured, semi-structured, and unstructured data, and can ingest real-time data, making them useful for data science and machine learning teams to develop and deploy accurate models.

Amazon S3, an object storage service, is integral for data lakes on AWS, offering high durability and consistent access. It allows for data organization with stringent access controls to satisfy business and compliance needs.

AWS Lake Formation enhances data lake creation by collecting, cataloging, and securing data from databases and object storage with the help of machine learning. AWS Glue provides a scalable, serverless data catalog and preparation service, including an ETL engine and data transformation capabilities. It also features AWS Glue DataBrew, which facilitates data ingestion, analysis, visualization, and transformation through an easy-to-use interface.

## Model Deployment with Amazon:

1. **SageMaker Endpoints:** This method is ideal for applications requiring low-latency, real-time predictions. A SageMaker endpoint is created to host the model, providing a REST API for serving predictions. This service supports auto-scaling and is deployed across multiple Availability Zones (AZs) to ensure high availability.
2. **SageMaker Batch Transform:** Suitable for scenarios where predictions are needed for entire datasets rather than in real-time. This service is optimized for high throughput, using a batch process that spins up resources to handle large-scale predictions on data stored in S3. After processing, the results are saved back to S3 and the resources are decommissioned.
3. **Serverless Model Deployment with AWS Lambda:** For serverless predictions, a model trained with SageMaker can be served using an AWS Lambda function. This function retrieves the model from S3 and provides predictions. It is important to note that Lambda has limitations in terms of memory and latency, which should be tested thoroughly if considering this deployment option for large-scale use.