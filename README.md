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

we repeat the process for the rest of CSVs: Coaches, EntriesGender, Medals, Teams:

We preview the data for Coaches:

![Screenshot 2024-02-19 at 23 04 33](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/72d1478d-7ba9-4818-a9bd-e99259269b40)

we connect the 2 datas and validate:

![Screenshot 2024-02-19 at 23 07 34](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/b2e79400-1b8c-4f6d-818f-0289c0605cac)

now Coaches.csv is in the Raw Data directory:

![Screenshot 2024-02-19 at 23 16 31](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/ef804064-9379-43be-ba1c-a0598108a57a)

![Screenshot 2024-02-19 at 23 30 21](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/1b2a3849-f840-4520-9603-6bee417b6970)

we have the 5 CSVs in Raw data:

![Screenshot 2024-02-19 at 23 35 41](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/a3630f0c-9db6-49f4-bc57-0fd6c64d2e7c)

we create a new Azure Databricks workspace:

![Screenshot 2024-02-19 at 23 38 06](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/a83b876b-4766-4d71-8f10-1807a91227d0)

We Launch the Workspace:

<img width="190" alt="Screenshot 2024-02-19 at 23 40 41" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/7a97be1e-260b-4e5f-9d90-99600483b3e4">

<img width="616" alt="Screenshot 2024-02-19 at 23 41 05" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/8f7af256-0ed4-435c-8713-f5a0a62b161f">

We create Compute:

![Screenshot 2024-02-19 at 23 43 51](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/ded27080-16f2-4163-8397-052444c16efa)

we open a new notebook:

![Screenshot 2024-02-19 at 23 47 01](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/c6c858fb-89b7-4cff-9984-784561418a8e)

we go to App registrations and create new:

![Screenshot 2024-02-19 at 23 49 24](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/c5d10ec7-e39b-4a97-a528-6dd1817b8f2a)

we copy the Application ID and the Directory ID in a notepad.

We go to Certificates and create New client secret. we copy the secret key into a notepad.

and we copy it in the notebook from Databricks:

![Screenshot 2024-02-19 at 23 53 52](https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/5877bbb9-f37c-401a-aca8-5774d3932c49)

see the code in the repository file: Tokyo Olympic Transformation.ipynb


We go to Azure Synapse Analytics:

<img width="786" alt="Screenshot 2024-02-20 at 00 15 00" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/6a443038-c1f8-43b6-8ef0-53deb89c67cb">

<img width="590" alt="Screenshot 2024-02-20 at 00 15 46" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/83379269-fcff-4c6f-b4fe-cba751f1218f">

we go to Synapse Studio:

<img width="583" alt="Screenshot 2024-02-20 at 00 16 44" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/d0eeb894-cc4a-44d1-945f-2c644e5decaf">

we create a Lake database:

<img width="873" alt="Screenshot 2024-02-20 at 00 21 28" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/49432540-cc4b-4a0c-acf9-6324f59c6e5b">

we create the athletes Table:

<img width="501" alt="Screenshot 2024-02-20 at 00 21 58" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/d20088c6-2a0d-4cff-bb26-cc36924e533b">

we do the same for the rest:

<img width="269" alt="Screenshot 2024-02-20 at 00 23 30" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/cb036d7d-6196-48a8-ba1a-d9891d8afdb1">


<img width="509" alt="Screenshot 2024-02-20 at 00 25 02" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/95e61bd8-4ac0-497e-b293-f8a198f59241">

we create a SQL script:

<img width="489" alt="Screenshot 2024-02-20 at 00 26 19" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/15d26111-cdc6-43df-b17d-dfa759258922">

<img width="562" alt="Screenshot 2024-02-20 at 00 28 36" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/bea7026d-97d8-4d20-85ba-68272d2d078f">


<img width="556" alt="Screenshot 2024-02-20 at 00 30 10" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/db849d6f-4340-4be0-aa88-59702b350407">

you have charts to understand better the data:


<img width="568" alt="Screenshot 2024-02-20 at 00 31 01" src="https://github.com/redjules/Azure-Data-Engineering-Olympic-Data-Analytics/assets/106017493/1b8571ab-86d3-4948-95b2-38c5dd4b0db9">
