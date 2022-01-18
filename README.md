# Data Pipeline Python, Google Cloud Platform, and Google Data Studio
1. Data Collection and Cleansing with Python from MySQL and REST API.
2. Extracted the data into Landing zone with Google Cloud Storage.
3. Transform data using Apache Spark and loaded into Google BigQuery.
4. Visualisation with Google Data Studio
5. The pipeline is orchestrated using Airflow with Cloud Composer (GCP).

# Data
Data collection from MySQL as a list. Then it was converted into Pandas DataFrame called audible_transaction. There were 2269 rows of data.

<img width="529" alt="Screen Shot 2565-01-18 at 18 25 53" src="https://user-images.githubusercontent.com/73461649/149928809-144df7cc-fd89-48b3-8cd7-a5849cf25cbb.png">

<img width="1441" alt="Screen Shot 2565-01-18 at 18 29 22" src="https://user-images.githubusercontent.com/73461649/149929342-1c8540c7-8881-4e99-b3b8-ea377d8f6639.png">

A transaction data was also imported from MySQL and converted into Pandas DataFrame called audible_data

<img width="519" alt="Screen Shot 2565-01-18 at 18 30 33" src="https://user-images.githubusercontent.com/73461649/149929489-ce074a77-1ae8-4b18-ada5-f8f699a62343.png">

Both tables were joined.
<img width="1450" alt="Screen Shot 2565-01-18 at 18 33 35" src="https://user-images.githubusercontent.com/73461649/149929905-53a4200e-5344-4efa-85c5-7350bdb53dc3.png">

Nevertheless, the price was listed as a USD but the client required the price to be listed as THB.
A conversion rate was imported through REST API.

<img width="216" alt="Screen Shot 2565-01-18 at 18 31 25" src="https://user-images.githubusercontent.com/73461649/149929615-ec06e3ce-4111-4bdf-b61a-848a2a3a3913.png">

Completed transformed data

<img width="1445" alt="Screen Shot 2565-01-18 at 18 35 28" src="https://user-images.githubusercontent.com/73461649/149930167-fee04880-a312-47e5-a26d-426ead4c5b9f.png">


# Visualisation with Google Data Studio
A view was created to illustrated the neccesary data: revenue, country, book name, customer id, category, purchased date, book id.

The first dashboard illustrated the overview which included the revenue of the business, no. of customer, transaction by country, besting selling book, and best selling categories.
<img width="1197" alt="Screen Shot 2565-01-18 at 18 01 31" src="https://user-images.githubusercontent.com/73461649/149925506-800b75f7-5d3d-4055-9fcd-f737789e4ac7.png">

The second dashboard illustrated "search book by revenue". It consists of a user defined parameter that will match result with the search criteria. 
<img width="1198" alt="Screen Shot 2565-01-18 at 18 01 37" src="https://user-images.githubusercontent.com/73461649/149925510-3902aed4-4163-4986-92fe-9d9dcaad18cd.png">
<img width="1195" alt="Screen Shot 2565-01-18 at 18 01 46" src="https://user-images.githubusercontent.com/73461649/149925515-9e3bd2b4-8bcc-4c1e-8833-aa24a81d100c.png">
