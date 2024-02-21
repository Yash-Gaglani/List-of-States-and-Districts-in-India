# Indian States and Districts

This repository contains a collection of Indian states and districts, following the data maintained by the Government of India. 


## JSON Structure

The JSON file is structured with the following properties for each document:

- `_id`: The unique identifier for the state, as maintained by the Government of India.
- `stateName`: The name of the state.
- `districts`: An array containing the districts within the state. Each district object includes:
  - `code`: The district code as maintained by the Government of India.
  - `name`: The name of the district.

## Importing the JSON into MongoDB

To import this JSON file into your MongoDB database, follow these steps:

1. **Download the JSON File**: Ensure the JSON file is downloaded to your local system or accessible on your server.

2. **Use `mongoimport` Command**: Open your terminal or command prompt and navigate to the directory containing the JSON file. Use the `mongoimport` tool to import the file into your MongoDB database with the following command:

```sh
mongoimport --db yourDatabaseName --collection yourCollectionName --file path_to_your_file/Indian_States_and_Districts.json --jsonArray
```




## Example

```json
[
  {
    "_id": "1",
    "stateName": "Jammu And Kashmir",
    "districts": [
      {
        "code": "1",
        "name": "Anantnag"
      },
      {
        "code": "623",
        "name": "Bandipora"
      },
      // Additional districts...
    ]
  },
  // Additional states...
]

```


## CSV Structure

The CSV file is structured with the following columns:

- `_id`: The unique identifier for the state, as maintained by the Government of India.
- `stateName`: The name of the state.
- `districts[0].code`, `districts[1].code`, ..., `districts[74].code`: The codes for up to 75 districts within the state, as maintained by the Government of India.
- `districts[0].name`, `districts[1].name`, ..., `districts[74].name`: The names of up to 75 districts within the state.
- `_class`: (If applicable) A column used to store additional metadata for object mapping in MongoDB or similar NoSQL databases.

Please note, that each state may have a varying number of districts; thus, not all columns may be filled for every state. Empty columns are expected for states with fewer than 75 districts.

## Importing the CSV into the SQL Database

To import this CSV into your SQL database, you might use the following general command or its equivalent in your database management system:

```sql
LOAD DATA INFILE 'path/to/your/csv/Indian_States_and_Districts.csv'
INTO TABLE your_table_name
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 LINES;
```

Please adjust path/to/your/csv/Indian_States_and_Districts.csv, your_table_name, and any specifics related to your SQL dialect and database requirements.


##Usage
This dataset is intended for use in applications that require detailed geographical information about India, including state and district-level data. It's ideal for analysis, mapping projects, or any application where such granularity is necessary.

##Contributions
Your contributions are welcome! If you have suggestions for improving the dataset or the documentation, please feel free to submit an issue or pull request.
