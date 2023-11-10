# nosql-challenge
Eat Safe, Love

Part 1: Database and Jupyter Notebook Set Up

The data provided in the 'establishments.json' was imported using a database named 'uk_food' and a collection named 'establishments'. It was imported using `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`. The dependencies were then imported and an instance of MongoClient was created. The new database was confirmed, before assigning the 'uk_food' database with the variable 'db' and reviewing the collections in the database. The function find_one was used to review a document in the establishments collection. 

Part 2: Update the Database

A dictionary was created for the new halal restaurant that hasn't been reviewed yet. That dictionary was the inserted usiing the insert_one function. The BusinessTypeID for Restaurant/Cafe/Canteen were found, using only the BusinessTypeID and BusinessType fields, and it was used to update the halal restaurant's BusinessTypeID with the corrent ID. As the magazine was not interested in any establishments in Dover so, all establishments where the LocalAuthorityName was Dover were found and removed from the collection. The number values for latitude, longitude and the were stored as strings so, they were converted decimal numbers and RatingValue into integers. 

Part 3: Exploratory Analysis

The number of establishments that had a hygiene score of 20, a total of 41 establishments, was determined using the count_documents function. The results were then converted to a Pandas DataFrame. The number of establishments within London with a RatingValue greater than or equal to 4, a total of 33 establishments, were counted also using the count_documents function, and the results were placed in a Pandas DataFrame. The top 5 establishments with a RatingValue of 5 was then sorted by the hygiene score, in relation to the proximity of the halal restaurant "Penang Flavours". These results were also placed in a Pandas DataFrame. The number of establishments in each Local Authority that had a hygiene score of 0, a total of 55 establishments, were determined using a pipeline and the results were imported to a Pandas DataFrame. 