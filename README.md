# Azure Data Engineering Olympic Data Analytics

In this project, we will extract the data from API using Azure Data Factory, the data pipeline tool available on Azure that will build a flow like this: 

![Screenshot 2024-02-19 at 20 50 42](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/bd0a3e59-53a7-4816-9132-29180744d818)

and load our data on Azure Data Lake storage so first we will load the raw data then using Azure Databricks we will write our spark code and transform our data and load our data back to our transform Data Lake storage. Once done, we will use Synapse Analytics to run the SQL queries on top of the transform the data so that we can find the insights and get the visualization on top of it.

![Screenshot 2024-02-19 at 20 54 56](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/301a589d-83d9-4aeb-b49f-051f17592804)



![Screenshot 2024-02-19 at 20 53 27](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/3d927fc1-832f-46fe-98de-1cd46c8dd6e3)

# Architecture

![Screenshot 2024-02-19 at 20 48 02](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/c831b105-d65d-4081-83e5-2bfc4be8d401)


# Data

We will take the Olympic data that is available on Kagel (see files in the repository) or in this link: 

https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo

