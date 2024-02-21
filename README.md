# Indian States and Districts

This repository contains a collection of Indian states and districts, following the data maintained by the Government of India. The data is structured for easy import into MongoDB or any other NoSQL database.

## Data Structure

The data is organized as a JSON array, with each element representing a state. Each state object has the following structure:

- **`_id`**: The state code as maintained by the Government of India.
- **`stateName`**: The name of the state.
- **`districts`**: An array of district objects within the state.
  - **`code`**: The district code as maintained by the Government of India.
  - **`name`**: The name of the district.

Feel free to use this data for various applications related to Indian states and districts. Contributions and improvements are welcome!

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

