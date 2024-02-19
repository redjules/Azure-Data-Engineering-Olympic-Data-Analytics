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


# Azure

We create a storage account:

![Screenshot 2024-02-19 at 21 43 38](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/3bb3fb4b-bb69-4b20-be0b-68c2bce096b8)

![Screenshot 2024-02-19 at 21 58 19](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/b493c25e-7e69-4b5c-9a40-e1dbf92fa917)

![Screenshot 2024-02-19 at 22 00 41](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/41a01e58-2dbc-4c25-bf38-5c42bb107dc4)

we go to Containers:

![Screenshot 2024-02-19 at 22 02 44](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/c9da32e5-5ce1-406d-bcae-69b12c6ac757)

we create 2 directories, 1 for raw data and the other for the transformed data:

![Screenshot 2024-02-19 at 22 23 00](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/444e7e35-0f0a-46df-94ae-a97d29d355fa)

we go to Data factory and create a data factory:

![Screenshot 2024-02-19 at 22 26 38](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/a6bad1eb-cca6-4c73-9714-f1de54002aeb)

![Screenshot 2024-02-19 at 22 27 51](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/f6743143-e9ba-496d-b59e-da1e2fe00078)

We launch the studio:

![Screenshot 2024-02-19 at 22 28 54](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/2a9c17a4-eb76-444a-b25e-7d6066b318fd)

we create a pipeline:

<img width="1298" alt="Screenshot 2024-02-19 at 22 35 18" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/80453ff6-cc6b-45bf-8c9a-41409b726227">

we copy data and source http:

![Screenshot 2024-02-19 at 22 34 59](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/aa9da169-c94f-48d5-979c-9ceafef20e55)

and csv:

![Screenshot 2024-02-19 at 22 42 07](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/ba508867-8458-44aa-b4f7-a59a232cab3d)

we use the link from the raw data from github:

![Screenshot 2024-02-19 at 22 44 46](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/1bcf453b-b0bf-4f32-8c76-21a1b1f5b864)

![Screenshot 2024-02-19 at 22 45 26](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/ad9b4f08-ba86-48c7-aaae-3d2d769d2c7f)

we preview the data:

![Screenshot 2024-02-19 at 22 46 42](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/82cf5aed-91e4-4897-a42c-e7d050de97cb)

![Screenshot 2024-02-19 at 22 48 50](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/a49e7e61-954f-4480-8a7d-f711b118e208)

In Sink, we go to Gen 2 and CSV:

![Screenshot 2024-02-19 at 22 51 36](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/4f804ea3-9212-4389-8aaa-8428e54246db)

![Screenshot 2024-02-19 at 22 52 49](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/dcd8e1ac-abc6-47e7-8381-fabf80c3f32b)

![Screenshot 2024-02-19 at 22 53 39](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/da3b1e71-1587-4fc7-af11-9c19173f68a6)

we validate and debug:

![Screenshot 2024-02-19 at 22 57 57](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/10f86be4-8168-423b-a3ae-1cc97ce46bd0)

now it's in our raw data directory:

![Screenshot 2024-02-19 at 22 59 17](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/2e869a8b-f07b-47e2-9282-b918675b85f6)

we repeat the process for the rest of csvs: Coaches, EntriesGender, Medals, Teams:

We preview the data for Coaches:

![Screenshot 2024-02-19 at 23 04 33](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/72d1478d-7ba9-4818-a9bd-e99259269b40)

we connect the 2 datas and validate:

![Screenshot 2024-02-19 at 23 07 34](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/b2e79400-1b8c-4f6d-818f-0289c0605cac)

